# Guest Lecture

## What do you do every day?
### Barry (AGL)
- haphazard, rebuilding security capabilities
    - outsourced security -> no control
    - industry trend; cyclic: outsourcing -> clean-up -> outsourcing -> ...
        - people who drag everything back in aren't sufficiently concerned with cost controls since they're concerned with recovery
        - then the people who come in later with budget in mind
        - if you have insourcing in mind - less likely
            - cost high, but can deliver better services
- as a security architect, deploying solutions that fit within the business's architecture
    - rolling on Crowdstrike, CarbonBlack, ???
    - endpoints that enable you to not only do protection, but also forensic capabilities (more than previous products)

### Peter
- Melbourne Uni for ~20 years
- contrasted to Melbourne Uni
    - AGL - very controlled, need ID card, etc.
- challenge: balance between keeping things secure, but still open (academic, etc.)
- worked for Faculty of Medicine and Dentistry
    - patient data: processing, deidentifying, 
    - uni is not siloed: work with other organisations (hospitals, drug companies)
- day not spent on terminal/console/IPS or ADS(?)
- currently involved with a project - return of artifacts to museums
- dealing with politics is not a purely computer-only thing
    - academics like to do things their way, unis have policies
    - not just black-and-white; but a lot of grey

## Progress of facial recognition, etc.
- new Melbourne Uni parking plate system -> license plate regonisition system
    - does not work well

## Privacy vs. security
- spatial recognition debate: privacy vs. security
    - privacy is security; but security in the classic CIA (confidentiality, integrity and availability), confidentiality is privacy
- IT security should enable and empower people
    - empowering people to protect their privacy
- Melbourne Uni project - allow only vetted devices to go on the network
    - didn't work
    - original goal: identification of network traffic, etc.

## IT security
- IT has traditionally been the PITA decision
    - if you stop people from getting what they want, they will bypass you
- IT security has been the stick; need to provide the carrot to work with people
    - Dropbox and Gmail: people don't have to jump through hoops
    - need to make stuff easy to use -> otherwise, fighting with users rather than helping them

## Data sovereignty - important issue to take note of?
- definitely
- Equifax: credit agency
    - credit checks either owned on them, or other credit agencies interoperate with them
    - ~143m US people's data, ~40m UK people
    - ReadyReference - job reference software under Equifax
        - everywhere you worked, lived
    - "lost": lost sovereignty
    - had massive amounts of data going out; but no means of checking: "we shouldn't have this amount of data going to an IP address that doesn't belong to our partners"
- utility, and a control network
    - SCADA: subset of industrial control systems
        - control power paints, gas flows from gas valves
        - systems under isolated networks
    - duty of care and strict regulatory requirements on customers' data
- data sovereignty
    - Unimelb didn't join Office 365 until Microsoft reassured that data will be stored in Sydney
    - issue: forwarding of email
    - issue:
        - Microsoft is a US government -> US law: they can take anything stored in their servers
            - MS goes to court against the US government
            - overreach in basically every matter
        - Echelon - how the governments of Canada, US, UK, NZ and AU made an agreement to circumvent the legislation from each country that prevent themselves from spying on their citizens
            - swap data
            - "5-eyes agreement"
            - share a lot of data: facial recognition
