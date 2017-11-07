# Infosec
## Course Outline 


## TOC
<!-- TOC -->

- [Infosec](#infosec)
  - [Course Outline](#course-outline)
  - [TOC](#toc)
  - [Guest Lecture on Infosec](#guest-lecture-on-infosec)
  - [Introduction to Security and Privay](#introduction-to-security-and-privay)
  - [Managing Security Risks](#managing-security-risks)
  - [Symmetric and Asymmetric Cryptography](#symmetric-and-asymmetric-cryptography)
    - [RSA](#rsa)
    - [TLS](#tls)
    - [Example: Maths and Democracy: Internet Voting](#example-maths-and-democracy-internet-voting)
    - [FREAK Attacks](#freak-attacks)
    - [End To End Encryption](#end-to-end-encryption)
  - [Digital Signatures and Application of Cryptography](#digital-signatures-and-application-of-cryptography)
  - [Guest Lecture: Digital Privacy Rights, Then, Now and In The Future](#guest-lecture-digital-privacy-rights-then-now-and-in-the-future)
  - [Digital Footprints and Privacy](#digital-footprints-and-privacy)
    - [Digital Footprints](#digital-footprints)
    - [Being Truly Anonymous is Hard](#being-truly-anonymous-is-hard)
    - [Dealing with Anonymity Issues](#dealing-with-anonymity-issues)
    - [Software to use](#software-to-use)
  - [Privacy in the Modern World and Differential Privacy](#privacy-in-the-modern-world-and-differential-privacy)
  - [The Security Audit](#the-security-audit)
  - [Industrial Perspectives of Infosec](#industrial-perspectives-of-infosec)
  - [Knowledge Leakage and Security Analysis](#knowledge-leakage-and-security-analysis)
  - [Concepts](#concepts)
    - [CIA](#cia)
    - [Australian Privacy Principles](#australian-privacy-principles)
    - [Privacy, Anonymity, and Security](#privacy-anonymity-and-security)
    - [Threats, Vulnerabilities, Risks](#threats-vulnerabilities-risks)
    - [The Definition of Infosec](#the-definition-of-infosec)
    - [Properties of a secure system](#properties-of-a-secure-system)
    - [Secrecy and Confidentiality](#secrecy-and-confidentiality)
    - [Privacy and Anonymity](#privacy-and-anonymity)
    - [Authentication](#authentication)
    - [SETA - Security Training and Awareness](#seta---security-training-and-awareness)
    - [Risk Management](#risk-management)
  - [Case Studies](#case-studies)
    - [Election Hacking](#election-hacking)
    - [San Bernadino](#san-bernadino)
    - [Paula Broadwell and David Petraeous](#paula-broadwell-and-david-petraeous)
    - [Mass Surveillance](#mass-surveillance)
    - [IOT Technologies](#iot-technologies)
    - [Security Audits](#security-audits)
    - [Signal Et Al](#signal-et-al)
    - [Others](#others)
  - [Revision Notes](#revision-notes)

<!-- /TOC -->

## Guest Lecture on Infosec 

## Introduction to Security and Privay 

## Managing Security Risks
*"Security is mostly a superstition, life is either a daring adventure or nothing."*

- Today's security risks
  - Drones weaponized
    - Until people have to defend it
  - Encryption clash between governments
  - Russian hacks lmao
  - Overreliance on IOT
  - Leaking of Private Information
  - Integrity of Information
    - Automated misinformation or falsified information as a compromise

## Symmetric and Asymmetric Cryptography 
- symmetric: one key for both encrypting and decrypting
- asymmetric: public-private key cryptography

### RSA

### TLS 

### Example: Maths and Democracy: Internet Voting
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


### FREAK Attacks
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

### End To End Encryption
- The way it should be
  - Encrypt messages so that only the receiver can read 
- In contrast to services such as Gmail or Facebook
  - Servers have access to the content you've written
- Diffie-Hellman: End to End
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
  - Somebody who has one of the secrets can possibly calculate it 


## Digital Signatures and Application of Cryptography 
- "Mathematical link between a message and a public key"
- Sign through private keys, and verify through public keys
  - CAs issue some digital signatures on some public keys
- High entropy - any message will have different digests 
  - Fixed-length hash
  - Has to be computationally infeasible to find two messages that hash to the same digest
    - and that's why we need the hashes to be long
  - If it is feasible, then we can have different 
- Digital signing algorithm works in the digest itself
- Signature collisions make good malware
  - Flak malware: Mess with digital signature that comes from software updates
- Critical to have hash functions where nobody can compute the same values - that's why MD5 and SHA1 is going out
- Two ways to deal with secrets 
  - Diffie Hellman
    - Usually with a new key 
    - Fresh values every time they communicate
    - Suspectible to MITM
  - RSA
    - If public key is fucked, everything else is fucked 
  - They are possible to exchange over SSL/TLS
- Desirable Properties of Secret Messages
  - Resistant to MITM
  - Forward secrecy: When the current key is compromised, past communications are secure
  - Future secrecy: When the current key is compromised, future communication stays secure 
  - Achievable via the use of ephemeral keys 
- Ratcheting Protocol
  - Diffie Hellman plus long term memory of public key exchange when contacts first met

## Guest Lecture: Digital Privacy Rights, Then, Now and In The Future 

## Digital Footprints and Privacy 
- Invasion of Privacy can be Episodic or Systemic
- Freedom from surveillance neede for an informed and reflective citzenship
- Privacy has economic role in innovation, sheltering processes of play and experimentation from which innovation emerges

### Digital Footprints
- You're leaving tons of it around
- Anonymity and Privacy are two different but related concepts 
- How digital footprints are left behind
  - Work habits
    - Cursor trackers
  - Metadata
  - Tagging on Facebook
  - Strangers sharing location and taking pictures
  - Business and services 
  - I know where your cat lives 
- No you can't just turn off your phone
- Governments
  - NSA TAO
  - Who knows how long it's been there 
  - DROPOUTJEEP - software implant on iPhones by the NSA 
  - Government actors are a different level of actors
  - Spying on journalists - Paul Farrell from The Guardian put into investigation with 200 pages of reports
  - NSA DISHFIRE: Collecting SMS every day 
- Practical ways to improve privacy
  - Check and update privacy settings, especially on mobile apps 
  - Turn off settings that share information that is unecessary for the service

### Being Truly Anonymous is Hard
- IP address always transmitted
- Browser tranmists information about the browser config
- Browser history and cookies
- Cloud services that will probably still ahve your data
- Data mining and inference techniques
- Nations can already have deliberate policies to remove anonymity
  - Collection of phone numbers, phone calls, text messages
  - Thailand provides tracking SIM cards to visitors 
- Printers print out small yellow dots to encoded to identify printers

### Dealing with Anonymity Issues 
- Always assume you have less anonymity and privacy when you do things electronically 
- Give out as much personal info as needed 

### Software to use
- Spideroak
- Ricochet
- Signal
- Keypass
- Keybase
- Authenticators
- Yubikeys
- 


## Privacy in the Modern World and Differential Privacy 

## The Security Audit 
- Patch and update
- Strong, unique passwords using password managers  
- Encrypt data at rest
- Encrypt data in transit
- Enable MFA

## Industrial Perspectives of Infosec 

## Knowledge Leakage and Security Analysis 

## Concepts
### CIA 

### Australian Privacy Principles 
See markdown document outlining the APP. 

### Privacy, Anonymity, and Security 
- Anonymity and Privacy are two different but related concepts
  - Anonymity is a subset of privacy
  - Different tools to get 
  - Encryption is good for privacy
  - Without very strong encryption, always assume comms are never just between intended parties
- Privacy and security are different
  - You need often need security to have privacy 


### Threats, Vulnerabilities, Risks
- ![](img/tvr.png)
- Threats
  - Can't be controlled and need to be identified 
- Vulnerabilities
  - Can be treated
  - Weaknesses to be identified 
  - Proactive measures should be taken
- Risks
  - Can be mitigated or managed
  - Risk assessment -> Identify critical assets
  - Asset that has a vulnerability to be exploited by a threat, in consequence and likelihood

### The Definition of Infosec
- Infosec: Protecting information systems against misuse and interference from external parties 
- It happens constantly that data, information and knowledge are leaked to competitors
- Lack of focus on infosec and knowledge leakage 
- "Building systems to remain dependable in the face of malice, error or mischance" - Ross Anderson


### Properties of a secure system
- C Confidentiality
- I Integrity
- A Availability 


### Secrecy and Confidentiality
- Secrecy 
  - Keep data hidden
- Confidentiality
  - Keep someone else's data from unauthorized entities
- Australian Privacy Principles 
  - Read this shit 
  - Familiarize yourself with this shit
- Forward Secrecy
- Future Secrecy

### Privacy and Anonymity
- Privacy
  - Use/disclose a person's data according to a set of rules
- Anonymity
  - Keep identity of a protocol participant secret 
- Integrity
  - Ensure data is correct, prvenintg unauthorized or improper changes

### Authentication
- Verify identity
- Data authentication: Ensure that the data originates from claimed senders 

### SETA - Security Training and Awareness

### Risk Management
![](img/srm.png)
- Identify
- Assess
  - Relative risk of each vulnerability
  - Impact vs Likelihood
    - Impact in dollars and cents 
    - Likelihood of the threat manifesting
- Control
  - For each threat create list of control ideas
  - Formal: Risk management, Policies, Access Control
    - Acces control: Mandatory or discretionary. Can be based on authority in organization
    - Control each risk by: 
      - Safeguards (avoidance), 
      - transfer the risk (transference), 
      - reduce impact by incident response plans (mitigate) 
        - Incident response
        - Disaster recovery
        - Business continuity plan
      - understand and accept (acceptance)
      - Chosen depending on if the vulnerability exists, when attacker's cost is less than potential gain, when potential loss is substaintial, when cost of control \< cost of impact
      - 
  - Informal: SETA
  - Technical
  

## Case Studies
### Election Hacking
### San Bernadino
### Paula Broadwell and David Petraeous
- Communications discovered by capture of IP address 
- http://www.usatoday.com/story/tech/2012/11/13/petraeus-broadwell-email/1702057


### Mass Surveillance 
### IOT Technologies 
### Security Audits 
### Signal Et Al
### Others
- Cyber espinoage charges
- Snowden's revelations 
- Russian/Ukrainian hacking on major retailers, payment processors and banks

## Revision Notes 
- Relationship between Infosec, privacy and cryptography 
  - Make sure you understand the linkbetween the three topics. Understand the definitions, show how constructs relate with one another. 
  - Put things together - mind map it if you need it
- The What, why, when, who, where
  - Why is infosec and privacy is important
  - What does it encompass/'
  - What are we trying to protect and how?
  - What are the threats out there and how are they classified
  - Where did they come from? What can be done about them? What happens if we ignore them?
  - Are the groupings really vital? Is it the same group of threats? Has it changed? What are the new infosec threat buzzwords
  - Think about what it actually means in our daily lives. 
- Think about risks
  - Risks are inherent in every single workshop topic
  - Why does risk play such a big role in infosec discussion? What are the risks and how do we manage them
  - Risks are inherent. Try and get a grip of what it means and what it is that makes it so important in infosec
- What are organizations doing wrong? 
  - What are they doing right?
  - Why is it more important now than it was back then? Is it actually more important, or inherently more important?
  - Strategies that organizations can use to protect important information they need
  - Are we in the need of getting new strategies? 
- Contemporary topics
  - Knowledge leakage
    - It's becoming more interesting these days to everyone because it costs a lot of money. How is this different from data leakage and information leakage
    - Is it the same these days? 
  - Every definition we talk about, try to relate it to our workshops if it's not clear enough just yet.
- In the exams, the questions are very specific. To answer quickly, make sure something's on your mind. These are small questions that you need to come up with a solution fairly quickly, and just move on. Don't really reflect, just be able to get to a solution.
- Australian Privacy Principles matter
  - You'll need it to apply them in your jobs
  - Read this shit motherfucker holy shit, it may even come out on the exam
  - They have legal relevance, but also provide a guide for organizations which cgather or store data on their customers
  - There's an 11 page factsheet, read that shit motherfucker 
- IT Security audit
  - Includes research and knowing the different solutions available to security problems, and their strengths and weaknesses 
- IT Security breach case
  - Excellent case studies for understanding what has or can happen and go wrong
  - Get familiar and get to know how they can be prevented
- Metadata 
  - Few IT byproducts affect security and privacy as much 
  - Be sure you understand the social and legal matters around metadata 
- US and Five Eyes digital surveillance
  - More widespread than we think
  - Be sure you can dimension the nature and scope of the privacy intrusions
- Be sure you can explain why privacy is important
- Understand the barriers to IT anonymity. 