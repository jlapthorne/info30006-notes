# Week 6 lecture
Guest lecturer: Dr. Peter Eckersley, chief computer scientist at EFF

## Copyright
- person who wrote Napster was arrested in Norway at the request of the US
- government policies mostly protect rivalrous good

## How did you end up at SF?
- the Internet came from SF, Silicon Valley
- didn’t know about that, but knew EFF was doing really great work
- interviewed over the phone and hired him
- lots of opportunities, Bay Area is always hiring
	- reach out to people not just in academia, but be part of the community around you
- major established tech companies
	- Apple, Google, Mozilla, Amazon
	- interview with them, very good employers
- startups that can do new things
	- US, huge amount of startups in Bay Area
	- better idea to do that there than here thanks to a community of expertise
	- a lot of money for projects, investors know how to invest in technology

## What the EFF does, history
- digital civil rights organisation
- pretty old - founded in 1995 by a group of rich visionaries
	- founders:
		- wrote first spreadsheet software
		- started a bunch of successful companies, but a bit weird
		- ?
	- role playing game was raided by the FBI mistook it for real things
	- internet is changing how everything works
	- set up a fund to defend people
- a lot of the law is made by judges as they judge cases
	- precedent
	- you create new law as you help make cases ends more favourably
	- future court cases will refer to previous court cases (precedent)
- joined a team of around 2, in 10 years it changed a lot
	- mostly it was digital activism
	- biggest campaign: against SOPA
	- Hollywood can basically make your websites disappear
- activism stuff
- team grew from around 2 people to 12 people
	- not just providing CS expertise to lawyers
	- started building technology
	- 6-7 really big projects
	- writing software, help people change the way people understand technology
	- Let’s Encrypt: free, automated and open Certificate Authority
		- used to be difficult to get a certificate
		- complicated process: which company, fees ($100-ish), ...
	- Certbot: software to run on Linux to get a certificate

### Let’s Encrypt
- ACME protocol
- how it works
	- you run a client on your web server
	- you need to prove that you own the domain?
	- install Certbot or a different ACME client
		- hey Certbot, get me a certificate for this web URL
	- Let’s Encrypt tells the server to prove ownership: shrubbery
		- special DNS record, or
		- serve a file over HTTP, or
		- serve a fake certificate over TLS, the kind that causes a browser to show a certificate error
			- Let’s Encrypt inspects, if it is valid shrubbery then issue the certificate

#### Why?
- HTTP is basically an open book
- we want to get the web to be HTTPS
	- started yelling at big tech companies in private
	- Google listened to EFF before the Arab Spring
	- during the Arab Spring, Facebook and Twitter deployed HTTPS
- but we wanted to extend that to the entire web by default
	- bureaucracy and cost of the certificates
	- in theory, you can get them for free, but in practice it is hard to do
	- $100-$1000 per year
	- also a genuine hassle and people might not think it’s worth it
- bureaucratic problems, tech problems
- haven’t solved: making auth mechanisms for HTTPS stronger
	- unfortunately it’s still possible to hack a router/domain name and get a certificate from Let’s Encrypt
- in order to provide a certificate, need to provide non-crypto proof
	- start with plain unecrypted
	- go up one ladder, then you get a key to be stored on your server
	- then from that, the key is used for future HTTPS challenges
	- what if you lose the key? get hacked?

#### Resistance
- IT departments that want to monitor employees and students
	- browsers hand them a solution
	- you can put on to those devices a new CA that lets the IT department to perform MITM attacks against everyone
- HTTPS: odd occasions

## Encryption, in general
- a lot of your work is spreading encryption and IT security
- but is there a downside/risk to society?
- encryption is a tool that has many use cases and consequences
	- HTTPS: very few downsides, except when you actually want to surveil
	- 2 branches
		- protect against hackers: keep passwords secure
		- bad thing for gov’ts to be able to monitor people everywhere
			- see Arab Spring
- tradeoff though
	- people can communicate freely and openly without being surveilled
	- may provide a powerful tool for criminals
- not a big fan of Bitcoin
	- makes it easier for people to attack
	- Bitcoin is interesting because the way it uses crypto uses a LOT of power, as an environmentalist

## Encrypted messaging in Australia
- issue of whether messaging allows future historians, investigators in criminal manners to investigate the president’s past messages
- historically, in the US, there was a time where crypto was regulated as ammunition
	- no SSH
	- Telnet
- EFF went into litigation about this, represented by Dan Bernstein
	- people have a free speech right to write cryptographic software
	- won, and thus crypto is available to everyone
- we thought we won the debate
	- say Gmail: secure only between you and Google, Google can comply to warrants
	- for messaging, end-to-end encryption
		- goes to the other end of the conversation
		- iMessage
			- iCloud backups are not encrypted
			- but if you turn off backups, it’s E2E’d
		- similar for WhatsApp, Facebook Messenger’s secret chats
- FBI wanted a way around iPhones’ encryption
	- and a way around iMessage by extension
	- waited until San Bernandino attack
	- “write a new version of iOS to let us go into the phone”
	- it’s like forging the blade that will be able to break into iOS forever
	- was theatre - they got backups from Apple for the phone
