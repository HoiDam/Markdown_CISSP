# Software Development Security
01/07/2021 Cybrary

## Design Process
### Reduce the attack surface  
- Evaluate the attacks of the product
1. User input fields
2. Protocols/ Services/ Interfaces/ Processes
3. Resources files
4. Open named pipes/ open sockets
5. no. of items accessible?
6. Dynamic web pages(ASP,etc)
7. Guest Accounts enabled
8. Acces Control config

### Threat Modeling
- Identify Scurity Objectives: Legislative Drivers, Contractual Requirements, Alignment with business objectives
- CIA Triad
- Tools for threat modling : Data flow diagrams, use/misuse cases

### Risks in Design
- Threat modeling: Stride

### Controls Evaluation
- Efficacy of controls
- Economy of mechanism
- Cost/ Benefit Analysis
- Psychological acceptability

## Desgin Considerations
- CIA
- AAA
- Secure Design Priniciples

### Risk in Design
- Code Reuse
- Flaws vs Bugs
- Flaw: Inherent(固有) fault with the design of code
- Bug: Omplementation fault
- Open vs closed design

### Secure design priniciples
- Good enough security 
- Least privilege
- Defense in depth
- fail safe
- Complete mediation
- open design
- Economy of mechanism
- least common mechanism
- psychological acceptability
- leverage existing components
- weakest link
- single point of failure

### Security vs Quality
- Quality: Fitness for use. Degree to which a product meets it requirements
- Security: Focuses on reducing probability and/ or impact of vulnerabilities/ threats
- Both security and quality are best implemented throughout the entire developemnt lifecycle

## Secure Techonologies
### Requirement to writing secure code
- Training an awareness for developers
- Shift of focus/ understanding for managers
- Security Checkpoints and reviews
- Bug trackking 
- DREAD: Damage potential, Reproducibility, Exploitability, Affected user base, Discoverability

## Secure Cloud/Web App
### Determining data sensitivity
- 6 key question in relation determining data sensitivity . ? Impact if:
1. Info was widely distributed
2. Employee of cloud provider accessed the app
3. Process was manipulated by an outsider
4. Process failed to provide expected result
5. Info was unexpectedly changed
6. App/ Info was unavailable for a period of time 

### Cloud application architecture
- App programing interfaces
- Multitenancy(多租戶技術)
- Cryptoraphy
- Sandboxing
- Application virtualization

### Security responsibilities across models

### Software development lifecycle / Sofware development methodologies
#### Waterfall 
- Step by step
- Pros  
~ Each phase has specific deliverables and a review process  
~ PHases are processed and completed one at a time  
~ Best for small projects where requirements are very well understood   
~ reinforces "define before design" and "design before code"
- Cons  
~ Adjusting scope during the life cycle can kill project  
~ No working software produced until late during the life cycle  
~ High amount of risk and uncertainty  
~ Poor model for long and ongoing projects  
~ Poor model IF there is a high probaility of change   
~ End of project can be far removed from the beginning in which the initial requirements are specified

#### Prototype
- Loop for dev + improvement
- Pros  
~ Software designer and implementer can obtain feedback from users early in the project  
~ client and the contrator can compare if the software made matches the software specification, according to which the software program is built  
~ allows the software engineer some insight into accuracy of initial project estimates and whether the deadlines and milestones proposed can be successfully met
- Cons   
~ Client rarely understand all the ramifications of proposed changes   
~ Developers may use shortcuts to create the prototype and sometimes do not formalize their processes for the actual product

#### Spiral
- Waterfall + Prototype
- Pros  
~ High amount of risk analysis   
~ Good for large and mission-critical projects  
~ Software is procduced early in the software life cycle  
- Cons  
~ Can be costly model to use  
~ Risk analysis requires highly specific expertise  
~ Project success is highly dependent on the risk analyisi phase   
~ Does not work well for smaller projects  
#### Agile

### OWASP Top 10 Vulnerabilities
- OWASP is an international non-profit organization
- Open Web Application Security Project 
- Offers a broad consensus on the cost common security flaws/ exploits
- Designed to raise awareness and the stress the need for security in web-based app

### IAM and federated identity management

### Application security testing

## OWASP TOP 10 2017
1. Code Injection
- Injection flaws, e.g. SQL, OS, LDAP injection occur when untrusted data is sent to an interpreter as part of a command or query
- Attacker's hotile data can trick the interpreter into executing unintended commands or accessing the data without proper authoirzation
2. Broken authentication & session management
- App functions related to authetication and session are not implement correctly
- Allowing attackers to compromise pw, keys, session token, to exploit other implementation flaws to assume other users' identities
3. Sensitive Data exposure
- Web app do not properly proteft sentitive data e.g. credit cards, taxIDs
- Attackers may steal/ modify
4. XML external entities
- Attackers can exploit vulnerable XML processors if they upload XML include hostile content in XML document
5. Broken access control
- Core skill of attackers
- Static application security testing / Dynamic application secuirty testing
- Detect absence of access control but cannot verify it is functional when it is present
6. Security Misconfigurations
- up to date
7. XSS
- XSS Flaws occur whenever an application takes untrusted data and sends it to web broweser without proper validation or secaping
- Allow attackers execute script in the victim's browser which hijeack user sessions, deface websites, redirect user to malicious sites
8. Insecure deserialization
- process of turning some object into data format that can be restored later
- Most popular data format for serializing data : JSON , XML
9. Known vulnerable componnet usage
- Some libraries, frameworks run full priviledges
- If those component exploited, attack can facilitate serious data loss/server takeover
10. Insufficient logging and monitoring
- Bedrock of nearly every major incident


## Security Common Used Architecture
### Organizational Normative Framework(ONF)
- Specified in ISO 27034
- 1 org 1 framework
- Defines component of app security best practices   
~ Business Context   
~ Regulatory Context  
~ Techincal Context   
~ Specification  
~ Roles  
~ Processes  
~ Application security control Library
#### Application Normative Framework
- Used in conjunction with the ONF and is created for specific applications
- Think of best practices for applications within the context of organization
#### Software unsecure reason
- Lack of training
- Lack of funding
- No prioritization of security 
- Security as an afterthought
#### Validation
- Does the software solve problem
- Does it meet real world need
- Is it customer/ manager wanted
#### Verification and Validation Checks
- Check for presence of securiy protection mechanisms to ensure confidentiality, integrity of data and system availability,
authentication, authorization, auditing, secure session management, proper exception handling and configuration manamgemnt
#### Certification
- Technical evaluation of security features of a product in a particular enviornment
#### Accreditation
- Management's / Customer's acceptance(risk ) of the product
- decision to implementsoftware in their environemnt
#### Post Acceptance
- Continue to monitor

## OOP
- Most widely used approach software development
- Traditional programing: (I P O)
### Classes and Objects
- Class = Conecept
- Object = instance of class

## Secure Database Design
### DB models
#### Hierachical DBs
- Store related info treelike fashion e.g. DNS
#### Distributed DBs
- Contents storing different locations e.g. different servers for .net , .com , etc
### Vulnerabilites, Threats, protections
- Aggregation (connecting small info to determine)
- Inference (chok info without any knowledge)
- Polyinstantiation(資料混合)
- Code Injection
- Input validation
### ACID test
- Atomicity: Transaction are either fully committed or rolled back
- Consistency: Database rules are enforced
- Isolation: Transactions are invisable until committed
- Durability: Once commit has been recieved, transaction cant be rolled back
### Goal of DB
- Data -> Info -> Knowledge

## Malware
- Adware
- Virus
- Worms
- Spyware
- Trojan
- Rookits
- Backdoors