- is AGL running Cisco? (a lot of a particular vendor's equipment)
- intelligence that backdoors might be built into NBN
    - imagine if an unfriendly foreign country takes control of our broadband network

## NYT article
- source of US Senate Committee passing down a ban on the Russian security companies' products in the US governments
    - https://www.wsj.com/articles/russian-hackers-stole-nsa-data-on-u-s-cyber-defense-1507222108
    - contractor removed sensitive information and put it on his home computer
    - leaked presumably via Kapersky's AV
- indicative of complexity of SW and HW
    - updates!
    - anyone who's ever used an AV program -> "do you want to send stuff to us to improve protections for everyone"
- if you look recently, one of the senior guys at Kapersky was arrested by the Russian gov't
    - people in Russian intelligence who were talking to the FBI
    - one of them mysteriously died
    - Russian gov't not very fond of Kapersky at the moment
    - US president who was willing to hand back spy compounds to the Russians
    - take: if US gov't is cracking down on Kapersky -> pissing them off
    - other point: comes back to what Sulette was saying about Kapersky uploading data about tools that shouldn't have ever been on unclassified networks
        - realistically: data has been out quite a while back - could've still gotten the code from GitHub
    - if Kapersky isn't "being bad", perhaps the US gov't thinks that Kapersky has a little too much power
        - userbase of X
        - that power
    - AV companies are the ones who called out intelligence operations in cyberspace
        - AV company researchers find tools in place in clients' networks
- lobbying - AV lobbyists, other parties, IC interests
    - who knows why these decisions were made
    - nobody's loving Kapersky
- software is intangible - very hard to restrict usage of software
    - first official export of PGP to Australia: as a book
    - North Korea: hell of a lot of things that cannot be exported (detonators, nuclear fissile materials)
    - we can still have "rogue" people in the government running Kapersky

## Issue: restrictions on the export of security info
- Vanessa working on (presumably) open-source product; secure electronic voting adapting innovative ways in existing cryptography
    - cannot communicate to people outside the country
    - even when she is out of the country; officially under this legislation, she has to ask if they are in the country every time
    - quite onerous on academics -> make sure that people who are involved with cryptoprograms from "putting in backdoors" for other countries
- similar legislation in the US
    - giant door in US legislation, especially if OSS, or going to be published
- software being intangible ->
    - when you look at crypto legislation, if a party can see everything you transfer -> can think as intangible, but you can see whatever you're doing
    - 2 provisions of crypto legislation: manufacturer has to break the crypto; or to give a backdoor on the endpoint
        - e.g. if manufacturer deems that it's not feasible to break the encryption for say, bank transactions
        - by legislation, they have to give the government a backdoor into the endpoint
        - at that point, OSS becomes the "savior", but comes back to inertia
            - most people will use what they're familiar/comfortable vs. something else a bit more "kinky" -> difficult to get up and running
            - e.g. Apple, MS' prevalence
            - tradeoff between security vs. convenience
                - common in this industry
            - any answers to questions on "what you should no" is at best simplistic and at worst harmful

## "IT security cold war"?
- video: hackers made a generator blow itself up by speeding it up -> shook itself loose of the restraining bolts that go into complete and annihilated itself
- replicated what Stuxnet (worm) did
    - Iranian nuclear program - US had 2 options:
        - kill all the scientists
        - disrupt the program in such a way that people think it's their inexperience, equipment
            - Stuxnet
            - not only Windows side of things, but the SCADA side of software
                - PLCs that drive the centrifuge (programmable logic controllers)
- -> has Australia started to take PLC security more seriously
    - "I can't answer that question"
    - threat of APTs (advanced persistent threats)
- Influence by Cialdini
    - 1984 book on influence and marketing
    - looking at stuff and think "how silly", that's how you get trapped
    - human beings doing human being stuff to get by
- majority of senior management in IT in the defence force have psychology degrees
    - learn marketing, communications
    - ultimately people see IT as a cost!

## Growing market for graduates and jobs in SCADA systems?
- already growing
- current shortfall in security specialists
    - supply and demand, bla...
- people who can do SCADA better compensated than other IT security specialists, which are pretty well compensated
    - standard corporate network + operations network edge + isolated operations network 
- boring is in the eye of the beholder
    - if a mistake makes 3m people lose access, that's interesting on its own

## "isolation" of SCADA systems
- people will opt for convenience
- while you have a protocol barrier, people don't actually totally airgap
    - Faraday cage: total isolation
    - look at BadUSB and BadBIOS

### Zooko's triangle
- like fast, cheap and good (for food)

## Party tricks!
### WiFi Pineapple
- ARM-based computer with wireless interfaces running a cut-down version of Linux
- can do WiFi network auditing, interception, SSL interception, deauth attacks on WiFi connections, listen for probes
- networks that are stored in your phone -> phone/laptop will actively look for those
    - can build up a clear picture of where this person goes in the day

### ?
- Pineapple
- a bunch of info from a specific MAC address in a specific area
- places that John's been
    - Lance Dixon Free WiFi
    - WestFieldFreeWifi
    - ICTIOT, TGSWN
- wigle.net -> look up SSIDs by location
    - this person goes to Kew
    - where the person was at the time -> around Hawthorne
- Wireshark -> find out what kind of device the person was us

### Don't connect to free WiFi!
- pick SSID from the list
- HTTP traffic getting intercepted
    - thus the push for hTTPS
- inference attacks
    - start taking inferential data about you
    - metadata: even if you can't see the content, as long as you can build up metadata, you don't need the data

#### HTTPS
- Google.com
    - DNS request!
- flip side: data centers sharing many customers on the same IP address
- Tor
    - DNS requests go through Tor

### SSL - caveats
- idea: certificate says what you're connecting to, signed by an authority that you trust
- or signed by any huge number of CAs that your browser/OS/etc. trusts
    - pool of root CAs that you will blindly trust

## Shadowbrokers, Vault7
- timing
    - interesting events in 2016 -> infer some things -> draw interesting conclusions about who Shadowbrokers
    - probably not Russians, but does not mean not Russian-afiliated
- 2 things
    - "legend": we're this l33t hackers and now we're dumping this shit
    - reality: people who stole and people who dumped are probably not the same
        - question: nation states already stole the stuff, so no nation states will pay up

## ?
- IC people: intelligence community?
- hacking: couple of things in the question
    - 1 -> classifications of US classified material
        - NOBUS: nobody but us.
        - "in theory": even our allies don't get access to this material
        - ways and means; bugs in software: delusional
            - studies on refindings of bugs in software -> surprising numbers
        - 2014: Obama ordered the disclosure of vulnerabilities
            - "you don't have to disclose anything if you're an intelligence agency as there is a 'clear intelligence need'"
    - 2 -> flip side with ETERNALBLUE, MS and NSA
        - almost certain that NSA reached out to MS
        - MS did that and the fix was availabile
        - 91 days between fix to WannaCry
        - same sort of things with CodeRed (60-90 days between when the patch is release, and the breakout)
        - organisation needs to get their shit together
            - Equifax is prime example of what to do wrong
                - CIO w/o IT experience

### Hospital
- medical equipment: only a certain environment is certified
    - are you going to replace a $300k machine just to replace the computer part to deal with the upgrade
- as a pragmatic security practician, higher-ups still have other priorities and concerns
    - have spare stock of IDE HDDs
    - hospitals run this stuff with the intention of running it for 10-15 years
    - after the 3-5 years, support costs ~20%-ish of the purchase price
- hard to blame hospital -> blame the equipment manufacturer
    - sweet-spot their profit by going with minimal effort versus something that's expected to be safe over the expected lifetime
- maintenance lifecycle, at what point is the organisation going to be forced to repalce this?
    - organisations are always making the tradeoff of where to spend the dollars for maximum effect
    - people don't care about the risk until something drastic happens

### Back to SSL - demo
- CAs, organisations with varying degrees of trustworthinesss
    - Mozilla delisting a couple of root CAs
- important to realise that you don't know all the root CAs on your machine
- other important point: if you work for an organisation, mostly if you use BYOD/WiFi on the network, you have a MDM-type setup
    - restrictions to the machines
    - installs a certificate
        - basically an authorized MITM
- general security question: what can this be misused for