- other parts of the English-speaking world, where there is no protection of the freedom of speech
	- governments of these companies are trying to create backdoors in our encryption
	- UK, Australia
	- Australia by itself might not have the capacity, but if the UK and Australia work together

## Does the right for private messaging outweigh the ability to investigate?
- some people tend to be absolutists
	- it doesn’t matter what the tradeoffs are, but I want my right
- look at people who are unjustly incarcerated by the US gov’t
	- sure you will be tempted to use surveillance methods, for even the entire internet for a small group of people
	- not sure if we should break encryption for a gov’t untrustworthy as this
	- FBI did a lot of terrible things -> Martin Luther King
	- yes you can defend democracy with surveillance, but it’ll go back to you like a boomerang
- warrants, targeted investigations are less dangerous for security as a whole

### Alternative methods used by law enforcement
- best alternative: old-fashioned investigation and due diligence
- if you investigate everyone you get confused by a lot of statistical positives
- ask: “why are you so sure that statistical fishing expeditions work worse than old-fashioned investigation”
	- US had metadata
	- controversial because it violates US constitutional law
	- NSA: despite having metadata for the entire US calls graph, there were no terrorist attacks foiled

## Analytics and AI
- hype and AI
	- how much of this is real and how much of this is speculation
- project to find out policy implications
	- Machine Learning used to make decisions on people: loans, insurance premium, promote/fire, or people let out of person/incarcerated
	- or we might even share our planet with some other software-powered intelligent lifeform
	- AGIs
- we went sifting through data on how fast different specific fields of machine learning were making progress through specific parts: computer vision, NLP, ...
	- it’s a mix of both
	- there is significant progress
	- but still tons of sci-fi speculation

### Image recognition
- neural network trained against ImageNet
	- NNs are now better at this task than humans
- https://eff.org/ai/metrics
- VQA: visual question answering
	- instead of just being asked what’s in the picture, ask a natural language
	- how many slices of pizza in the picture? is it vegan?
	- what is the color of her eyes?
	- not yet solved
- social implications
	- biased ML - labeling Caucassians as non-dangerous, and African-Americans as dangerous
		- algorithms are trained on broken data
			- racist cops -> data -> trained system
		- immediate variable bias
			- if you have a ML system
			- build a model to predict
			- fundamentally possible whether something is going to be true in the future
			- suppose it’s insurance - predict probability of car crash in the future
				- there is an equation that spits out the true probabilities in the future
				- (if you Monte Carlo the entire universe)
			- the things that drive the true probability are usually not accessible to the model
				- e.g. driving skill - how much I can swerve/react, how sleepy I get when driving
			- variables that are accessible to companies - correlated, but not necessarily the cause
			- concrete example
				- people who drive at night tend to be a dangerous driver
				- model classified friend’s son as dangerous
				- but, he worked night shifts
				- model did not account for that
			- in racial bias models: immediate variables
				- are you inclined to work hard?
				- racial variables are not present in the model
				- but postcodes are -> proxy to race
		- what do you do about this?
			- paper on how to correct out these immediate variable biases
			- protected variables: gender, other variables with the taxonomy of gender
				- race: taxonomy of what the ? are
			- open area of research
				- any time you’re deploying a ML model
				- at least run tests to see if it is biased
				- and add de-biasing algorithms
		- people entitled to right to get a human-understandable explanation of why the network decided to make a prediction
- Monte Carlo analysis
	- complicated process
	- want to get a sense of the behaviour
	- what you put in are the current observations from weather stations
	- you do it once, and it spits out a number
	- or change the inputs randomly slightly, look at correlations, etc.

### No child left behind?
- education policy used to be based mostly on feeling/gut instinct
- instead of that, collect data and see what makes testing effective
- run standardised tests
	- schools who were able to get big improvements in test scores were likely to get funding
- whenever you turn a metric into a target, it ceases to be a good metric
- previous cohort cheating, next year teacher was not able to keep it up and would get fired by algo

### PageRank

## Aaron Swartz
- personal friend of Peter
- pursued by FBI, decades -> 7 years
- took his own life

### Summary
- brilliant, a little flighty
- out-of-the-box creative ways
- Peter was doing PhD on alternatives to copyright

### Contributions and achievements
- co-founder of Reddit
	- sold to Conde Nast, not excited about what Reddit was turning into
- RSS
- Internet Library
- interested in politics and political activism -> campaign in protection for digital rights
- EFF is based in SF, laws are made in Washington DC
	- the main way that legistation is passed in the US
	- law that has the potential to split the internet domain registration system
		- censorship

# Questions
## How to make a difference
- altruism
- career choice? from within the government or otherwise?
	- data on how to get access to important decisions
	- one person who is in the UK gov’t’s Foreign Aid department
		- he took 8 programs that are basically random, and have some systematic criteria
		- redirect these billions of pounds that are going to arbitrary stuff	  
	- research in looking into the human brain
		- new microscopic techniques that are a bit better
- look at how the company’s work impacts the world

## With ML and paroles
- comparison with humans?
- decent humans actually try really hard to make informed judgments on the people
	- ask a lot of questions, look at reactions
	- ask lawyers
	- 