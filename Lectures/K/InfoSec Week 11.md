# Information Security

## Next week
- exams - trial exams
- ask questions to Sulette and Vanessa - not over content
- questions for you to think about

## Information security
- protecting information systems against misuse and interference from external parties
- knowledge vs. information
    - 10-20 years ago, knowledge management -> information management
    - we used to talk about data, now we have knowledge (design/recipe/etc.)
        - incidents of data/knowledge leaked to competitors, often
        - cost a lot more now thanks to a global society

### Aside
- Jebb - connect to him on LinkedIn?

### Properties of a secure system
- confidentiality: information* is protected from unintended disclosure (secrecy, privacy, access control)
- integrity: system, data and information* are maintained in a correct and consistent condition
- availability: system, data and information* are usable when needed
- *we are increasingly discussing knowledge along with information (knowledge leakage talk today)
    - not necessarily in books/article/web, but protecting data => protecting knowledge

### Definitions
- secrecy: keep data hidden
- confidentiality: keep (someone else's) data hidden from unauthorised entities
- privacy: use/disclose a person's data according to a set of rules
    - e.g. to protect Alice's privacy, company XYZ removed her name from data
- anonymity: keep identity of a protocl participant secret (think security audit!)
    - e.g. TOR, surveys
- entity auth/identification: verify identify of another protocol participant
- data authentication: ensure that data originates from claimed sender

## Security through obscurity
- different books -> different frameworks for how to protect information/knowledge
    - collaborate with own/other organisations at some point or another
- think from another perspective:
    - first, make sure you comply with rules/law
    - actively protect data
    - when engaging with other companies - data protection laws
- "you can't be attacked if people don't know you exist"
    - it requires a bit a fair bit of knowledge about the system to do it
        - vulnerabilites of certain software
- classical example: breaking into a safe: harder/easier if?
    - lights on/off?
    - know what kind of make/model?
    - can see the numbers on the safe
- information helps hackers by narrowing field of potential exploits
- solution
    - limit exposed information
    - "what is the least information to get the job done?" (all public information is a clue for hackers)
    - obscurity does NOT mean (intended) "Misdirection"! This also violates the principle of "simple is more secure"
        - honeypots - servers that pretend to be an important server -> organisations learns from hackers: not the intention of this particular saying
        - actually more about keeping things as simple as possible

## Basic security analysis
### Common security threats
- human errors, compromise to IP, espionage, extortion/ransomware, theft, SW/HW attacks, forces of nature, ...

### Real world security
- principles of real-world security (by ?)
    - specification/policy: what is the system supposed to do?
    - implementation/mechanism: how does it do it
    - correctness/assurance: does it really work?
    - human nature: can the system survive "clever" users?

### Basic security analysis
- how do we as organisations secure <something>? Is system <something> secure?
    - who/what are we protecting?
    - who/what are the adversaries/potential threats?
    - what are the security requirements
    - what security strategies are effective?
- these are used, but adapted to different organisations (based on industry/kinds of data being protected)

#### What are we protecting?
- info/knowledge *assets* and *value*
- understand architecture of the system
- useful quesitons to ask:
    - operating value - i.e. how much we lose per unit time if the resource stopped?
    - replacement cost: how long would it take to replace it?
        - quite high if it's something that gives you competitive advantage

#### Who is the adversary?
- *identify* potential attackers
    - how motivated are they?
- estimate their resources
- estimate number of attackers, probability of attack
- recall definition from earlier classes: risk, vulnerability, threat
- exam: ask about concepts; stuff that matters in this space
    - won't find this in books!
    - more in line with workshops
    - know what's going on around them; concepts in slides    

#### Common (abstract) adversary
- framework to help orgs assess who/how big threats are
    - attacker action
    - attacker sophistication
    - attacker access

#### What are the security requirements?
- enumerate security requirements: CIA, availability, auditability, access control, privacy, ...
    - understand what they mean beyond the definitions
    - in crypto: doesn't matter if you understand the mathematical equations - but matters to understand what it means when we have individuals communicating; intercepting; concepts in workshops

#### Strategies to achieve security
- no security
    - legal protection
- ...
- resilience to attack
    - redundancy system ("hot spares")
- detection and recovery (& offense?)
    - intrusion detection system
- *will not be asked in depth*
- types
    - prevention
        - passive (always there in the background)
        - not all are physical (e.g. anti-copy software)
        - prevention is the hardest strategy to implement and often the most expensive
            - "defense is harder than offense"
            - protecting a VIP - analogy
            - expert assassin might still get the target
    - deterrence
    - surveillance
    - detection and response
    - perimeter defense: old principle
        - in Middle Ages, we have castles placed in very strategic places
            - at the border so you can get away if you needed to; get in if you needed to
        - spread around, moat, ...
        - different defense mechanisms in a castle
            - where you are
            - moats
            - towers + different way of accessing the tower
                - tower in tower in tower, ...
                - which among the many?
            - exactly the same principles being used for coomputer systems:
                - idea of getting through multiple gates
    - compartmentalisation
    - layering

### Threat modelling
- can't protect against everything
    - too expensive
    - takes too much time
- identify the things to protect against

### NOTE
- copy things over from the slides.

# Knowledge leakage talk
- Carlos A. Agudelo
- supervised by Rachelle Bosua, Atif Ahmad, Sean B. Maynard

## Context
- leaking information out of the company
    - email documents out
    - printing documents
- example
    - Uber/Waymo
    - common in pharma, consulting companies
    - Equifax, Deloitte

## Outline
- motivation
    - mobile devices, social media
- definitions
- framework
- methodology
- preliminary findings
- contributions
- limitations; future work

## Motivation
- mobile devices increasing risks
- each security incident costing an average of US$2.8m (Australian businesses)
    - 2nd highest spend worldwide for investigating/assessing these breaches
    - insider threat: employees the main cause of knowledge leakage, more than hackers
- key questions
    - how can organisations protect their information/knowledge assets?
        - what security strategies?
        - how can these be deployed?
    - problem of security goes beyond IT - most organisations have IT security capability but not leakage mitigation capability -> address the human aspect

## Literature
- literature review
    - theories from organisational strategy
    - knowledge management
    - information security management
    - computer science

### Data vs. information vs. knowledge
- data -> information
    - processed, analysed
- information -> knowledge
    - absorbed into the human mind
- knowledge: 2 type
    - tacit knowledge: e.g. dancing, cooking
        - not easily pexpressed; learn by doing
    - explicit knowledge
        - has been qualified - in books, documents
        - back to information
    - stored in mind; cannot be stored in a computer *(debatable; computers have "knowledge" with ML/AI)*
- knowledge -> information
    - knowledge can be externalised: verbalised and/or illustrated
- information -> data
    - captured and stored

### Knowledge cycle
- once once knowledge has been made explicit (codified) into artefacts (text/A/V/pictures) then it becomes information (data) (Alavi and Leidner, 2001)
- argue: possible to infer knowledge from information (a knowledge object) which can enable an unauthorized party to cause harm (e.g. competitive advantage erosion, loss of reputation, financial/legal liabilities) (Alavi and Leidner, 2001)
- inference attack: information that has been leaked before + new information -> infer knowledge about something
    - interviews with knowledge managers: people tend to disclose information because they think they can safely disclose some information
    - don't realise: said information can be correlated with other pieces of information

### Knowledge
- Davenport and Prusak (1998)
    - documents, repositories, routines, processes, practices, norms
    - a fluid mix of framed experience, values, contextual information, and expert insight that provides a framework for evaluating and incorporating new experiences and information. It originates and is applied in the minds of knowers. In organisations, it often becomes embedded not only in documents or repositories but also in organisational routines, processes, practices, and norms.
- difference between perspectives of knowledge managers and security managers (coming next)
    - security managers tend to be quite restrictive in their approach to address information and knowledge leakage
        - constrain outflows of information
    - KM tend to enable innovation and sharing - more important for them to enable sharing

### Perspectives on knowledge from KM literature
- perspective
    - knowledge vis-a-vis data and information
    - state of mind (Schubert et al, 1998) - state of knowing and understanding
    - object (Carlson et al 1996, Mcqueen 1998, Zack 1998) - object to be stored/manipulated "knowledge stocks"
    - process
    - access to information
    - capability

### Knowledge leakage
- accidental/deliberate loss/unauthorised transfer of information
- ...

### Knowledge leakage - confidentiality
- CIA triangle -> focus on confidentiality
- prevent access of information/knowledge from access by unwanted parties

### Intentional vs. unintentional
- intentional
    - disclosure of knowledge
    - copy of organisation's sensitive content
- unintentional
    - focus here - most interesting; if you want to leak knowledge
    - accidental email to recipient
    - loss of staff (experts leaving the organisation)
        - firewall, encryption, etc. won't do anything
    - outsourcing/joint ventures
    - employee oversights (human errors/insider threat)
    - poor business process
    - risky behaviours
        - posting confidential details on social media
        - phishing emails
        - open public WiFi networks
        - selection of poor security controls/bypassing controls (weak password)
- examples of organisational knowledge
    - IP
    - trade secrets
    - business strategies
    - product designs
- research focus: knowledge-intensive organisation
    - organisation that derives profits from knowledge activities
    
### Example scenarios
- data leakage
- information leakage
- knowledge leakage
    - knowledgable employee leaves company to competitor
    - solution: NDAs, ...

### Knowledge Leakage Risk (KLR) - definition
- a measure of the extent to which an organisation is threatened by a potential KL circumstance/event, and typlically a function of
    - the adverse impacts that would arise if the KL (knowledge leakage) circumstance/event occurs, and
    - likelihood of the event

### KL framework
- matrix
    - type of knowledge: tacit/explicit
    - nature: intentional/accidental

### KL as a multiple dimensional problem
- human dimension
- organisational
- technical
    - information can go from data to knowledge -> cycle

### Taxonomy of KL Strategies
- prevention
- surveillance
- detrrence
- ...

### KL framework II
- formal; tacit: trade secret, trademark, confidentiality agreements (NDAs, ...)
- informal; tacit: secrecy, keeping knowledge tacit, confidentiality, complexity
- formal; explicit: copyright, IPR, patents, trademark, design right
- informal; explicit: DB/network protection, division of duties, complex design, fast innovation cycle