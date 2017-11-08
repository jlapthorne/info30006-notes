# Summary

## Information Security
- from Cherdantseva and Hilton
  - multidisciplinary area of study and professional activity
  - concerned w/ development and implementation of security mechanisms of all available types
    - technical, organisational, human-oriented and legal
  - in order to keep information in all its locations (within and outside the organisation's perimeter)
    - and, consequently, information systems, where information is created, processed, stored, transmitted and destructed,
  - free from threats
- in other words: defending information
  - preventing the unauthorised access, use, disclosure, disruption, modification, inspection, recording or destruction of information

### Why?
- possibility of monetary loss?

## Assets
- any data, device, or other component of the environment that supports information-related activities
- hardware, software, confidential information, people
- what we are trying to protect

## Threats
- possible danger that might exploit a vulnerability to breach security -> cause harm
- what we're trying to protect against

### List of threats (Whitman, ME & Mattord, HJ 2012)
- human error
- IP compromise - piracy, copyright infringement
- deliberate acts of:
  - espionage/trespass: e.g. unauthorised access, data collection, or even shoulder surfing
  - information extortion: e.g. blackmail
  - sabotage/vandalism: e.g. destruction of systems/information
    - contrast: hacktivism and serious threats such as nation states, cybercriminals
  - theft
  - software attacks: e.g. DDoS, viruses, worms, macros
- forces of nature
- deviations in QoS (quality of service) from service providers
- HW or SW failures/errors
- technological obsolescence

## Vulnerabilities
- weakness which allows an attacker to work around protection efforts

## Risks
- **potential for loss**, damage, or destruction of an asset as a result of a threat exploiting a vulnerability

## Controls
Control, as in "means of limiting/regulating something".
Set of managerial and technical controls to protect information resources.

### Risk management
- applying risk management techniques:
  - identification
  - assessment
  - response
  - review/control
- ref/week3

#### Conceptual/big picture
- threat agent gives rise to threat
- a threat exploits a vulnerability, leading to a security risk
- a security risk has the potential to cause damages to an asset -> risk exposure
- counter-measures against risk exposure: security safeguards
  - strategy, policy, etc.
  - which directly affects (the ability to cause damage of) the threat agent

#### Risk identification
- establish the context: where? who?
- identifying assets, and valuing them
  - no point protecting assets with low "value"
    - low importance
- residual risk: risk that remains after applying a control

#### Risk assessment
- evaluating the relative risk for each vulnerability -> risk rating/score
  - quantitative: textbook definition
    - numerical scores
  - can also be qualitative: LOW, MEDIUM, HIGH, CRITICAL
- also known as: risk evaluation, risk estimation, risk analysis(?)
- determine 2 things:
  - the likelihood of a risk happening
    - likelihood: consider the value and vulnerability of an asset
      - value: no one will be interested to breach security to get a low-value item
      - vulnerability: low-hanging fruit -> bigger risk
    - determination: from past records, experience, simulations, experimentation, specialist/expert evaluation
  - and the impact should the risk be realised
    - usually measured in terms of money ($)
    - depends on the risk, not the asset
      - availability attack on a system has a different cost to a confidentiality attack on a document
        - availability: lost sales, etc.
        - confidentiality: think: lost competitive advantage
  - other impacts of a risk:
    - productivity cost: regaining the asset or reputation
    - penalties: confidentiality agreements have stipulations for breach of confidentiality, etc.

#### Risk control
- selecting which control (strategies) to use
  - categories
    - formal: risk management, policy, etc.
    - informal: SETA
    - technical: firewalls, VPNs, access control, etc.
- access control:
  - system that restricts access to an asset by a user
  - types
    - mandatory: users and data owners have limited control over access to information
      - some users are flat-out not allowed to access sensitive info
    - discretionary: access controls are implemented at the discretion of the data owner
      - "open by default"
    - other:
      - central authority
      - role-based
      - task-based
- maintenance, review (how are we doing now?)

##### Risk control strategies
###### Avoidance
- try to prevent the vulnerability being exploited
  - preferred
  - methods:
    - applying policy
    - SETA
    - technology: firewalls, patches

###### Transferrence
- shift risk to other assets/processes/organisations
- if organisation lacks expertise: hire outside specialist help
  - transfer risk of managing complex systems to said party

###### Mitigation
- reducing impact (of the vuln being exploited)
- 3 types
  - IRP: incident response plan
    - what to do during the incident
  - DRP: disaster reecovery plan
    - how to recover from the fallout
  - BCP: business continuity plan
    - how to stay afloat if shit hits the fan

###### Acceptance
- doing nothing - if asset gets exploited, accept the outcome
- only valid when the value of the asset does not justify the cost of protecting it
- risk appetite:
  - how much risk an organisation is willing to take on versus the cost of applying controls

###### Selection
- level of threat, value of asset
- rules of thumb for applying strategies
  - when a vulnerability exists and can be exploited
  - when attacker's cost is less than potential gain
  - when potential loss is substantial
  - when cost of control is less than cost of impact
- otherwise, not worth the trade-off?

### Policy
- policy:
  - plan/course of action
  - conveys instructions from an organisation's senior management to those who make decisions, take actions, and perform othr duties (Whitman, ME & Mattord, HJ 2012)
- types
  - strategic-level guidance
  - operational-level guidance
  - other terms: "practices", "procedures"
- ref/week9

### Strategy
- strategy:
  - actions to be enacted upon in the future
    - security actions
  - the use of a range of formal, informal and technological controls
  - at a tactical and operational level
  - in order to reduce security risk exposure
- strategy is:
  - prescriptive: involves decision-making about a future course of action
  - multi-faceted -> has tradeoffs
- ref/week10

### SETA - Security Education, Training and Awareness
- control measure designed to positively influence security behaviours of employees
- aims and objectives are drawn from security policy and security strategy (see above)
- after a comprehensive (security) risk assessment,
  - part of the strategy: seeing where SETA fits in, in addition to formal controls and technical controls
    - formal controls e.g. policy

## Privacy
- safeguarding personal data **and** protecting a personal image
  - cryptography (encryption) a means to ensure privacy
- legal, regulatory, political and technological aspects to privacy

## Cryptography
- "art of writing and solving codes" - dictionary definition
- sending messages that are secret from everyone but the intended recipient
- encryption: "hiding" the message for sending, so nobody else can understand it
- decryption: "un-hiding" and recovering the message
- enables secure information transactions through encryption and decryption
- ref/week4

### Debates, legal controversies
- E2E encryption, backdoors
- electronic voting (the "paperless option")
- privacy and big data

### Secret-key cryptography
- sender and receiver had to agree on the secret key in advance - had to "meet" somehow
- encrypting and decrypting uses the same key
  - symmetric
- still used - e.g. AES

### Public-key cryptography
- asymmetric
- receiver generates 2 keys:
  - public key *e* for encrypting
  - private key *d* for decrypting
- receiver publicises the public key *e*
  - people encrypt messages sent to the receiver using *e*
- receiver keeps private key *d* secret
  - to decrypt messages

#### RSA - maths
- receiver: 2 large primes *p* and *q* (~300 digits long)
  - multiplies *p* and *q*  to get *N* = *p* * *q*
  - generate public key *e* (almost any *e* will do)
  - publicises *(N, e)* - her full public key
- encrypting a message
  - compute *m<sup>e</sup> mod N*
- receiver can decrypt because she knows *p* and *q*
  - nobody else can factorise *N* - the computation takes too long

#### Even more details
- *e* will do as long as it is coprime to (p - 1)(q - 1)
- message: padding with a carefully chosen random string r
  - compute (m || r)<sup>e</sup> mod N
  - 2 identical messages will look different -> can't tell if it's the same message
- receiver can decrypt
  - Wikipedia page on RSA + Euler-Fermat Theorem
  - nobody else can factorise N: too long
    - strictly speaking, breaking RSA has never been shown to be as difficult as factorising N, but
    - no one has found a faster way to do it either
- Chinese remainder theorem - more efficient decryption
- how long does e need to be?
  - not very long - padding m witih random junk ensures that m<sup>e</sup> mod N is always many times larger than N
  - e = 1 + 2<sup>16</sup> = 65537 is popular because it makes m<sup>e</sup> easy to compute quickly
  - subtle reasons why small e is insecure
  - https://crypto.stanford.edu/~dabo/abstracts/RSAattack-survey.html

#### Good for?
- exchanging a secret key for secret-key cryptography
  - sender
    - generate a secret key
    - encrypts a message with the secret key
    - encryptes the secret key with the receiver's public key
    - sends the encrypted message and the encrypted key
  - receiver
    - uses private key to decrypt the secret key
    - uses the secret key to decrypt the message
  - almost but not quite how SSL/TLS works

#### TLS
- TLS
  - encrypts communication
  - adds secrecy (confidentiality) and integrity
  - checks the public key of the website you are visiting: if it does belong to the organisation that owns this URL
- digital signatures: digital analog of pen signatures
  - but very different implementation
  - RSA signature: computed using the private key
    - and verifiable using the public key -> verify if private key holder *did* sign the message
    - *d*, computed from *p* and *q*
      - totient: lcm of (p-1) and (q-1)
      - d: modular multiplicative inverse of e (mod totient)
        - d x e mod totient = 1
    - signing: holder of private key has a value d with the property (x<sup>e<sup>d</sup></sup> = x (mod N))
      - getting at d is equivalent to factorising N
      - verify signature: S<sup>e</sup> = Pad(Hash(M)) (mod N)
        - M: message
        - N: public key component
- built-in certs in PCs: root certs
  - => chain of trust
    - can break down if: CA tricked into issuing fradulent certificates, CAs being compromised
- example: Western Australia Electoral Commission
  - cert does not belong to them, but a cloud service provider
  - domain name on the certificate does not match
    - domain name of the EC is in "Certificate Subject Alt Name"
  - this was with good intentions - the EC saw the ABS DDoS attack and bought DDNS protection from a 3rd party
    - the 3rd party interposes (posing in between every connection from the voter to the EC) on all the connections

### Internet voting
#### Picture
- system: voters voting at PCs, encrypted -> sent to EC server -> election outcome
- what's wrong?
  - vote multiple times
  - manipulation at the EC server
  - can vote for someone else by pretending to be someone else
  - changing their vote right on their own PC
  - less privacy: someone at the EC might be able to trace the vote

#### Security properties required
- verifiability: no one can manipulate the output
  - only eligible voters vote, only once
  - voters should get evidence that their vote was cast as intended and counted as cast
  - everyone gets evidence votes were properly tallied
- privacy: coercers cannot manipulate the inputs e.g. by blackmail
- achieving both is hard, especially for remote voting

#### FREAK (factoring RSA export keys)
- 1990s: US gov't restricted export of strong crypto, in particular RSA w/ more than 512-bit keys
  - servers and clients in US can use strong RSA params
  - software made outside US not bound by this restriction
  - software produced in the US but exported outside was restricted to this "export grade" crypto
- lots of servers (and client) maintained option to use "export grade" crypto in case they have to communicate with a restricted client/server
  - many still do
- problem with 512-bit RSA: only costs $100 to break running overnight on Amazon EC2 cloud
- how it works
  - client: "I'd like to use 1024 or 2048-bit RSA"
  - attacker MITM: "I'd like to use 512-bit RSA"
  - server response: OK, here's my 512-bit RSA-EXP key (with valid cert chain)
  - buggy client accepts 512-bit key and uses it to encrypt comms
  - attacker uses factored 512-bit key to control SSL/TLS session

### Diffie-Hellman

### Signal - 3-DH, double ratchet algorithm

# Workshops
## Week 2 - Mass Surveillance
- Four Corners documentary - takeaways
  - relative ease of doing mass surveillance
  - oppresive governments using mass surveillance to suppress revolts and dissents
  - capabilities (Evident system): not just content, but also locations
  - these systems were developed by commercial companies and sold to gov'ts worldwide
  - decryption capabilities - putting governments' communications at risk

### Arguments
- mass surveillance is problematic
  - allows suppressing people
  - could be seen as a breach of individuals' privacy rights
  - no guarantee of lawful use - what protections are there against misuse?
  - data gathered from mass surveillance -> vulnerability
  - quandary (difficult problem): who should have access to the data
  - no evidence that mass surveillance led to improvements
  - inherent ambiguity in governments' wants for data -> imply they want everything
- value neutral
  - can prevent terrorist attacks
  - surveillance is just technology - not inherently immoral. Users abusing it is the problem
    - -> mass surveillance is not inherently oppresive
- who should be allowed to do surveillance?
  - government, handled by law enforcement
  - "nothing to hide"
    - issue: **everyone** has information they want to keep private
    - rephrase: if you have nothing to hide, that means you won't mind if gov'ts mandates a live-feed camera in YOUR bedroom
  - dictatorship vs. proper government
    - corruption: obvious in dicatorships, but is present in some form in every government
    - what stops unscrupulous members from selling surveillance information? misusing it for blackmail?
- who shouldn't be surveilled?
  - politicians -> prevent backmail
  - law enforcement agents -> protects from dangers, but lowers accountability
  - same argument for military personnel
  - individuals in Witness Protection programs
    - protect their identity
    - argument can also be made that surveillance can actually protect them

### Security and privacy
- in this context - national security
- surveillance = "security > privacy"
- but
  - loss of personal privacy
  - loss of freedom of expression
  - possibility of information being misinterpreted - Eckerseley's talk: online chat banter thought to be actual terrorist activity back then -> caused EFF's formation (confirm w/ notes)
  - mass surveillance can be used to control what we do: behavioural patterns -> influencing people

## Week 3 - Blood Service breach
- website outsourced to Precedent Communications
- what happened:
  - Precedent employee accidentally put backup of DB w/ personal info of prospective blood donors on public-facing web server
- APP principles
  - 6: disclosure of personal information
  - 11.1: protection of personal information - take reasonable steps against misuse, interference, loss, unauthorised access, modification or disclosure of personal information
  - 11.2: retention of personal information - take reasonable steps to destroy/de-identify info no longer needed
- Blood Service's mistakes
  - 11.1
    - Information Asset Classification Policy: classify info as sensitive -> tighter controls
    - launch site after PIA (Privacy Impact Assessment)
    - better control measures to protect data in the hands of 3rd party providers
    - external consultants: audit system
  - 11.2
    - shorter data retention time
    - de-identification/destruction of personal information after done w/ use
    - could've extended data retention policy to DonateBlood site
    - limit personal info collected
      - after the incident: any sensitive info required will be collected at a later stage (not through the online form)
- Precedent's mistakes
  - 11.1
    - safeguards - IP authentication, DB backups, dummy data, monitoring systems (suspicious activity)
    - risk assessment, risk mangement policies, external audits to assure security
    - organisational: better SETA, some staff did not have adequate training and education
  - 6
    - UAT (user acceptance testing) environment should've been in a private subnet
    - disable directory browsing
- human errors that could cause incidents (from Verizon and CompTIA's reports)
  - weak passwords
  - low security awareness
  - careless andling of data
- protecting assets from human errors:
  - strategy: prevention
    - backup log
    - safety procedures: dummy data, disable directory browsing
    - SETA
  - strategy: mitigation
    - auditing
    - breach detection
- outsourcing vs insourcing?
  - sensitivity of assets - high sensitivity: better not outsource
  - type of company
    - do not outsource governance, risk and compliance (Vladmir Jirasek)
    - outsource other parts of the security stack: firewalls, NetSec, vuln scanning, etc.
    - do not outsource application security, identity, access control
      - risk surface too big
- outsourcing - adding value
  - specialists might be able to carry out work for less cost
- always keep in mind possibility of failure
  - assume worst case: supplier failing -> should be able to manage the potential fall-out
  - work w/ supplier to minimise risk of such a failure
