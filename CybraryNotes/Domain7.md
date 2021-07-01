# Security Incident Response
30/06/2021 Cybrary

- Event: A change in state
- Incident: Series of events that has a negative impact on the company and its security
- Incident response focuses on containing the damage of an attack and restoring normal operations
- Investigations focuses on gathering evidence of an attack with the goal of prosecuting the attack

## Framework include:
### 1.Response capability 
- Incident response  
~ Corporate incident response polics, procedures and guidelines should be in place  
~ Legal, HR, Executive management, key business units must be involved  
~ If handling in-house, an incident response team must be in plcae  
~ List of outside agencies and resources to contact or report to Computer Emergency Response Team(CERT)  
~ Steps on how to secure and preservev evidence   
~ Steps on how to search for evidence   
~ List of items that should be included on the report    
~ A list that indicates how the different systems should be treated in this type of situation   

### 2. Incident response and handling 
- Triage(v): [Detection, Identification, Notification]
- Investigations
- Containment
- Analysis and Tracking

### 3. Recovery and feedback
- Recovery and Repair: Restoration of the system to operations     
~ Not practical to restore to original status(since got attacked with low security)  
- Provide Feedback: Document (important step)

## Computer Forensics (鑒證)
- = Discipline of using proven methods toward the collection, preservation, validation, identification, analysis, interpretation, documentation, presentation of digital evidence  
- IOCE and SWGDE: Two entities that provide forensics guidelines and priniciples as follows   
~ All forensic principles must be applied to digital evidence  
~ Evidence should not be altered as a result of collection  
~ Must be trained person to access the digital evidence  
~ All activity relating the seizure, access, storage, transfer of digital evidence must be fully documented and available for review    
~ An individual is responsible for actions affecting digital evidence while that evidence is in their possession   
~ Any entity responsible for seizing, accessing, storing, transferring digital evidence is resposbile for compliance with these principles    

## Five Rules of Digital Evidence
- Be authentic(確鑿)  
- Be accurate
- Be complete
- Be Convincing 
- Be admissible(受理)

## Forensics investigation process

### Identification
- Locard's principle of exchange: When crime is committed, attacker takes something and leaves something behind. e.g. DNA, knowledge, Behaviour  
- Help us identify aspects of responsible party  

### Perservation
- Chain of custody ***   
~ Must be well documented    
~ History of how evidence was [collected, analyzed, transported, preserved]    
~ Necessary because digital evidence can be manipulated so easily    
- Hashing algorithms are used to show the integrity of the eveidence has not been modified by the investigation process  

### Collection
- Minimize handling/ corruption of evidence e.g. (doing 3 hashing on copying the hdd)  
- Keep detailed logs of your actions  
- Comply with the 5 rules of digital evidence  
- Do not exceed your knowledge
- Follow organization's secuirty policy
- Capture an accurate image of the system
- Ensure actions are repeatable
- Work Fast(digital evidence may have short lifespan)
- Work from volatile to persistent evidence
- Do not run programs or open any files on the infected system until a forensic copy
- Forth Amendment proteccts aginst illegal search and seizure  

#### Step to evidence collection
1. Photograph area, record what is on the screen
2. Dump contents from memory
3. Power down system
4. Photograph inside of system
5. Label each piece of evidence
6. Record who collected what and how
7. Have legal department and possbily human resources involved

#### Exceptions to previous statement
- Private citizen not subject to fourth amendment rules unless acting as a police agent
- Citizen may be subject to restrictions of Electronic Communications Privacy Act

#### Computer evidence can be obtained by law enforcement only through
- Subpoena 
- Search warrent
- Voluntary consent 
- Exigent Circumstances

### Examination
- Look for signatures of known attacks
- Review audit logs
- Hidden data recovery

### Analysis
- Primary image (original) vs Working image (copy)
- Working image should be bit by bit copy from original
- Both copies must be hashed + working copy should be write-protected
- root cause?
- wt files were altered/installed?
- wt communications channels were opened?

