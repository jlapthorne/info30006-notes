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
- encryption: turning data into "gibberish"; decryption: turning the "gibberish" back into data
- enables secure information transactions through encryption and decryption

### Intro

### RSA

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
