# Security Assessments and Testing
23/06/2021 Cybrary

## 6 Security Asssessments and testing objectives
- Introduction to Security Assessments/Vulnerability Assessments
- Penetration testing
- Remediation(how we fix the problem we find)
- Intrusion Detection
- Audit Logs
- Common Vulnerabilities

## Vulnerability Assesments and Penetration Testing
- Vulnerability Assessment (just starting point) 
~ Physcial/ Administrative/ Logical
~ Identify weaknesses  
- Penetration Testing  (test if those policy works?)
~ Ethical hacking to validate discovered weakness  
~ Red Teams(Attack)/ Blue Teams(Defend)  
- NIST SP 800-42 Guideline on Security Testing  
- ###Audit is just check if the system following the security policy  

## Degree of knowledge
- Zero knowledge(Black box testing)  
~ Team has no knowledge of target + Must start with only information that is publically available  
~ Simulates an external attack  
- Partial Knowledge  
~ Team has limited knowledge of organization  
- Full knowledge  
~ Simulates internal attack  
~ team has full knowledge of network operations  

## Vulnerability Scanning
- Passive
- Identifying  
~ Active hosts on network  
~ Active and vulnerable services(ports) on hosts  
~ Applications  
~ OS  
~ Vulnerabilities associated with discovered OS & applications  
~ Misconfigured settings  
- Testing compliance with host application usage/security policies 
- Establishing a foundation for penetration testing  

## Attack Methodology  

1. Reconnaissance  
~ Whole DB, Company Website, Job Search Engines, Social Networking  
2. Footprinting(knowing the network)  
~ mapping the network(Nmap), ICMP ping sweeps, DNS zone transfers  
3. Fingerprinting(knowing about software)  
~ Identifying host information, Port scanning  e.g. OS TCP/IP is different handle
4. Vulnerability assessment  
~ Identifiying weaknesses in system config/ Discovering unpatched software
5. ATTACK  
- Penetration  
- Priviledge escalation (Run as SU)
- Root kits - Collections of tools to allow continued access e.g. Back door software, can update the kernel of OS, very difficult to detect
- Cover tracks  
~ Trojaned Programs - replaces default utilities with ones that masquerade as system utilities that provide normal services, with the exception of helping identify the backdoor software
- Log Scrubbers

## Testing Guidelines
- Why Test?  
~ Risk Analysis  
~ Certification  
~ Accreditation  
~ Security architectures  
~ Policy development  
- Develop a cohesive, well-planned,operational security tesing program

### Pen test consideration
- 3 basic requirements:  
~ Meet senior management to determine goal of assessment  
~ Document Rules of engagement  
~ Get sign off from senior management  
- Issue: it could disrupt productivity and systems  
- overall purpose is to determine subject's ability to withstand an attack + determine effectiveness of current secuirty measures  
- Tester should determine effectiveness of safeguards + identify areas of improvement.
- ###Tester should not be the one suggesting remediation + Violates Seperation of duties | tester test / fixer fix

### Rules of Engagement
- Specific IP address/ranges to be testeed e.g. any restricted hosts  
- A list of acceptable testing techniques  
- Times when testing is to be conducted
- Points of contact for pen testing team, the targeted systems, and the networks
- Measures to prevent law enforcement being called with false alarms
- Handling of info collected by pen test team

### Type of pen tests
1. Physical Security
~ Access into building or department  
~ Wiring closets, locked file cabinets, offices, server room, sensitive areas  
~ Remove materials from building   
2. Administrative Security  
~ Help desk giving out sensitive information, data on disposed disks  
3. Logical Security  
~ Attacks on systems, network, communication

### Approaches to testing 
- Do not rely on single method of attack  
~ Get creative   
- Path of least resistance  
~ ALWAYs start with users - social engineering is often the easiest way to gain access  
- Break the rules  
~ Even if a company follows its own policy, standards and procedures, it does not mean that there are not vulnerabilities  
~ Attempt things note expected  
- Do not rely exclusivly on high tech tools(Dumpster diving)  
- Stealth methods may be required  
- Do not damage systems or data  
- Do not overlook small weakness in serach for the big ones  
- Have a toolkit of techiques 

#### Network Scanning
- List of all active hosts
- Network services: ICMP, UDP&TCP
- Port scanner: Nmap, Finger Printing

#### Passwork Cracking
- Goal is to identify weak pw
- Pw are generally stored and transmitted in an encrypted from called a hash
- Pw cracking requires captured password hashes  
~ hashes can be intercepted   
~ can be retrieved from targeted system  
##### Crack techniques
1. Dict attack
2. Brute force
3. hybrid 
4. LanMan password hashes
5. Rainbow Tables
 
#### Rouge Infrastructures 
- Unauthorized DHCP Servers can be used to redirect hosts to rogue DNS servers 
- Rogue DNS servers can direct traffic to spoofed hosts 
- DNS zone transfer info contains much info about a network and its config
- Secure physical access to the network, require DHCP servers to require authorization, User DHCP reservations and MAC addressing to control assignment of IPs, Secure DNS zone transfers only to specific hosts

#### War Dialing
- Goal is to discover unauthorized modems   
~ Provide a mean to bypass most or all of the security measures in place  
- Dial large blocks of phone numbers in search of available modems  
~ should be conducted at least annually  
~ should be performed after-hours  
- Include all numbers that belong to an organization, except those that could be impacted negatively  
- if removal is not possible, block inbound calls to the modem

#### Corrective Actions
- Investiage and disconnect unauthorized hosts
- Disable or remove unnecssary and vulnerable services
- Modify vulnerable hosts to restrict access to vulnerable services to a limited number of required hosts e.g. host-level firewall or TCP wrappers
- Modify enterprise firewalls to restrict outside access to know vulnerable services     
~ Ingress Filtering: No inbound traffic allowed with internal addresses(spoofing)     
~ Egress Filtering: No outbound traffic allowed with external addressing(DDOS)
- Upgrade or patch vulnerable systems
- Deploy mitigating countermeasures 
- Improve configuration management program and procedures
- assign a staff member to monitor vulnerability alerts/mailing lists + examine applicability to environment + intiate appropriatte system changes
- Modify the organization's scurity policies and arachiecture 
- ALL ABOVE ACTIONS require going throgh proper change management procedures

#### Watching network traffic 
- Traffic analysis (side channel analysis)
~ Watching traffic and its patterns to try and determine if something special is taking place  
~ e.g. lot of traffic between two military units may indicate that an attack is being planned   
~ e.g. traffic beween HR/Headquarters may indicate layoffs are around the corner  
- Traffic padding
~ Generating spurious data in traffic to make traffic analysis more difficult e.g. sending out decoy attacks   
~ amount and nature of traffic may be masked  
~ attempt to keep traffic constant so no information can be gained