## Symmetric and asymmetric cryptography
- symmetric: one key for both encrypting and decrypting
- asymmetric: public-private key cryptography

## Example: RSA (for the mathematically inclined)
- receiver thinks of 2 large numbers p, q
	- about 300 digits long
	- she multiplies them together to get N=pq
	- she generates the public key e (almost any e will do)
	- she publicises (N, e). This is her full public key
- to encrypt message m, compute
	- m<sup>e</sup> mod N
	- (this means take the remainder when m<sup>e</sup> is divided by N)
- the receiver can decrypt because she knows p and q
	- Euler-Fermat Theorem
	- nobody else can factorise N. The computation takes too long
- what if it’s a yes/no for elections?
	- w/o padding, identical input messages result in identical outputs (thus the meaning is not properly encrypted)
	- to encrypt message m,
		- pad m with a carefully chosen random string r
			- make 2 identical messages look different so the hacker can’t tell they’re the same message
		- compute (m || r)<sup>e</sup> mod N

## TLS
- Transport Layer Security protocol
	- encrypts your communication
	- adds integrity and secrecy?
	- checks the public key of the website you’re talking to to check if that public key really does belong to the organisation that owns this URL
- digital signatures: analog of someone writing a pen signature at the bottom of the contract
	- very different implementation
	- RSA *signature*: something who the person who holds the private key can compute on the message
		- and then can use the public key to verify that the person with the private key signed the message
	- built-in certificates in our PCs: root certificates
		- Symantec signs the statement that a website’s public key is as such
			- certificate
- chain of trust: how they break down
	- CA tricked into issuing certificates
		- junior employees at the corporation, or fraud
	- CAs being compromised
		- not all CAs are equally trustworthy
		- Google had a big dispute with a Chinese CA and kicked them out the accepted CAs in Chrome
- bad example: Western Australia Electoral Commission
	- imagine you’re about to register (w/ IDs), or you’ve done it already and are logging in to cast a vote
	- certificate doesn’t actually belong to Western Australia Electoral Commission, but a cloud service provider
	- one way a TLS certificate can work: a huge corporation that’s hosting many people’s sites could handle TLS for a lot of sites
	- domain name does not match - we would expect to get an error
	- Certificate Subject Alt Name
		- allowed to use the same certificate for all these sites
	- EC watched the ABS
		- DDOS attack
		- bought protection from a 3rd-party company from a DDNS attack
		- interposing (posing in between every connection from the voter to the electoral commission)

# Internet voting - or how to use maths to save democracy
## What’s wrong with this picture?
- people voting multiple times
- electoral manipulation at the server
- can vote for someone else by pretending to be someone else
- changing their vote right on their own PC
- less privacy - someone at the EC might be able to trace back the plaintext

## Case
- in 2015, NSW ran a trial of an electronic voting system
- TLS certificate looked pretty good at that time
- checked crypto libraries, etc. - didn’t find anything wrong
- Alex had the idea of looking not at the main page, but at everything else the internet connection was pulling
	- 5 little pieces of js
	- at the time it was coming from a 3rd party foreign company
		- serving analytics code into the web browser
		- meant to offer information about where voters were getting stuck on the web pages
- 3rd party company was not as careful about privacy as the main iVote page
	- 3rd party company had configured their server insecurely
	- 512 bits long public key
		- possible to intercept the traffic, decrypt the key, expose how everyone who passes through that route voted, changed their vote

## Factoring RSA Export Keys (FREAK)
- a huge part of the strength of RSA is the length of the prime numbers
- first some history
	- around the 1990s, US gov’t restricted the export of strong crypto, in particular of RSA using more than 512-bit keys
	- so lots of servers (and clients) maintained the option to use “export grade” crypto, just in case they had to communicate with a restricted computer
		- everyone else has to deal with this stupid restriction - account for the possibility of having to communicate with the “export grade” restricted servers/clients
		- enforcement stopped, but
	- unfortunately, many still do (or did until very recently)
		- many servers used the same 512-bit key over and over again
- also, there was a bug in the TLS client for a large fraction of browsers
	- where they would accept the export-restricted key even if they haven’t asked for it

### FREAK: how it works
- client: I’d like to use 1024/2048 bit RSA
- attacker modifies message to “I can only use 512 bit RSA”
	- impersonates the web server
	- what does it mean for the attacker to completely impersonate the server?
		- once they’ve factorised the 512 bit key
		- they can, from then on, they can act like the server in every attempt to connect
- server responds w/ 512 bit RSA-EXP key (with valid certificate chain)
	- unfortunately the server keeps serving the same key over and over
		- (not refreshing the key)
- buggy client: accepts 512 bit key, uses it to encrypt
	- buggy since the client did not offer 512 bit in the first place
- attacker can use the factored 512-bit key to control the SSL/TLS session
	- decryption does not actually happen on the fly
- 512-bit “export-grade” RSA now costs about $100 to break running overnight on Amazon’s EC2 cloud

## End-to-end encryption
- E2E is the way that encryption **should** be
	- just means that when you encrypt a message, you encrypt it with a key that only lets the intended receiver can read
- in contrast, to services like Gmail, or Facebook
	- upload might be encrypted using TLS
	- but servers you’re using has access to the content you’ve sent
- Signal uses a different method: Diffie-Hellman Key exchange
	- Alice and Bob
	- everyone knows (part of the protocol)
		- a prime *p*
			- another large prime (300 or 600 digits)
		- a generator *g*
	- secret
		- Alice has a secret *a*
		- Bob has a secret *b*
	- Alice computes A = g<sup>a</sup> mod p
	- Bob sends to B = g<sup>b</sup> mod p
	- Alice sends big A to Bob
	- Bob sends big B to Alice
		- big letters are sent in a way that anybody can read it
	- once we’ve agreed on a shared secret, we have a key to use for symmetric cryptography
	- shared secret: g<sup>ab</sup> mod p
		- how can Alice compute this from little a and big B?
			- S = B<sup>a</sup> = (g<sup>b</sup>)<sup>a</sup> = g<sup>ab</sup> mod p
		- Bob
			- S = A<sup>b</sup> = (g<sup>a</sup>)<sup>b</sup> = g<sup>ab</sup> mod p
		- what’s the big assumption?
			- remember that in RSA: prime numbers are hard to factorise
			- here, the big assumption (discrete log assumption)
				- hard to compute a from A and b from B, even if you know all the other parameters
	- someone who only sees A and B cannot (infeasible) calculate the numbers, but someone who has **one** of the secrets can calculate it (as above)
		- just like RSA, we don’t have a proof that it’s hard to compute discrete logs
			- it’s actually not proven in general that breaking RSA is as hard as breaking the factorisation problem
		- we haven’t even proven that computing g<sup>ab</sup>