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

### Sensitive information
Information protected against unwarranted disclosure (to protect privacy/security of an individual/organisation)

### InfoSec (Week 11 Lecture)
Protecting information systems against misuse and interference from external parties.
"Building systems to remain dependable in the face of malice, error or mischance" - Ross Anderson

### Properties of a secure system
#### CIA triad
- Confidentiality: information is protected from unintended disclosure (secrecy, privacy, access control)
- Integrity: system, data and information are maintained in a correct and consistent condition
- Availability: system, data and information are usable when needed (includes timeliness)
- note: information also implies knowledge

#### Secrecy and confidentiality
- Secrecy: keeping data hidden - e.g. keeping an incriminating secret
- Confidentiality: keep (someone else's) data hidden from unauthorised entities

#### Privacy and anonymity
- Privacy: use/disclose a person's data according to a set of rules - e.g. de-identification of information
- Anonymity: keep identity of a protocol participant secret - e.g. TOR

#### Integrity, authentication
- integrity
  - ensure data is "correct" - unchanged, correct syntax
  - prevent unauthorised or improper changes
- entity auth/id: verify identitiy of another protocol participant
- data auth: ensure that data originates from claimed sender

### "Security through obscurity"
"You can't be attacked if adversaries don't know you exist/what you use/etc."
- attacking a system requires knowledge of how it works
  - info can narrow field of potential exploits
- solution
  - limit exposed information - all public info are clues for hackers
    - "what is the least information needed to get the job done?"
  - obscurity != misdirection
    - misdirection adds complexity (e.g. adding fake servers, fake data)
    - principle: "simple is more secure" violated - additional complexity -> more points of failure

### Basic security analysis
#### Real-world security - principles
- specification/policy: what system is supposed to do
- implementation/mechanism: how it is done
- correctness/assurance: does it work
- human nature: "clever" users?

#### Security analysis
- who/what are we protecting?
  - information assets, and their value
  - understand the architecture of the system
  - ask:
    - what's the operating value? (rate of loss if resource is gone)
    - replacement cost: time, cost?
      - quite high if competitive advantage
- who/what are the adverseries/potential threats?: identifying potential attackers
  - motivations? nation state vs. script kiddie?
  - estimate resources, no of attackers, likelihood of attack
  - recall: risk, vulnerability, threat
  - for exam: concepts, not definitions will be asked - more in line with workshops
  - common (abstract) adversary: a framework to help assess who/how severe threats are
    - action: passive/active?
    - sophistication: script kiddies vs gov't funded?
    - access: external/internal?
      - result of system compromise
- what are the security requirements?
  - enumerate security requirements: CIA, availability, access control, privacy
    - for exam: understsand beyond defiinitions
- what security strategies are effective?
  - list:
    - no security
    - resilience to attack - redundant systems
    - detection, recovery (and offense) - intrusion detection
    - *will not be asked in depth*
  - types
    - prevention
      - block attacks, before they happen
      - passive, may be software (not just H/W)
      - hardest strategy - most expensive
        - think: protecting someone from an assasin
    - countermeasure
      - only barriers - slowing down/preventing attacker from getting to asset
    - deterrence
    - surveillance
    - detection and response
    - perimeter defense
      - old principle: in the Middle Ages, placing castles in very strategic places such that you can easily get in and get out (at the border)
      - having several defense mechanisms
        - where you are
        - moats
        - towers + secret entrances + sub-towers
        - same principle - going through multiple gates
    - compartmentalisation: limiting access to information to persons/other entities
    - layering
      - "defense in depth"
      - combining multiple security controls to protect resources/data

#### Threat modelling
- you *cannot* protect against everything
  - too expensive and takes too much time
- have to model what to protect against

#### Think like an attacker
- target: asset, not defenses
- weakest link
- adapt steps depending on context

### Why?
- possibility of monetary loss?
- reputation/image
- context of individuals: personal information, freedom from having personal information disclosed/surveillanced

## Assets
- any data, device, or other component of the environment that supports information-related activities
- hardware, software, confidential information, people
- what we are trying to protect

### Knowledge leakage
- KIF: knowledge intensive firm (Anand, Gardner & Morris 2007, Teece 2003, Winch and Schneider 1993)
  - characterised by an analytical knowledge base
  - strong reliance on knowledge as a basis for competitive advantage
  - differentiator: produce qualified products and/or services; even generate new and unique knowledge

#### Motivation
- mobile devices increase organisational risks
- **money**: each incident costs US$2.8m on average (Aus)
  - investigation and assessment - 2nd highest worldwide (US$1.2m)
- insider threat: employees accidentally or intentionally leak knowledge
  - culture, people
  - weakest link

#### Data, information and knowledge
- can be thought of as a cycle
- data -> information
  - processing, analysing
- information -> knowledge
  - internalised: absorbed by mind
- knowledge -> information
  - externalised: verbalised/illustrated
- information -> data
  - captured and stored
- tacit knowledge: knowledge that is not easily expressed
- explicit knowledge: formal and systematic - easily communicated and shared, documented
- cycle
  - explicit knowledge -> tacit knowledge: internalisation
  - internalisation -> socialisation
  - tacit -> explicit: externalisation
  - externalisation -> combination
- cycle (2) (Alavi and Leidner 2001)
  - knowledge -> information: when it has been codified (made explicit) into artefacts
  - possible to infer knowledge from information
- knowledge (Davenport and Prusak 1998):
  - fluid mix of framed experience, values, contextual **information** and expert insight that provides a framework for evaluating and incorporating new experiences and information
  - originates, is applied in the minds of "knowers"
  - organisations - embedded not only in docs/repos but also in routines/processes/practices/norms

##### Different perspectives on knowledge
- Fahey and Prusak: data, information and knowledge compared
  - data: raw facts and no
  - information: processed data
  - knowledge: personalised information, value-added information
- state of mind (Schubert et al, 1998)
  - state of knowing and understanding
- object (Carlson et al 1996, McQueen 1998, Zack 1998)
  - object to be stored and manipulated
    - object: knowledge stocks
  - IT: provides access to knowledge *sources*, not knowledge itself
- process (McQueen 1998, Zack 1998)
  - process of applying expertise (flows, creating, sharing and distribution)
  - process of knowing and acting
- capability (Carlson et al 1996, Watson 1999)
  - potential to influence action
  - building core competencies and understanding strategic know-how necessary in decision making

#### Knowledge Leakage
- accidental or deliberate loss or unauthorised transfer of knowledge
  - knowledge intended to stay within an organisation's boundary that may weaken the competitiveness and industrial position of the organisation
  - (Annaisgngh 2007, Frishammar et al 2010)
- confidentiality from CIA triad
- examples: IP, trade secrets, business strats, product designs

##### Compared
- data and info leakage: can take technical approach; CIA requirements
  - data prevention loss, encryption, firewall, antivirus
- knowledge leakage: human approach - as knowledge is embedded in people
  - knowledge protection, legal, tacit knowledge instead of explicit, compartmentalisation, disruption, misinformation, Knowledge Protection Policies
  - **Confidentiality**, Knowledge Protection, Knowledge Retention, security risk exposure (perceived)

##### KLR (KL risk)
- extent to which an org is threatened by a KL event
  - function of impact and likelihood
  - KLR = KL impact x KL likelihood

#### Strategies
See: above from `#### Security analysis`

#### Findings
- human factor: how to prevent KL
- personal context
  - develop trust
  - use deterrents (punishments/sanctions)
  - weed out high risk people/positions
  - user behavior analytics
  - gamification (simulation) - see what could go wrong
  - SETA
  - decoy campaigns
  - quote from CEO: if people are weakest link, education is the strongest link -> education program
- social context
  - mobile security culture - habits
  - deterrants
  - communities/portal (tips, reminderse, HR mood boost)
  - peer mentoring - encourage asking questions
- organisational context
  - mobile risk management framework - IDing valuable knowledge assets - who knows what
  - standards, policies, procedures (for mobile workers)
  - legal
  - embed security into knowledge processes to protect when using mobile devices
  - knowledge governance: HRM dealing with tacit knowledge
  - roles for Knowledge Protection
  - protecting knowledge flows
  - embed extra complexity into process
  - constant monitoring to *mobile* workers dealing w/ sensitive knowledge
  - knowledge management strat
  - resilience capability - handle impacts
  - knowledge reconfiguration: combine knowledge assets to create new knowledge
  - multi-disciplinary integration
- environment
  - cooperate between orgs
  - factors to deter knowledge transfer
  - market analysis
  - analyse competitors/adversaries
  - counter-intelligence
  - policies for off-site work
  - conversation and behaviors outside company
- devices
  - MDM
  - encryption
  - geolocks
  - sandboxing
  - remote admin
- technical
  - enterprise mobility strategy
  - mobile device usage analytics
  - knowledge compartmentalisation
  - classification - tagging/labelling
  - auth, control, tracking of documents


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

### What is privacy?
Cohen (2013) - "What Privacy Is For"
- "legal scholarship has conceptualised privacy as a form of protection for the liberal self"
- invasion of privacy can be episodic or systematic
- argues that freedom from surveillance is needed for an informed and reflective citizenship
- privacy has an economic role in innovation: it shelters the processes of play and experimentation from which innovation emerges
- Regimes of pervasively distributed surveillance and modulation seek to mold individual preferences and behavior in ways that reduce the serendipity and the freedom to tinker on which innovation thrives.
  - Modulation: exerting a modifying/controlling influence on something
  - it is modulation, not privacy by itself that poses the greater threat to innovative practice.

Dictionary.com
- state of being free from unwanted or undue intrusion or disturbance in one's private life or affairs
- freedom from damaging publicity, public scrutiny, secret surveillance, or unauthorized disclosure of one's personal data or information, as by a government, corporation or individual


### Important concepts
- you're leaving digital footprints: not just what you post online, but metadata, fingerprinting, etc.
  - work habits, cursor movement, browser and OS info, etc.
  - metadata: location data
  - not just your phone/tablet/device belieing your privacy:
    - other people tagging/mentioning you
    - geo-tags - if you happen to be inside a geo-tagged photo
    - business and services: transactions, how you use their services (think rewards programs), CC (credit card) data -> business strategies from behavior from user accounts
- example: "I know where your cat lives"
  - metadata of cat pics: latitude an dlongitude coordinates embedded in their metadata

### Footprints: phones
- turning off phones might not be enough
- NSA's TAO (Tailored Access Operations) unit
  - exploits 0-days
  - efficient, discrete attacks
  - started when \<2% of world had access to internet
  - DROPOUTJEEP: iPhone software implant
    - push/pull files, contacts, voicemails, geolocation, hot mic, camera, cell tower, C&C (command and control), data exfiltration
    - covert, encrypted comms
- US Gov't spied on AP
- Paul Farrell: journalist
  - 200 pages of information about him from a FoI (freedom of information) request
  - metadata and records, to find his source
- NSA collected almost 200m SMSes a day across the globe
  - extract data: location, contact networks, CC details

### Impact of technology on privacy
- difficult to be anonymous, or have privacy anymore
  - technical:
    - IP address transmitted
    - user agent
    - browser history
    - cloud services don't delete data: "marked for deletion"
    - case study: Paula Broadwell and Gen Petraeus
      - discovered by capture of Broadwell's IP address
      - convicted for access to classified information - was not imprisoned
      - Paula hid her identity trying to be anonymous, sent threating emails to a Florida socialite
      - former exec of FBI:
        - her IP address was captured, they were using email drafts as an onlien dropbox to conceal email traffic -> account activity still logged
    - data mining, facial recognition tech, activity modelling, fingerprinting
      - the way you write
        - word pairings, character ingrams,
- the State as data-taker
  - deliberate mechanisms to reduce privacy
  - phones:
- Snowden, other revelations

### How to defend end-user privacy - good security practices; and how privacy and security are intertwined
- periodically check privacy settings and update them
- turn off settings that share information unnecessary for use/service
- big five:
  - patch
  - strong passwords
  - encrypt data at rest, in transit
  - mfa and OTP
  - optional: HTTPS everywhere, VPN

### Data is valuable - to you and others
- in every community, there is a necessary balance between the rights of the citizen and companies, particularly around privacy
  - is ours out of balance?
- dollar vs. data - experiment
  - how much is your personal information worth?
  - 3 characteristics that increase the value of your data?
    - ethnicity, job, marriage status, etc.
    - http://www.ft.com/cms/s/2/927ca86e-d29b-11e2-88ed-00144feab7de.html
- private info
  - how would it be valuable to others? Who do you think could use that information?
    - institutions? companies? the government? your friends and family? cybercriminals?

### Value of privacy, as provided by security on society, and particularly commerce
- hard data about what happens to customers and commerce relating to security/privacy

#### Customers' privacy and security - issues for business
- customers want to feel their data is secure from unauthorised access and their privacy is kept intact
- ways of ensuring privacy through better security can be heavy-handed and clunky for average user
  - puts them off -> leads them to choose less secure options -> risking their privacy
- 2 issues
  - integrity of the company "harvesting" the data and using it, vs.
  - integrity/protection of that data from others

#### Is "secure" enough for privacy?
- even if the data is kept appropriately?'
- increasing no of large-scale data breaches: (Hasham S. et al 2016)
  - higher security burden on clients
  - diminsed UX for the customer
  - on average, clients need to remember >14 passwords
  - despite this, customer perception of security has gone worse
  - issues around digital security and privacy "eroding consumer trust online" (Goldberg 2016)
    - 45% of households reported that concerns about online security/privacy stopped them from:
      - financial transactions, or buying goods/services, or posting on social networks, or expressing opinions on controversial or political issues via the internet?

#### New realities for consumer behavior online (Goldberg 2016)
- 19% of Internet-using households impacted by online security breach/identity theft/similar activity in the 12 months before the July 2015 survey
- 22% of Internet-using households that used a mobile data plan to go online outside the home experienced an online security breach
- 84% of households had at least 1 specific privacy or concern
  - 40% had at least 2

#### Case study: Equifax breach
- breach that exposed sensitive data for 143m US consumers
  - May 13 - July 30
- did not disclose breach until Sept 7
- critical vuln in Apache Struts Webapp framework
  - known bug, trivial to exploit
  - PATCH!
- financial impact:
  - stock tanked from $140 to $94 in 2 weeks

#### Trade-offs between privacy/security and convenience: what customers say (Hasham, S et al. 2016)
- 30% prioritize ease and convenience over security
- want "basic level" operating behind the scenes, but say "having access to account info w/o the need to enter pswd attractive"
- reject notion of a "OTP sent to them for every login"

#### How to keep privacy through good security with high adoption among users (Hasham, S et al. 2016)
- device/no recognition, omnichannel auth
  - (customers don't want to be treated like strangers because they're on a different device)
- remaining 20% prefer a verification phone call
- log-in credentials should be the same across all channels
  - allow custs to logn in one channel to use another, eliminating duplicate auths
- better visual UX matters
  - inconsistent design, poor error messaging, clunky comms, site slowness or unavailability make it less appealing to the end user to accept security that will improve their privacy

### APP - overview
#### Privacy policy
A company's privacy policy describes how it gathers, uses, discloses and manages a customer's information.

#### Legal background
- Australian Information Commissioner Act 2010 (AIC Act) establishes the Office of the Australian Information Commissioner (OAIC), with 3 primary functions:
  - privacy functions, conferred by Privacy Act 1988 (Privacy Act) and other laws
  - freedom of information functions - oversight of the operation of the Freedom of Information Act 1982 (FoI Act), reviewing decisions made by agencies and ministers under that Act
  - government information policy functions, conferred on the AIC under the AIC 2010 (AIC Act)
- APPs, in schedule 1 of the Privacy Act, outline how most Australian and Norfolk Island Government agencies, all private sector and not-for-profit organisations with an annual turnover of more than $3 million, all private health service providers and some small businesses (collectively called 'APP entities') must handle, use and manage personal information
- APPs are not prescriptive: each APP entity needs to ocnisder how the principles apply to its own situation

#### APPs
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

#### Not prescriptive
- separate APPs for situations in APP 7, 8 and 9
- more stringent obligations on APP entities who handle "sensitive information"
  - health, racial/ethnic origin, political opinions, membership of a political/professional/trade association/union
  - religious beliefs/affiliations, philosophical beliefs, sexual orientation/practices, criminal record, biometric info, biometric templates

#### USB killer

### Privacy Audit - part 2
#### Importance of encryption in email to privacy
Snowden: "The security of people's communication is very important to me" (first approach to Greenwald)
Urged Greenwald to start using PGP mail

### Bonus: extra privacy and security steps
- tweak IM settings - WhatsApp: remove cloud backups (unencrypted), security code verification, security notifications
- paper printouts are not safer!
  - secret information: yellow dots which can be seen under blue light or with digital manipulation
  - encoded in documents when they were printed
  - http://www.bbc.com/future/story/20170607-why-printers-add-secret-tracking-dots
- turn off Bluetooth when not using it
- Tor: browsing with more privacy
- Ricochet - P2P IM via Tor

### Differential privacy
#### Privacy in the modern world
- for each phone, you have a long trace of everything that it does
  - spacio-temporal points (space and time)
  - time can be very precise, location is rather broad (cell tower/WiFi triangulation)
    - triangulation: only a triangle of cell towers needed to get a good fix of your location
  - need some verification between data points to distinguish one person from another if that's all you have to track them
    - even over large areas, trajectory of the places you went can still be unique
    - (think: specific patterns, going home to specific places)
- let's say we reduce the resolution of the data
  - blur the time, blur the space
  - still have a lot of uniqueness
- how not to find yourself, an example
  - 3m patients
  - 17310 women share year of birth
  - had 2 children in 2006 and 2011
    - 59 possible matches, 25 in VIC
  - exact birthdates +/- 14 days
    - luckily there were no dates
  - takeaway: it's really easy to pick someone out - easy to reidentify them from an "anonymised" dataset
    - and possible when the dataset is updated

#### Differential privacy: main idea
- technique that came out from a research committee: how to get data about a population without exposing data of individuals?
- analogy/idea: coin toss
  - let's say we ask a sensitive question
  - differential privacy adds "noise" to the answer:
    - toss a coin. If you get heads, answer the truth
    - If you get tails, toss a coin and say whatever the coin tells you (Heads -> Yes, Tails -> No)
  - how does this protect someone's privacy?
    - cannot be sure what every single person in the dataset answered thanks to the random noise
      - said person can simply say "I got tails in the 1st coin and just answered whatever the coin told me to" even if they didn't: plausible deniability

#### Differential privacy: formal definition
- If for every 2 neighboring databases D1 and D2, the distributions returned by a mechanism M over D1 and D2 are close, the mechanism is differentially private. (Dwork et al 2006)
  - Explanation
    - The idea is: the mechanism does not return a precise value for every query towards the database. It returns an answer with random noise, usually from a probability distribution - so any answer given from the database is not precise.
    - In addition to that, the mechanism (usually a probability distribution over the data) is constructed in such a way that small changes in the input (say whether a person is missing or not from the dataset) only affect the output very slightly.
      - The idea is: any *one* person in the dataset can claim that he/she never contributed to it/said something else thanks to this random noise (as with the coin analogy above) - this preserves privacy of **individuals**
      - But overall, when it comes to returning the general distribution over the population, this mechanism does not return useless data!
- Mechanism: random function on a database
- Neighboring: 2 databases, R<sup>n x d</sup> differ in only one row

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

### Signal - X3DH, double ratchet algorithm
- [Signal - Advanced Ratcheting](https://signal.org/blog/advanced-ratcheting/)
- [Signal - X3DH](https://signal.org/docs/specifications/x3dh/)

#### [Reddit thread on X3DH](https://www.reddit.com/r/netsec/comments/5bg3f4/x3dh_extended_triple_diffiehellman_key_exchange/)
- X3DH uses 3 Diffie-Hellman key agreement phases
- provides confidentiality, integrity and authenticity + plausible deniability and forward secrecy
- Signal protocol is asynchronous: communication can begin and occur even when one of the users is not connected to the Signal network (complete later)

```
Signal uses 3DH + hash ratcheting + optional rekeying with 3DH.
As a recipient, you have a list of signed asymmetric ephemeral keys stored on your behalf by your server.
The person contacting you requests an ephemeral public key for you, and verifies the signature. He computes key exchanges between [his permanent private key + your ephemeral public key], [his ephemeral private key + your ephemeral public key] and [his ephemeral private key + your permanent public key].
The three outputs are mixed to generate a seed. This seed is iterated (deleting past seed values) in a PFS manner using the hash ratchet for every message.
Rekeying mixes the 3DH key exchange outputs with the existing iterated seed value.
Both people know they're talking to the right person because they got the same output from all three key exchanges and thus both knows the respective private keys from the long term keypairs and ephemeral keys.
And yet a falsified conversation is indistinguishable from a real one to somebody without ALL the keys!
```

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
