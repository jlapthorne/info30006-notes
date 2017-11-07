# InfoSec workshops

## 'Donate Blood' data breach
- 5 Sep: data file (550k prospective blood donors, used website from 2010-2015) mistakenly backed up to publicly accessible server by Precedent employee working on the site (UAT - user acceptance testing environment)
  - identifying particulars, contact details, appointment preferences, answers to eligibility questions (meds, sexual behaviour, etc.)
- 25 Oct: anonymous individual scanning the internet for security individuals located, accessed and made a backup of the 'data file'
- 26 Oct: Blood Service aware of breach; took steps in response
- Precedent Communications: digital agency managing the DonateBlood website

### Mitigating/avoiding data breach: Blood Service
- measures taken
  - BS staff create donor's profile in NBMS - information remained on the backend of the website as a backup - *vulnerability*
  - data retention policy did not extend to the information stored on the Blood Service website
  - no process for reviewing th einformation maintained on th ebackend of the website and how long it hsould be held
  - overall: risk *transference* to Precendent
- measures that should have been taken
  - destroy all historical data and personal information periodically
  - develop and implement Third Party Management Policy and 3rd Party SOP (Standard Operating Procedure)
  - update template contractual terms for the acquisition of products and services
  - amend procurement process - so a completed PIA (private internet access) is gotten prior to any significant contract negotiation
  - accelerate and expand a review of information and technology services; external consultants
  - overall: risk limitation - limiting the exposure to risk

### Risks for outsourcing?
- risk transferrence: taking fewer risks
  - seek help from specialists/"experts" in InfoSec
  - transfer risk associated with storign donor information to Precedent, absolving the Blood Service of some personal liability
- but can increase risks:
  - confidentiality of personal data was made conditional on Precedent's InfoSec standards (which failed)
  - BS retained effective control of the personal information - still required to take reasonable steps against misuse/interference/loss/unauthorised access/modification/disclosure

### Measures to mitigate/avoid: Precedent's side
- practices at the time:
  - no internal practices/procedures to mitigate against any risks of using **live data**
  - not disabling directory browsing on the affected server
  - not according in accordance to Privacy Act
- should have been taken - risk limitation:
  - put up safeguards
  - policies and procedures should cover preventive and proactive measures to limit impact of human error (e.g. monitoring systems, QA)
  - limit personal information collected by Donate Blood or via the website to *reduce* the risk of storing personal info
  - use dummy data instead of live data for testing purposes

### Findings from the Australian Information Commissioner
- Blood Service
  - protections strong in general, but
  - some issues w/ protection of information held by 3rd party providers
  - breached APP 11.1 (taking reasonable steps to protect information) and 11.2 (destroy/deidentify unused info)
  - acted swiftly and appropriately in response with a commitment to review security measures - then implemented
- Precedent
  - failed to adequately mitigate against the forseeable risk of human error resulting in a data breach
  - breached APP 6 (only use/disclose information for the primary purpose of collection) and
  - 11.1 Took extensive remedial action, acting in a timely, open manner

### Human errors that could cause incidents
- using weak passwords
- low security awareness
- careless handling of data

#### Protecting from human errors
- prevention
  - checklists
    - backup log
  - safety procedures
    - dummy data on testing platform
    - disable directory browsing
  - training and raising awareness
- mitigation
  - audit - of files
  - breach detection
  - system monitoring

### Outsourcing vs. not outsourcing?
- depends on:
  - sensitivity of the assets - if sensitive, better not
  - depends on the type of company: if multinantional, not advised to outsource for governance-related security functions
    - Vladmir Jirasek (leads UK chapter of CSA): "can be argued that entire security stack can be outsourced, except governance, risk and compliance"
    - things like application security, identity or access management and virtualisation should not be outsourced
    - firewall, netsec, vuln scanning, anti-malware, host security, DB firewall management safe candidates for outsourcing
  - if outsourcing can add value to the business
    - if reduce cost; or make customers more confident in product
  - reputation
    - organisations looking to outsource specific security capabilities must be confident they are aware of and can manage the potential fallout if their supplier fails;
    - also work closely w/ suppliers to minimise risk of failure
- even if outsourced, the client organisation will still suffer the brunt of the fallout

### Conclusions
- improvements following the breach:
  - improved practices
  - sought external audits
- site to address concerns
- Blood Service and Precedent both not held accountable for breach
  - Commissioner praised both for their response and considered an "enforceable undertaking" to be an appropriate conclusion
  - taking steps to mitigate risks in the future does not make up for previous failings, which were all made very clear in the report
  - class-action lawsuits

## Keys under doormats
- debate: on exceptional access (govts have special access to encrypted systems)