### Presentation 
- Interpreting the results of the investigation and presenting the findings in an appropriate format
- Documentation
- Expert testimony(見證)

### Decision
- The result of investigation? [Suspect? /Corrective Action?]
- Dont fire ppl now

## Evidence
### Controlling the crime scene
- The scene of the crime should be immediately secured with only authorized individuals allowed in 
- Document (Integrity of the evidence could be called in to question if not proper document)
- Logs should be kept detailed all activities

### Evidence Types
- Direct Evidence: can prove a fact by itself and does not need backup information/ Information provided based on 5 sense of witness
- Real Evidence: Physical evidence. The objects themselves that are used in a crime
- Best Evidence: Most reliable e.g. signed contract
- Secondary: Not strong enough to stand alone, but can suppport other evidence e.g. Expert Opinion
- Corroborative Evidence: Support evidence. Backs up other information. Cant stand alone
- Circumstantial: Proves one fact which can be used to reasonably to suggest another. Cant stand alone 
- Hearsay: 2nd hand oral or written. Usually not admissible
- Demonstrative: Presentation based. e.g. photos of crime scene, x-rays, diagrams

#### Who should do investigation?
- Law Enforcement  
~ Available skilled resources for this investigation?  
~ Forth amendment, jurisdiction, miranda, privacy issues   
~ Information dissemination is not controlled

#### Suspect's Action and Intent
- Enticement OKAY e.g. honeypot
- Entrapment NO (illegal/not ethical)

## Fault Management
### Spares
- Redundant hardware
- Available in the event that primary device becomes unusable
- Often associated with hard drives 
- Hot, warm, cold swappable devices
- SLAs
- MTBF /MTTR

### RAID
- RAID-0: Disk striping provides no redundancy or fault tolerance but provides performance improvements for read/write functions
- RAID-1(Most expensive): Disk Mirroring-Provides redundancy but is often considered to be the least efficient usage of space
- RAID-5 Disk striping with parity: Fault tolerance + speed

### Redundant Servers
- Primary server mirrors data to secondary server     
~ primary fails it rollover to secondary    
~ server fault tolerance  

### Clustering
- Group of servers that are managed as a single system 
- Higher availability, Greater scalability, easier to manage instead of instead of individual systems  
- May provide redundancy, load balancing, or both    
~ Active/Passive     
~ Active/Active   
- Cluster looks like google server the user (server farm)  

### Uninteruptible Power Supply
- Issue to consider  
~ Size of load UPS can support    
~ How long it can support this load(battery duration)    
~ Speed the UPS takes on the load when the primary power sources fails   
~ Physical space required  
- Desirable Features  
~ Long battery life   
~ Remote diagnostic software   
~ EMI/RFI filters to prevent data errors caused by electrical noise    
~ High MTBF values   
~ Allow for automatic shudown of system    

## Backups
- Backup software and having backup hardware is a large part of network availability  
- Important to be able to restore data    
~ If a hard drive fails  
~ A disaster take place   
~ Some types of software corruption  

### Full backup  
- Archive bit is reset  

### Incremental backup  
- Backs up all filese that have been modified since last backup  
- Archive bit is reset  
 
### Differential backup  
- Backs up all filese that have been modified since last FULL backup   
- Archive bit is NOT reset  

### Copy backup  
- Same as full bakcup but archive bit is not reset  
- Use before upgrades, or system maintenance
 

### Backup Issues
- Identify what needs to be backed up first
- Media Rotation scheme  
~ Grandfather, Father, Son  
~ Tower of Hanoi  
- Backup schedule needs to be developed  
- If resoring a backup after a compromise, ensure tah backup material does not contain same vulnerabilities that were exploited 

### Redundancy of Staff
- Elminate single point of failure
- Cross Training (Train your people)
- Job rotation
- Mandatory vacations
- Training and education
