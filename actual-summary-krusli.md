# Summary
## InfoSec
Protecting assets against unwarranted access/disclosure/modification/destruction.

### Why?
- protecting privacy/security of individual/organisation
- impact of compromise of InfoSec: $, loss of competitive advantage, etc.

### Concepts
#### Assets
- data/device/component that supports information-related activities

#### Risk, threat, vulnerability
- threat: possible danger that exploits a vulnerability
- vulnerability: weakness (in the system) that enables threat to work around protection efforts
- risk: the potential for loss/damage/destruction of an asset as a result of a threat exploiting a vulnerability

#### Threats
- human error
- IP compromise
- deliberate cats of
  - espionage/trespass
  - information extortion: extortion using information
  - sabotage/vandalism
  - theft
  - software attacks - DDoS, viruses, etc.
  - forces of nature
  - QoS
  - HW/SW failures/errors
  - tech obsolescence

### Properties
- CIA
  - confidentiality: protected against unintended disclosure - for privacy/secrecy
    - privacy: disclosing data according to a set of rules
    - secrecy: hiding data
  - integrity: maintaining correct state of data/information (not modified by unauthorised entities)
  - availability: data/info has to be (usably) available when needed

### Security analysis/risk management
#### Principles
- specification/policy: what system should do
- implementation/mechanism
- correctness/assurance
- human nature: "clever" users

#### Method
- what are we protecting: information assets
  - analyse value + cost of replacement
- who are the threats?
  - motivations, resources, number, likelihood
  - framework
    - action: passive (shoulder surfing) vs. actively attacking?
    - sophistication: script kiddies or nation state?
    - access: external or internal (own staff!)
    - impact: result of system compromise
- what are the security requirements?
  - CIA, availability, access control, privacy?
- which strategies will work?

#### Risk management
- identification -> assessment -> response -> review/control
- ID: context, assets
- assessment: relative risk - risk rating
  - likelihood - value and vulnerability of asset
    - determine from past records or expert evaluation
  - impact - $, depends on risk, not asset
    - other: productivity cost, penalties (from legal agreements etc.)
- control
  - select which strategies to use
  - formal: risk management, policy, etc.
  - informal: SETA
  - technical: firewalls, VPNs, access control, etc.
    - access control: system to restrict access to an asset by user
      - mandatory (MAC): users/data owners have limited control over access of information; controlled by admin/higher-up
      - discretionary (DAC): users/data owners can control access to their own data
      - role-based: real-world approach - assign permissions based on role
      - task-based
      - central authority
- maintenance/review: how are we doing now? revise strategies/applied controls?

#### Concepts
##### Policy
- plan or course of action
- conveys instructions from management to those who make decisions, take actions and perform other duties
  - strategic-level guidance, operational-level guidance
- also called "practices"/"procedures"

##### Strategy
- actions to be done in the future
- using a range of (formal/informal/technological) controls (at a tactical and operational level) to reduce security risk exposure

##### SETA: security education, training and awareness
- control measure
- to +vely influence security behaviors of employees
- aims and objectives (of the education/training) from security policy and strategy

#### Risk control strategies
- avoidance: prevent vuln from being exploited in first place
  - policy, SETA, technology etc.
- transferrence: transfer risk to other assets/processes/organisations
  - if lacking expertise, hire outside expertise - transfer risk of managing complex systems
- mitigation - reducing impact (from the vuln being exploited)
  - IRP: incident response plan - what to do during the incident
  - DRP: disaster recovery plan - how to recover from fallout
  - BCP: business continuity plan - how to go on
- acceptance: do nothing, accept outcome of asset being compromised
- selecting a risk control strategy
  - depends on level of threat, and value of asset
  - rules of thumb
    - when a vuln exists and can be exploited
    - when attacker cost < potential gain
    - when potential loss is substantial
    - when cost of control < cost of impact
  - t r a d e o f f s

#### Security strategies
- no security
- redundant systems for resiliency
- intrusion detection: detection, recovery (and offense)
- types:
  - prevention: hardest
  - countermeasure: "barriers" to slow down/prevent attacks
  - deterrence
- strategies:
  - surveillance
  - detection and response
  - perimeter defense: strategically selected/placed defense mechanisms
  - compartmentalisation: limiting access to information by people/entities
  - layering: "defense in depth" - using several strategies

#### Threat modelling
- infeasible to protect against everything -> model threats as above
  - too expensive, too much time
- think like an attacker: target is asset
- weakest link

#### Methods
##### Security through obscurity
- limiting exposed information -> limit feasibility of attack
  - any public information is clue for how to attack the system
  - does not mean "make the system more complicated"

### Privacy
- Cohen (2013)
  - legal scholarship (study) conceptualised privacy as a form of protection for the liberal self
  - argues that freedom from surveillance is needed for an informed and reflective citizenship
  - pervasive surveillance and modulation -> mold individual preferences and behavior in ways that compromise innovation
    - it is modulation, not surveillance by itself that poses the threat
- dictionary
  - state of being free from unwanted/undue intrusion/disturbance in one's private life/affairs
  - freedom from damaging publicity, public scrutiny, secret surveillance, or unintended disclosure of one's personal **data or information** - either by gov't, corp or individual

#### Concepts
- digital footprints
  - metadata: "data about data"
  - phones leaking information
