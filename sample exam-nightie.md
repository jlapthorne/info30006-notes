# Sample Exam Questions and Notes
Exam will be 2 hours

## Part 1: Infosec 

- The CIA Triad represents fundamental security goals of Information Security. Describe two other security goals and briefly explain what they represent. (3 marks)
  - Non-repudiation
    - Where the author of a piece of information will not be able to disprove that it was authored by one. 
    - This represents systems, technicalities or procedures in place that would definitely prove that any information comes from a verified sender, in order to provide authenticity of information. 
    - In the CIA triad, this provides an extension of integrity of information, in which the use cases demands integrity of information via avenues of ensuring information can be held accountable from the producing parties 
  - Anonymity
    - The concept of staying anonymous, or which information source and transfer are shaped in a way to make it intricate or impossible to be identified
    - They represent the an alternative use case of information. When coupled with confidentiality, this goal attempts to ensure information is untraceable to its original bearer by any means
- List 5 different types of security threats and provide an example of each.
  - Acts of human error
    - Wrong data entry from employees
    - Mistakes in inputting or accessing information
  - Compromises to intellectual property
    - Breach of patents
    - Privacy
    - Copyright infringements
  - Technical obsolences
    - Old software or hardware that are hardly updated
    - No longer any information
  - Software failure
    - Software goes down, crashes, enters a crash, or is taken malicious control over
  - Hardware failure
    - Same thing as above but hardware 
  - Deliberate acts of sabotage or vandalism
    - Someone attempts to modify, damage, or destroy assets
  - Deliberate software attacks
    - Attacks towards software - this is obvious
  - Deliberate acts of thefts
    - Removal of data, physically or electronically
  - Deliberate acts of information retrieval and extortion
  - Deliberate acts of espionage or trespass
  - Deviation of service
    - Service outages, failures, such as power outages, internet outages, DNS outages
  - Forces of nature
    - Natural disasters
- You  are  conducting  a  risk  management  exercise  in  your  company  and  you and your team have identified 10 risks that have been classified as project and business risks.
  - Describe what project and business risks are
    - Project Risk: Uncertain conditions that has an effect to at least one single project objective to have negative impact on a small, project-scope 
    - Business Risk: Associated with the wellbeing and execution of an entire organization, associated with business purpose of projects
  - Describe  the  processing  of  analysing  the  identified  risks  before  you can respond with the proper response strategy. 
    - Risk managemment model
      - Identify
        - This is where we are
        - Examine current security situation
        - What's in the assets we want to protect
        - Vulnerability analysis
        - Check for residual risk we have to keep in mind
      - Assess
        - Impact
          - In dollars and cents, of the risk
          - Cost of attacks in real money
        - Likelihood
          - How likely would it happen? 
          - Can be calculated from past incidents, experience, simulations, expert decisions and heuristics
      - Response strategies
        - Avoid
          - Safeguards, Defense in Depth
          - Costly to set up and maintain
        - Transfer
          - Kind of like insurance companies - let someone else deal with it
          - Not always applicable in all cases where the screw-up is definitely only your problem, or if they are uninsured 
        - Mitigate
          - Response plans
          - ICP, DRP, BCP
        - Accept
          - Understand and accept that it will happen
          - Not something we can do on every level - some of the tiniest threats can be shrugged off

## Part 2: Cryptography and Protocols 
- What is  wrong  with  512-bit  RSA?    Why  was  it  mandated,  for  what purpose, and how long ago?
  - 512-bit RSA has been proven to be breakable from FREAK attacks 
  - We use an MITM to modify the request for 512bit RSA from the server and forge it to get communications between clients and servers
  - 512bit RSA is also trivial to exploit and brute-force with modern day services - about a hundred bucks running on AWS
  - Especially when server and client doesn't do ephemeral key exchanges, third party can factor the RSA key sent from the server and then pose as the server at any time or to read client transmissions
  - It was mandated back in the era of the information wars in the 80s/90s by the US, in which it mandates export grade cryptography. 
  - The restrictions were already removed, but a lot of browsers and servers still support it
- Write two desirable secrecy properties of a key exchange protocol, and write a sentence explaining what they mean.
  - Forward secrecy
  - Future secrecy
- List three crucial security properties necessary for elections.
  - CIA
- You  are  a  manager  in  an  organisation  and  are  explainingto  a  staff member why and how to use Signal.  Briefly justify why they should use Signal, and at least one important applied security feature in it including instructions on how to use it.
- Give 3 specific examples of digital footprints that impinge on privacy.
- Provide at least one way to improve user adoption of privacy-enhancing technologies and explain why it will improve adoption (briefly)

## Part 3: Privacy MCQ 
- WhatsApp provides confidentiality of communication and anonymity: **True**, following Signal protocols 
- Which of these are samples of metadata: 
  -  **The creation date of a cell-phone photograph**
  -  Your public key listed in your signature (on some implementations this can be defined as part of metadata, but we are now sticking to the dictionary definition of metadata)
  -  A video attachment sent over WeChat
  -  All of the above
  -  Two of the above
- If an APP entity holds personal information about an individual, the entity must,  on  request  by  the individual,  give  the  individual  access  to  the information without exception: **false**
- An APP entity must have a clearly expressed and up to date policy about the management of personal information by the entity which contains:
  - the kinds of personal information that the entity collects and holds;
  - how the entity collects and holds personal information;
  - the purposes for which the entity collects, holds, uses and discloses personal information;
  - all of the above
- In relation an APP entity’s functions or activities,  the  entity  must  take reasonable  steps  to  make  sure  it  complies  with  the  Australian  Privacy Principles in its:
  - practices
  - procedures
  - systems
  - **all of the above**

### Privacy Essay 
- You take a photo of your cat on your smartphone and then upload it to a cat website. What metadata could be included specifically in that photos that infringes your privacy (not to mention your cat’s)
- Explain briefly why privacy is important even if you’re not doing anything ‘wrong’
 