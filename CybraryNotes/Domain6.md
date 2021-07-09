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
1. Reconnaissance(偵察   
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
- Develop a cohesive(團結), well-planned,operational security tesing program

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

## Protocol Analyzers (sniffers) and Privacy
- Promiscuous mode
- Bridging/Switching affect the packet capture

## IDS 
- tool in a layered security model
### Purpose
- identify suspcious activity
- log activity
- respond (alert people)
- needs an interface in "promiscuous" mode
- port mirroring/ span needs to be enabled to view traffic on a switch
### Categories
- Host Based Intrusion detection system
- Networks Intrusion detection system
### IDS Components
- Both types of IDS have several components that make up the product
1. Sensor (Data collector)  
~ On network segments(NIDS)  
~ On Hosts(HIDS)  
2. Analysis Engine  
~ Analyze data collected by the sensor, determines if there is sus activity  
3. signature database  
~ Used by Analysis Engine, defines signatures of previously know attacks  
4. UI and reporting  
~ the way system interacts with users  

### HIDS
- Examine the operation of SINGLE system independently to determine of anything "of note" is going on  
- e.g. Logins/ system log files/ app log files

#### Advantages of HIDS
- Can be OS and application specific - might understand the latest attack against a certain service on a host  
- they can look at data after it's been decrypted

#### Disadvantages of HIDS
- Only protect one machine
- Use local system resources (CPU/Memory)
- Dont see whats going on for other machines
- Scalability
- could be disabled if machine is hacked

### Network Based IDS
- Entire network and all associated machines
- Focuses specifically on network traffic, in this case the sensor is sometimes called traffic collector
- e.g. SRC IP, DEST IP, Protocol, Port Numbers, Data content
- Look for DOS attack/ Port scans/ malicious content/ vulnerability tests/ tunneling/ brute force attacks
- watch the internal network for policy violations e.g. detecting instant messaging or streaming video (port number cant block)
- Should put in DMZ

### Advantages of NIDS
- Single sensor can cover whole network
- Deployment Easier
- Can see things that are happening on multiple machine , bigger picture and may see distributed attacks that a HIDS would miss

### Disadvantage of NIDS
- Data must be unencrypted for NIDS to analyze (Many protocols are encrypted)
- Switches cause problems for NIDS (port span should be implemented)
- only on the perimeter, missing things on the inside
- Must be able to handle lots of data to be effective
- Does not see whats going on a server directly 

## IDS vs IPS
- IDS - Passive device
- IPS - Active

### Analysis Engines

#### Pattern Matching 
- Signature based
- Most network attacks have distinct signatures that is data that is passed between attacker and victim
- A sign based NIDS has a adatabase of know attack signatures, and compares network traffic against this database
- Concern for sign based systems
1. pay for vendor
2. keep sign updated
3. cant deal with 0 day attacks

#### Profile Matching
- Anomaly/ Behavior/ Heuristics
- Anomaly based systems - look for changes in normal behavior
- let anomaly based system learn what normal behavior is over time e.g. creating baseline
- anomaly based system will then look for traffic types and volume that is outside of the normal behavior

##### Profile Matching Advantages
- able to detect 0 days
- able to detect behavioral changes that might not be technical attacks

##### Profile Matching Disadvantages
- Lots of False positives
- often ignored due to reason above
- requires much more skilled analyst

### Bypassing an IDS
- Evasion attack (flying under the radar)  
~ Many small attacks from different directions  
- Insertion attack (geared toward sign based systems)  
~ Adding meaningless info (without modifying the payload) to a known attack(加d垃圾落去矇混過關)  

### IDS Rules Based
- Uses expert system/ knowledge based systems
- Use a db of knowledge and an "inference engine" to try to mimic human knowledge
- Promiscuous mode
~ Network interfaces generally only look at packets specifically intended for their MAC address
~ Put network interfaces to Promiscous mode TO Accomplish sniffing, network analysis, or IDS functionality

### Honeypot
- Deployment  
~ Pseudo Flaw: Loophole purposely added to OS or application to trap intruders  
~ Sacrificial lamb system on the network  
~ Administrators hope that intruders will attack this system instead of their production systems  
~ Enticing caz many ports are open and services are running
- Enticement(誘惑) vs Entrapment(誘捕)

### Padded Cell and Vulnerability Tools
- Concept used in software prog where a "safe" environment is created for app and processes to run in (similar to VM)
- Concept used in IDS where identified intruder is moved to a "safe" environment without their knowing
- Simulated env to keep intruder happy&busy (leave production systems alone)
- A.K.A Self mutating honeypot, Tarpit