- impact of technology on privacy
  - very difficult to be anonymous, or even just privacy (anon is harder than priv)
  - reasons
    - technical
      - IP address - identifier, user agent, browser history, cloud services, data mining/AI/facial recog
    - State as data-taker
    - Snowden and other revelations
- defending your privacy
  - check privacy settings, update them
  - turn off unnecessary settings
  - big 5: patch, strong passwords, encryption (at rest and in transit), MFA, optional: HTTPS everywhere, VPN
- data has value - to you and others
  - balance of rights between citizen and companies - particularly around privacy
  - experiment: dollar vs. data
    - "interesting" characteristics
- value of privacy
  - report: customers want to feel data is secure from unauthorised access and their privacy is kept intact
  - clunky UX for privacy controls put them off
- APPs
  - 1: open and transparent management of personal information
  - 2: anonymity and pseudonymity
  - 3: collection of solicited personal information
  - 4: dealing with unsolicited personal information
  - 5: notification of the collection of personal information
  - 6: use or disclousre of personal information
  - 7: use/disclosure of personal info for direct marketing
  - 8: cross-border disclosure of personal information
  - 9: adoption, use or disclosure of government related identifiers
  - 10: quality of personal information
  - 11: security of personal information
  - 12: access to personal information
  - 13: correction of personal information
  - not prescriptive, more stringent obligations on APP entities with access to sensitive info

#### Differential privacy
##### Spacio-temporal data - even when anonymised and blurred is not enough

##### Main idea
- technique that came out from a research committee: how to get data about a population without exposing data of individuals?
- analogy/idea: coin toss
  - let's say we ask a sensitive question
  - differential privacy adds "noise" to the answer:
    - toss a coin. If you get heads, answer the truth
    - If you get tails, toss a coin and say whatever the coin tells you (Heads -> Yes, Tails -> No)
  - how does this protect someone's privacy?
    - cannot be sure what every single person in the dataset answered thanks to the random noise
      - said person can simply say "I got tails in the 1st coin and just answered whatever the coin told me to" even if they didn't: plausible deniability

##### Formal definition
- If for every 2 neighboring databases D1 and D2, the distributions returned by a mechanism M over D1 and D2 are close, the mechanism is differentially private. (Dwork et al 2006)
  - Explanation
    - The idea is: the mechanism does not return a precise value for every query towards the database. It returns an answer with random noise, usually from a probability distribution - so any answer given from the database is not precise.
    - In addition to that, the mechanism (usually a probability distribution over the data) is constructed in such a way that small changes in the input (say whether a person is missing or not from the dataset) only affect the output very slightly.
      - The idea is: any *one* person in the dataset can claim that he/she never contributed to it/said something else thanks to this random noise (as with the coin analogy above) - this preserves privacy of **individuals**
      - But overall, when it comes to returning the general distribution over the population, this mechanism does not return useless data!
- Mechanism: random function on a database
- Neighboring: 2 databases, R<sup>n x d</sup> differ in only one row

### Cryptography
- sending messages that are secret from everyone but intended recipient(s)
- encryption: "hiding" message for sending, so no one else can understand it
- decryption: "un-hiding"

#### Debates, controversies
- E2E encryption, backdoors
- electronic voting
- privacy and big data

#### Concepts: public key crypto (asymmetric), secret-key crypto (symmetric)
#### Secret-key crypto
- sender and receiver agree on key in advance
- use same key for encrypting/decrypting
- e.g. AES - still in use

#### Public-key crypto
- asymmetric: only one party can read the sent messages
- receiver generates 2 keys:
  - public key *e* for encrypting
  - private key *d* for decrypting
- receiver publicises the public key *e*
  - people encrypt messages sent to the receiver using *e*
- receiver keeps private key *d* secret
  - to decrypt messages
- use
  - exchanging a secret key for secret-key cryptography

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
- 2 parties: Alice and Bob
- Numbers
  - primes: g and p - both Alice and Bob know these
  - Alice picks a secret number a
  - Bob picks a secret number b
- Steps
  - Alice computes A = g<sup>a</sup> mod p; Bob computes B = g<sup>b</sup> mod p
  - Alice sends A to Bob, Bob sends B to Alice
  - Alice calculates S = B<sup>a</sup> mod p, and Bob calculates S = A<sup>b</sup> mod p
    - a and b are "local" secrets, A and B are in "public view" - sent through the network
    - but the same key is still derived - thanks to a property of modulo exponents
      - (g<sup>a</sup> mod p)<sup>b</sup> mod p = g<sup>ab</sup> mod p = (g<sup>b</sup> mod p)<sup>a</sup> mod p

#### Signed DH
- Alice and Bob agree on g and p (large prime) as before
  - George (adversary) learns about g and p too
- Alice generates a secret a and sends A = g<sup>a</sup> mod p to Bob
  - and signs A with her private signing key
- Bob generates a secret b and sends B = g<sup>b</sup> mod p to Alice
- When Bob receives A from Alice, he checks her signature (using her public key) to make sure A is really from her
  - takes care of the possibility of a MiTM attack
- Alice and Bob computes S = g<sup>ab</sup> mod p as before
- Bob sends Alice a message encrypted with their shared key S, using, for example AES
  - AES(message, sharedKey)
