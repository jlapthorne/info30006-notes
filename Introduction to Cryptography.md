# Intro to Cryptography

## Public key cryptography
### Cryptography
- sending messages which are secret from everyone but the intended recipient
- encrypting: "hiding" the message for sending
- decrypting: "un-hiding" and recovering th emessage

### Before public-key crypto
- secret-key cryptography
  - sender and receiver has to agree on the secret key in advance: have to "meet" somehow
  - same key used for encryption and decryption
  - still used, e.g. AES

### Public-key crypto
- receiver generates 2 keys: public key and private key
  - e: public key (for encrypting), and
  - d: private key (for decrypting)
- public key e is public - people use this to encrypt messages to be sent to the receiver
- receiver keeps the private key secret and uses this to decrypt messages

### RSA (maths)
- 2 large prime numbers - p and q (receiver's side; ~300 digits long)
  - N = p * q
  - e (public key) generated
  - publicise (N, e)
- encrypting a message
  - compute m<sup>e</sup> mod N
- decrypting is possible because she knows p and q
  - anyone else "cannot" - computation takes too long

#### More details
- public key e
  - almost any e will do as long as it's coprime to (p - 1)(q - 1)
    - coprime: 2 numbers are coprime if the only +ve integer that divides them is 1
- encrypting a message w/ padding:
  - pad m with a carefully chosen random string r
  - compute (m r)<sup>e</sup> mod N

#### Details
- how long does e need to be?
  - not very long - padding m with random junk ensures that m<sup>e</sup> mod N is always many times larger than N
  - e = 1 + 2<sup>16</sup> is popular because it makes m<sup>e</sup> easy to compute quickly
  - subtle reasons why small e is insecure
  - http://crypto.stanford.edu/~dabo/abstracts/RSAattack-survey.html

### What is public-key crypto good for
- exchanging a key for secret-key crypto
  - sender
    - generates a secret key
    - encrypts message using secret key
    - encrypts secret key with the receiver's public key, and
    - sends the encrypted message and the encrypted key
  - receiver
    - uses private key to decrypt the secret key
    - and uses the secret key to decrypt the message
- rough picture of how SSL/TLS works
- lots of people sending to the same receiver - e.g. in electronic voting, everyone sends their vote to the Electoral Commission

## Internet voting
### Security requirements
- verifiability: no one can manipulate the output
  - only allow eligible voters to vote at most once
  - voters should get evidence that their vote was cast as intended and counted as cast
- privacy: coercers cannot manipulate the inputs
- achieving both is hard, esp. for remote voting

### FREAK - intercepting SSL/TLS key establishment
- MITM attacker claims client can only use 512-bit RSA (downgrade attack) and buggy client accepts 512-bit key despite only advertising 1024 or 2048-bit RSA
- 512-bit keys easy to factor
- steps
  - client hello: "I'd like to use 1024-bit or 2048-bit RSA or ..."
  - attacker: changes client hello to "I can only use 512-bit RSA"
  - server response: OK, here's my 512-bit RSA-EXP key (w/ valid certificate chain)
  - (buggy) client accepts 512-bit key and uses it to encrypt
  - attacker: uses factored 512-bit key to control SSL/TLS session