### Exceptional access
- "situation that was nto included within the intended bounds of the original transaction" - 1996 National Academies CRISIS report
  - access to a system/device which is normally not allowed/possible
- govts want this access (so far vague)

### Lessons from 1997
- authors came together to analyse security risk associated w/ key escrow systems
  - key escrow: copy of decryption key is stored with a trusted 3rd party, allowing access to systems or devices under exceptional cirumstances
  - unsurprisingly:
    - places enormous costs on end-users
    - difficult and expensive to implement
    - many systems had major flaws
  - plan was scratched

### What has changed?
- 18 years later, authors reconvened - arguments are the same (still a bad idea)
  - scale of assets at risk has actually grown immensely
  - greater no of vulns - systems now more complex
  - previous attempts were expensive -> failure
  - solutions will still be complicated, stifles innovation

### Scenarios
#### Access to encrypted messaging systems
- can a secure messaging system exist that allows exceptional access?
  - normally, messages are encrypted with a symmetric key which is itself encrypted with the recipient's public key
  - in order to comply w/ exceptional access, encrypt the symmetric key again with an escrow agent (the party that holds the keys)'s public key -> special escrow key, can be used to decrypt original message (if decrypted by escrow agent)
  - encrypted message sent along with the 2 copies of the symmetric key
- problems
  - what happens when the recipient's or escrow service's private key gets breached?
    - **all** data secured using the corresponding public key is compromised
    - to counteract this, companies are moving to *forward secrecy*
      - forward secrecy: if a breach occurs in the future, messages from the past maintain their secrecy - "carry forward"
  - giving a 3rd party access to encryption key allows them to read and forge traffic to the recipient: violates confidentiality and authentication principles
  - how do we determine who controls/has access to escrow keys?

#### Access to encrypted devices
- e.g. law enforcement - to unlock device at a crime scene
- options
  - NOT the passphrase: too time-consuming, especially what if the user changes the password?
  - use a random key - encrypted by the user-supplied key
    - Key-Encrypting Key
  - step further: use the user's passphrase along with a device-specific unique identifier to encrypt the random key for the KEK
- how to enable exceptional access?
  - use another key
  - take the random key (that unlocks the device), encrypt it with the additional key(s) for the additional parties who need access
  - who owns it: manufacturers? law enforcement agencies?
    - manufacturer keys: network protocol to decrypt the device key
      - problem: auth - are you who you say you are? (are you actually law enforcement?)
      - need an auth system for the thousands of law-enforcement agencies
    - law enforcement
      - equally difficult
      - auth
      - alternative: ship devices back to vendor
        - store keys for a long time -> security risk shifts to manufacturers
- 3rd options?
  - per-country keys?
  - but travellers also bring devices
  - installation on the border is problematic

#### Summary of risks
- trade-off: cannot guarantee access w/o serious compromises in terms of risk
- guaranteeing access is complex, introduces more flaws into s/w
- can be used for surveillance
- stifling innovation -> puts econ. growth at risk

#### Why not?
- law enforcement agencies have not been very specific
  - we can only assume they want general surveillance capabilities
  - this access needs to be controlled and monitored (see: lecture on privacy, anonymity)
  - rule of law?
- how?
  - access unencrypted central databases to obtain content
  - what if there is no central database? -> have to intercept comms as they occur
  - if encrypted: to gain access (as law enforcement), session keys need to be encrypted using public keys from police forces from different countries, or some trusted 3rd party (escrow)
    - issues
      - restricts important security features (e.g. forward secrecy)
      - access could be abused by others who get access to the key escrow
      - difficult to define and enforce on a global scale -> criminals can just use software from a non-enforcing country, geo-spoofing to pretend that you are not from an enforcing country
      - issues arising from several companies refusing to grant exceptional access: do we simply ban them?!
- access to comms data
  - back in the day: unencrypted phone records
  - now: some encrypted (email, SMS) - e.g. TLS
  - can still obtain plaintext via court orders
  - UK may soon make it compulsory for companies to honor requests
  - issues
    - aggresive enforcement
    - cost on innovation - technical burden!
- access to data at rest
  - escrow keys
    - already in used in companies
  - but not scalable
    - issue: most data at rest is on personal devices - difficult to obtain
    - options:
      - catch them with the device open and accessible (see: Silk Road)
      - obtain warrants to install malware

#### Security principles at stake
- considerations for exceptional access
  - scope of applicability of the exceptional access requirement
  - limitations on the mandate
  - freedom of the user that remain protected
  - desigining systems; planning administrative procedures
- finding a balance
  - sticking to public policy, and the associated security risks, costs and teechnical feasability

#### Conclusions
- paper only states that introducing exceptional access comes w/ unacceptable security risks
