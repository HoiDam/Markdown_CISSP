# Agenda Information Security and Risk Management
20/06/2021 Cybrary

## Asset Security
- Asset Value and classification
- Data Protection
- Data Redundancy
- Secure Data Disposal

## Asset value
- Value to organization
- loss if compromised
- legislative drivers
- liabilities
- value to competitors
- acquisition costs

## Data Classification
- Development of sensitivity labels for data and assignment of those labels for the purpose of configuring baseline security based on value of data
- Cost: Value of Data
- Classify: Criteria for Classification
- Controls: Determining the baseline security configuration for each
- Data Owner: Determines the classification of data
- Data Cusodian: Maintains the data

### Gov / Military Level of data classification
1. Top Secret: Grave damage to national security e.g. blueprints of wartime weapons, spy satelite information
2. Secret: Serious Damage to national security e.g. Troop movements
3. Confidential: Data exempt from freedom of information act e.g. cause damage to national security
4. Sensitive but unclassified: Minor Secret e.g. personnel information
5. Unclassified: Not sensitive e.g. recruiting

### Private Sector Level of data classification
1. Confidential: Company Secrets e.g. Serious implications if info is released
2. Private: Personal information of employees within an organization
3. Sensitive: Financial information e.g. forecast, project related information
4. Public: Disclosure is not necessarily welcome e.g. inpact would not have adverse effect

### Sensitivity
- amount of damage that would be done should / should the information be disclosed

### Criticality
- The time sensitivity of the data. Usually driven by the understanding of how much revenue a specific asset generates and without that asset there will be lose of revenue

## Data Protection
### Location and Access
- Though the data lifecycle model doesnot specify requirements for location and access, these two factors are essentail in planning the implementation for access controls

#### Location
- Jurisdiction
- Audit
- Threat landscape
- What actors have access to the data
- does data move betweeen locations and how?

#### Access
- Who have access 
- what controls are in place
- what devices can be used

### State of data
- At rest: File System encryptions, EFS, TPM
- In process: 
- In Transition: SSL/TLS

## System hardening and baselining
- remove unnecessary services
- install the lastest services packs and patches
- renaming default accounts
- changing default settings
- enabling security config  e.g. auditing, firewalls, updates, etc
- *Physical security*

## Threats to data storage
- Unauthorized usage/access  
~ Strong authentication  
~ Encryption  
~ Obfuscation, anonymization, tokenization,. masking  
~ organizational policies / layered defense  
- Liability due to noncompliance   
~ Due care and due diligence  
~ SLAs  
- DOS / DDOS    
~ Redundancy  
~ Data Dispersion  
- Corruption, modification, destruction of data  
~ Hashes/ Digitally signed files
- Data leakage and breaches  
~ DLP  
- Theft or accidental media loss  
~ TPM  
- Malware attack  
~ Anti-malware
- improper treatment or sanitization of data at end of lifecycle 

### Data security in the cloud
- Protecting data moving to and within the cloud e.g. SSL/TLS/IPSec
- Protecting data in the cloud e.g. encrpytion
- Detection of data migration to the cloud e.g. DAM/DLP
- Data dispersion: data is replicated in multiple phyiscal locations across your cloud (Higher availability)
- Data fragmentation involves splitting a data set into smaller fragments(shards), distributing them across a large number of machines


### Masking, Obfuscation, Anonymization, Tokenization
- Obfusaction: process of hiding, replacing or omitting sensitive information
- Masking: process of using specific charaters to hide certain parts of specific dataset e.g. displaying asterisks for all but last 4 digits of SSN
- Data anonymization: process of either encrypting or removing personally identiable infromation from data sets, so people describe remain anonymous
- Tokeniztion: Public cloud service can be integrated and paired with a private cloud that stores sensitive data. Data sent to pubic cloud is altered and contains a reference to data residing in the private cloud

### Data rights management
- DRM or Inforamtion Rights Management adds an extra layer of access control on the top of data object/document and provides granularity flowing down to printing, saving, copying, other options
- Useful for protecting sensitive organization content and intellectual property
- ACLs are embedded into the file, its agnostic to the location of data. IRM will travel with the file(persistent)
- Dynamic policy control allows the owner to define and change user permissions and recall or expire content even after distribution

## Data Redundancy

### Backups and Archives
- keep data retention requirements 
- select backup methods appropriate with business objectives
- use numbers from BIA: RTO/RPO
- remember secuirty of backup media
- backups: copies of current data, intended for fault tolerance
- archives: data conisdered to be out of use but perserved in the event that it is required at a later time

### Data Protection policies: Retention
- Established protocol for keeping information for operational or regulatory compliance needs
- Cloud considerations:
1. legal regulatory and standards requirements must be well documented and agreed upon
2. Data mapping should map all relevant data in order to understand formats, data types and data locations
3. Data classification based on locations, compliance requirements, ownership and business usage
4. Each category's procedures should be followed based on appropritate policy that governs the data type

### Data archiving
- Process of identifying and moving inactive data out of current productions systems and into specialized long-term archival storage systems
- Consideration : Encryption, Monitoring, Granular retrieval, Electronic discovery, Backup and recovery, media type, restoration procedures

## Secure Data Disposal
### Sanitizing media
- what types(optical non rewritable, magetic) and size (TB,MB) need to be sanitized
- Confidentialiy of data ?
- sanitization process conduct within organization or outsourced ?
- anticipated volume of media to be sanitized by type of media ?
- availability of sanitization equipment and tools ?

### Media Sanitation
- Disposal, Clearing, Purging, Destroying   

| Data | Media |
| --- | ----------- |
| Magnetic optical | Hard copy |
| Electrical | Electronic copy |

### Removing Data remnants
- Disposal   
~ Clearing, overwriting: renders data in accessible  
~ Purging, degaussing: renders media unusable  
~ Destruction, Physical destruction: irreversible by all known techniques

