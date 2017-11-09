# Sample exam answers (again)

## Part I: Information Security
1
- Authentication: verify if the other entity in an information transaction is who they say they are
- Accountability: possibility of tracing actions and events to the processes/entities that performed them
- Anonymity: protocol participant(s) cannot be identified
- Auditability: keeping logs and audit trails
- Non-repudiation: service that provides proof of the integrity and origin of data (hashes, signing with certificates)
- Privacy: using/disclosing a person's data according to a state of rules; safeguarding personal data and a personal image
- Reliability, effectiveness/efficiency, compliance, utility

2
- acts of human error/failure
- compromises to IP
- deliberate acts of
  - espionage/trespass
  - information extortion
  - sabotage/vandalism
  - theft
  - software attacks
- forces of nature
- QoS
- technical HW failures/errors
- technical SW failures/errors
- technologoical obsolescence


3
a) business risk: risk which can impact business; project risk: impact is only on one/several projects

b) risk analysis
- risk identification
  - what asset are we trying to protect?
  - what is the context?
- risk assessment
  - from the value and the vulnerability of the asset, we can derive the likelihood and impact of the risk
  - the impact depends on the risk, not the asset
  - assign a risk rating: quantitative (numerical score) or qualitative (HIGH, LOW, etc.)
- control: selecting which strategies (actions to be taken in the future - using a set of formal, informal and technical controls at a tactical and operational level in order to reduce security risk exposure)
  - formal: risk management, policies, etc.
  - informal: SETA
  - technical: firewalls, AV, access control, etc.
- maintenance/review: see how well the asset is doing - has it been exposed? are the existing controls/strategies holding up well against attacks (if any)?

## Cryptography and protocols

4
a) In the 1990s the United States restricted the export of software containing RSA with strengths greater than 512-bit ("export-grade" crypto). This limitation did not affect software from outside the United States and inside the United States.

This was done by US (and UK) intelligence agencies to control the spread of the more effective cryptography techniques - and to monitor the communications of other nations.

In 1996 this restriction is no longer enforced after several legal challenges. However, due to a lot of software (and clients) being from and located in the United States, a lot of clients and servers had to maintain backwards compatibility with 512-bit RSA to ensure that they can communicate with those dated clients.

This is bad, because right now in 2017 you could factorise a 512-bit key (and thus compromise it) in less than a day for $100 (very feasible). The FREAK downgrade attack is one such attack which took advantage of the weakness of 512-bit RSA and bugs in the (web browser) client.

b) **Secrecy???**
Authenticity: make sure you are exchanging keys with the right person
Confidentiality: the keys should be secret to every one else except the intended recipient (both ways)
Integrity: integrity of the data (keys being sent, in this case). In other words, the data has not been tampered with (modified, deleted, etc.) without authorisation.

If the question asked for the secrecy properties of the messaging protocol: forward secrecy and future secrecy
Forward: compromise of long-term keys does not compromise past session keys
Future secrecy: compromise of a session key does not compromise keys in the future

c)
- verifiability: no one can manipulate the output (integrity?)
  - only eligible voters can vote only once
  - voters should get evidence that their vote was cast as intended
- anonymity/privacy:
  - voters' votes should be kept private
  - or votes should not be tied to voters' identity
  - so they cannot be coerced into voting for a specific candidate

d)
Why? End-to-end encryption: only the communicating users can read the messages as only the participants hold the keys to read the messages.

Security feature: "safety number" - the participants can meet up in real life to verify if their communication has not been compromised. This safety number is a fingerprint derived from the public keys of the participants.

How to use it?
1. Open Signal
2. Open the chat
3. Tap the title
4. Tap on "View safety number"
5. Compare the safety number or do a QR scan.

5
a) geotagged photos, search history, user agent strings, IP address

b) UX. From Goldberg 2016 - 30% of users surveyed prioritised ease of use over security. Making using privacy-enhancing technologies painless is crucial in getting that 30% of people to adopt the technologies.

## Privacy

6
a) false - WhatsApp is tied to your phone number

b) Metadata: creation date, signature
Signature: not the message being sent - so it counts as metadata
=> Two of the above

c) false
- there are exceptions (see APP 12.1)

d) all of the above

e) all of the above (APP 1.2)

f) false

7

a)
- location
- time photo is taken + time of upload
  - this might seem far-fetched, however this data can be cross-linked with other data (e.g. location) to practically be a tracking beacon for where you are
- IP address
- user agent string
- ~~EXIF data - camera serial number (rare)~~

b)
Everyone has something to hide. Privacy is not limited to just witholding personal information, but also maintaining your image to the public eye. So even when you do not have "anything to hide", your personal information can still be used against you (incriminate you) - and privacy is necessary to prevent this. A good example is identity theft.

Privacy, of citizens and individuals, also matter collectively. Oppresive regimes have been known to use mass surveillance (which is an overreach in terms of privacy) to suppress voices and uprisings (e.g. UAE, Arab Spring). This can be taken as the extreme, but to some extent, surveillance will enable the influencing (and perhaps blackmail) of individuals.

Cohen (2013) argues that "freedom from surveillance is needed for an informed and reflective citizenship", and later elaborates on that position by showing how surveillance (and thus modulation - enabled by surveillance) stifles innovation by restricting the processes of play and experimentation that drives innovation.
