# Questions - preparation exam

## Relationship between information security, privacy and cryptography
- information security: protecting assets against unwanted access/disclosure/modification/destruction/...
- privacy
  - disclosing data according to a set of rules
  - safeguarding personal data and protecting a personal image
  - freedom from surveillance, or having personal data disclosed w/o authorisation
  - Cohen:
    - freedom from surveillance needed for an informed and reflective citizenship
    - surveillance (and modulation) stifle innovation
- cryptography: the art of writing and decoding codes
  - in this context, sending messages that are secret from everyone but the intended recipient(s)
  - encryption: "hiding" the data, such that only the recipient(s) can understand it
  - decryption: "unhiding" the data, recovering the original message from the encrypted data so the recipient can understand data
  - concepts: public-key crypto, secret key crypto, key exchange
- security affords privacy, and privacy is made possible through cryptography and other technologies.

## Why information security and privacy is important
- potential for damages/impacts due to a threat exploiting a vulnerability
  - marring the image of a person/organisation
  - monetary loss - e.g. identity fraud, losing a trade secret that gives a competitive advantage, etc.
- individuals:
  - privacy is "needed for an informed and reflective citizenship"
  - privacy is about keeping private information secret and maintaining a personal image. Without InfoSec and privacy, adversaries can use personal information to cause damage, from things as innocuous as targeted advertising to identity theft, behavior manipulation, silencing through mass surveillance, etc.
- economic:
  - surveillance (and modulation) stifles innovation
- organisations:
  - possibility for monetary (and productivity loss) from having an information asset be compromised

## What are we trying to protect? How?
- we are protecting information assets in Information Security and Privacy
  - data/device/component that supports information-related activities

### How
#### Security measures
- what are we protecting?
  - value of the asset, and
  - cost of replacing the asset - not limited to $, but productivity cost, etc.
- threat modelling - know who are the threats
  - threats: possible danger that exploits a vulnerability to breach security
  - motivations, number of threats, resources of threats, likelihood of threat
- security requirements required:
  - CIA?
  - access control?
  - privacy?
- which strategies to implement?
  - strategy: set of actions to be done in the future
    - uses formal/informal/technological controls
    - to reduce security risk exposure
  - types of strategies
    - prevention (hardest one)
    - countermeasure
    - deterrence
    - surveillance
    - detection and response
    - perimeter defense
    - compartmentalisation
    - layering/"defense-in-depth"
  - strategies (will not be asked in depth):
    - no security
    - redundant systems
    - detection, recovery (and offense)

## Threats? How are they classified?
- human error
- IP compromise
- espionage/trespass
- theft
- HW/SW failure
- vandalism
- software attacks (DDoS, viruses)
- information extortion
- QoS from providers
- technological obsolescence

### Classification, with the common (abstract) adversary framework
- action: passive/active
- sophistication
- access: internal/external

## Risks - what are they, how to manage risks?
### Risk
- **potential for loss**, damage, or destruction of an asset as a result of a threat exploiting a vulnerability

### Risk management
- identifying
  - what is the asset?
  - what is the context?
- assessment/analysis
  - likelihood
  - impact
  - assign a "risk score" - quantitative (number) or qualitative (LOW, MED, HIGH, ...)
- control
  - select which strategies to use
    - formal: risk management, policy, etc.
    - informal: SETA
    - technical: firewalls, AV, access control, etc.
      - access control: MAC (mandatory), DAC (discretionary), role-based, task-based, central authority
  - risk control strategies
    - avoidance
    - transferrance
    - mitigation: IRP, DRP, BCP
      - IRP: incident response plan - what to do during the incident
      - DRP: disaster recovery plan - how to recover from the fallout
      - BCP: business continuity plan
    - acceptance: do nothing, accept risk
  - selection?
    - depends on level of threat and the value of the asset
    - when?
      - cost of attack < potential gain for attacker
      - when a vulnerability exists and can be exploited
      - potential for substantial loss
      - cost of control < cost of impact
- review/maintenance

### Why does risk play such a big role in the InfoSec discussion?
- InfoSec: protecting information assets from threats exploiting vulnerabilities
- risk: **potential for loss**, damage, or destruction of an asset as a result of a threat exploiting a vulnerability
- natural extension of the discussion - risk analysis and management techniques are used in the selection of security measures; techniques (policies and strategies from InfoSec) are used to control the risks (of threats exploiting vulnerabilities)
- reword?
  - security measures/safeguards can countermeasure risk exposure

## What are organisations doing wrong? Right? Strategies they can use, and how good are they?
- organisations often make it a tradeoff between convenience and security/privacy
- privacy/security as an afterthought
- inadequate safeguards
  - Precdent Communications, VTech (toy company - online service breach)
  - IoT
  - Equifax
    - NOT PATCHING
- not following APPs or other similar principles/best practices
  - Precedent, Blood Service
- hard data (Hasham S et al, 2016)
  - customers do not view companies as adequately protecting their privacy
    - 84% of surveyed households had at least 1 privacy concern
    - 19% of Internet-using households impacted by online security breach/identity theft/similar activity in the 12 months before the July 2015 survey
    - 22% of Internet-using households that used a mobile data plan to go online outside the home experienced an online security breach
  - what they can do better
    - better UX for privacy controls
      - simplifying process while not compromising privacy
      - example: Signal, WhatsApp
    - better communication on how data is disclosed, used
      - households having conern = communication is not good enough

## Contemporary topics
### Knowledge leakage (vs. data/information leakage)
- KL: accidental or deliberate loss or transfer of knowledge
- how does it differ from data/information leakage?
  - data: raw facts/numbers
  - information: processed data
  - knowledge: internalised information or has added value
    - information with meaning
  - vs. data/information leakage
    - data/information leakage: technical measures to prevent data/information leakage, while with knowledge leakage, need human-oriented measures
    - why?
      - KL happens when a knowledgable employee takes knowledge to another party, either unintentionally or intentionally
        - e.g. leaving company to competitor, being eavesdropped when employee is discussing sensitive knowledge
          - real-world interactions, as opposed to digitial interactions
        - a different set of preventive (and reactionary) measures is required: Legal (NDA, patents, contracts), keeping knowledge tacit, culture, compartmentalisation, disruption, misinformation, policies
    - focus is mainly on Confidentiality, where with the 2 others - CIA

### Workshop cases - what do they have in common? what are the differences?
- mass surveillance - value of privacy, government overreach (and abuse)
- Blood Service breach
  - outsource with caution
  - following best practices
  - value of privacy - cannot take back leaked personal info
- cryptography - keys under protocol
  - cannot introduce exceptional access w/o introducing unacceptable risks into the system
  - complexity -> greater risks
- encryption and decryption: RSA, DH
- AI (superintelligence)
  - risk analysis
    - analyse the probability/likelihood that it will happen
    - impact: will AIs pose a threat to the human species?
- digital footprints and the privacy paradox?
- de-identification and re-identification of data
- Kapersky ban
- KL
- electronic voting, CIA triad
