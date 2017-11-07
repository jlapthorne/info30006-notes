# Managing Information Security Risks
## Information asset, threat, vulnerability, risk
### Changing infosec landscape
- global shift: infosec is now a main concern for businesses and nations
    - 2015: US files cyberespionage charges against Chinese military
    - 2013: Snowden reveals US hackers target China, NK and HK
    - 2013: US charged Russian/Ukranian hackers with hacking into computers of major retailers, payment processors and banks, CC no theft

### Threat, vulnerability, risk
- threats
    - cannot be controlled, need to be identified
- vulnerabilities
    - can be treated
    - weaknesses need to be identified
    - proactive measures should be taken to correct vulnerabilities
- risks
    - *can* be mitigated/managed to lower vulnerability or overall impact
    - risk assessment -> identification of critical assets

#### What is a risk?
- risk
    - asset that has a vulnerability
    - that can be exploited by a threat
    - measured in terms of consequence and likelihood

#### Relationship between these terms
- threat agent
    - gives rise to threat
- threat
    - exploits a vulnerability
- a vulnerability
    - leads ot a risk
- risk
    - can damage an asset
- an asset can be exposed to a risk
- risk exposure can be counter-measured by a safeguard
    - which can directly affect a threat agent

## Security threats and risks today
- drones being weaponised
- encryption clash between govts and tech companies
- election hacking - Russia hacking US election
- 2019
    - disruption: over-reliance on IoT
    - internet outages create conflicts globally -> nation chaos
    - ransomware: HBO hack - Game of Thrones stolen
    - insiders giving up crown jewels
        - employees vulnerable to blackmail -> threat of violence towards civilians
    - integrity of information
        - automated misinformation (fake news, etc) gaining credibility
        - falsified information a compromise (e.g. counterintelligence or data distortion)

## Risk management
### InfoSec risk management
- process of identifying and controlling risks (for an organisation)
- 3 steps
    - identification
        - identify current infosec situation
        - establish the context and identify (and figure out the value of) assets
    - assessment
        - determine impact and likelihood
    - control
        - select control strategy; implement
        - apply controls to reduce risks (to data and information systems)
        - maintenance and review
- variants on terminology
    - risk management and its phases
        - risk analysis
        - risk assessment
        - risk evaluation
        - risk estimation

#### Risk assessment
- evaluating the relative risk (for a vulnerability)
    - give a rating/score for each information asset (can be qualitatify - numerical, or quantitative - CRITICAL, HIGH, MEDIUM, LOW, etc.)
- impact of an attack
    - measured in terms of money, productivity cost (in regaining/reproducing asset), penalties (e.g. for breaching confidentiality)
- likelihood of an attack
    - prob of threat, considering the value and vulnerability of the asset
    - sources for calculating likelihood:
        - past records, experience, simulations, experimentation, specialist/expert opinion/judgments

#### Risk controls
- for each threat, create a list of ideas of what controls to use
- examples
    - formal: risk management, policy, etc.
    - informal: SETA (security education, training and awareness)
    - technical: firewalls, VPNs, access control, etc.
- access control?
    - allowing a user into a trusted area (of an organisation)
    - can be mandatory, discretionary, or custom (depending on situation)
        - mandatory: users and data owners have limited control over access to information
            - MAC: mandatory access controls
        - discretionary: impleted at discretion/option of the data user
            - DAC: discretionary access controls
        - other types:
            - central authority @ organisation for managing access controls
            - based on role (role-based)
            - based on tasks (task-based)
- risk control strategies
    - avoidance: prevent by applying safeguards
        - try to prevent the vulnerability from being exploited
        - how?
            - counter threats; remove asset vulnerabilities; limit asset access; adding protective safeguards
        - common methods
            - applying policy
            - training and education
            - applying technology
    - transferrence: transfer the risk
        - try to shift the risk to other assets/processes/organisations
        - if lacking, outsource (hire specialists in security management and administration - individuals/firms)
        - usually for complex systems
    - mitigation: reduce the impact of the risk
        - includes 3 types of plans:
            - incident response plan (IRP): actions to take during the incident
            - disaster recovery plan (DRP): steps to recover from incident
            - business continuity plan (BCP): how to continue doing business if a catastrophic event occurs
    - acceptance: understand the consequences and accept the risk
        - doing nothing; accept the consequences if the asset gets exploited
        - only valid if the costs outweigh the rewards - asset not worth protecting
            - “only when the particular function/service/information/asset does not justify cost of protection”
        - risk appetite: extent to which the organisation is willing to accept the risk as a trade-off to the expense of applying controls

### Selecting a risk control strategy
- level of threat and value of asset - major role
- rules of thumb on strategy selection
    - when a vulnerability exists and can be exploited
    - when attacker’s cost is less than the potential gain
    - when the potential loss is substantial
    - when cost of control < cost of impact
- balance between risks vs. controls

## Concluding remarks, workshop
- risk identification
    - risk management strategy enables ID, classification & prioritzation of organisation’s information assets
    - residual risk: risk that remains to the information asset even after the existing control is applied
        - residual - leftover
- risk assessment
    - evaluate consequence and likelihood
    - quantitative or qualitative methods
- risk control: 4 strategies
    - avoidance (applying strategies)
    - transferrence (transferring risk)
    - mitigation (reduce risk)
    - acceptance (understand consequences and accept the risk)
   