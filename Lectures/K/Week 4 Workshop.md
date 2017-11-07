# DonateBlood.com.au data breach
- who?
	- Australian Red Cross Service
	- Precedent Communications
- what and how?
	- backup of the DB file saved to a public facing web server
	- 550k individuals affected
		- sensitive information

## Impact of measures taken to mitigate/avoid data breach
- gov’t assessed breach
	- could’ve taken more precautions
		- protection of personal information
		- retention of personal information
			- destroy or de-identify information when no longer needed
			- not all of the information needed to be collected
	- organisations are required to take steps to protect personal information (from loss, etc...)

## Precedent Communications Pty Ltd.
- w.r.t. its failure to protect personal information
- APP 11.1
	- technology
		- no IP auth system at time of data breach
			- due to incompatibility
		- company used live data in user acceptance testing environment
			- UNT: to test company’s new code and functionality which could be achieved w/ dummy data, instead of live data
		- did not take backups, did not control for the possibility of human error by restricting access
	- risk assessment
		- did not complete risk register
		- did not mention risk of data breach in the DonateBlood website and in the contract
		- did have, but policy did not address information security
			- did not document privacy obligations
	- the company itself - organisational safeguards
		- could’ve conducted better staff training
		- some staff did not read data protection policy at their commencement
		- no further training w.r.t. personal info and privacy problems
		- company did not take steps to improve security
			- no external experts/audits
			- no regular risk assessment analyses

## Human errors
- w.r.t disclosure of personal info
- Precedent breached this policy
- prevention:
	- could’ve disabled directory discovery to prevent public access

### Mitigation strategies
- assessment ?
- mitigation

## Does outsourcing reduce or increase risk?
- 4 key criteria
	- sensitivity of the assets they want to protect
		- very sensitive: want to take more extreme measures
			- want to limit amount of people who comes into contact w/ the data
		- less sensitive
			- might be a good idea to outsource security
			- firms are *probably* more well versed in this
			- might have proven strategy
	- what type of firm you work for
		- suggestion: except governance, risk and compliance
		- they just build a stack that wraps around it, and it goes back to you
		- limit exposure to risk: outsource only parts that exclude the actual data
			- access management, virtualisation, etc... can be outsourced comfortably
			- firewall management, network security, vulnerability scanning, anti-malware
	- companies w/o InfoSec expertise
		- have no choice but to outsource
		- do due diligence

## What we could’ve done as Blood Service?
- don’t outsource the actual database
- do due diligence
	- once the cat’s out of the bag, it’s out
- might push outsourcing out of the table
	- do it in-house
	- segment: outsource infrastructure, not with the data
- realistic
	- budget

## Risk?
- a scenario where something goes 