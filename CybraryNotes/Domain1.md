# Agenda Information Security and Risk Management
20/06/2021 Cybrary
- DR: https://acsense.com/blog/disaster-recovery-testing-a-comprehensive-guide/
- ![image](https://github.com/HoiDam/Markdown_CISSP/assets/66233626/47d27c3b-3e1e-4c11-80a5-dd3dd9724b4f)


## Information Security Program
- Provides the means for achieving strategy
### Policies , Standards, Procedures
#### Standards
~ Mandatory   
~ Created to support policy while providing details  
~ Reinforces policy and provides direction  
~ Can be internal or external  

#### Guidelines
~ Not Mandatory  
~ Suggestive in Nature  
~ Recommended actions and guides to users
~ "Best Practices"

#### Baselines
~ Mandatory  
~ Minimum acceptable security configuration for a system or process  
~ Purpose of security classification is to determine and assign the necessary baseline to protect data

#### Types of Policy
##### Corporate policy  
##### System specific policy  
##### Issue Specific policy
~ Change Management Policy  
~ Acceptable Use Policy  
~ Privacy  
~ Data/System Ownership  
~ Separation of Duties  
~ Mandatory Vacations  
~ Job rotation  
~ Least privilege  
~ Need to know  
~ Dual Control / M of N Control

### Roles and Responsibilities
- SLA's Service Level Agreements / Outsourcing
- Data Classification / Security
- Certification and Accreditation
- Auditing

#### Senior Management's Responsibilities
~ Provide oversight  
~ Provide funding / support  
~ Ensure testing  
~ Prioritize business functions  
~ Establish a common vision / strategy / framework for the enterprise  
~ "Sign off" on policy , Business Impact Avoidance  and other organizational documents  

#### Steering Committee
~ Oversight of information security program  
~ acts as Liaison between Management , business , information technology , and information security   
~ assess and incorporate results of the risk assessment activity into decision-making process  
~ ensures all stakeholder interests are addressed  
~ Oversees compliance activities

#### Chieft Information Security Officer
~ Strategic Planning   
~ Policy Development  
~ Technology Assessments  
~ Process Improvement  
~ Acquisitions  
~ Capital Planning  
~ Security  

#### Infomation Security Manager
~ Functional manager , "how" based  
~ Play a leading role in introducing an appropriate structured methodology  
~ act as major consultants in support of senior management  

#### Business Managers
~ Responsible for business operations  
~ Provide direction to ensure security is implemented in such a way as to meet business objectives  
~ Responsible for security enforcement and direction  
~ Responsible for day to day monitoring / reporting / disciplinary actions / compliance  

#### Security Practitioners 
~ Responsible for proper implementaion of security requirements in their IT systems  
~ Support or use the risk management process to identify and assess new potential risk and implemnt new security controls as needed to safeguard their IT system

#### Auditors
~ Objective Evaluation of controls and policies to ensure that ehy are being implemented and are effective  
~ if internal auditing is in place , auditors should not report to the head of a business unit , but rather to the Chief operation officer or some other entity without direct stake in result  
~ auditors document and do not modify  

#### Securiity Trainers
~ Must understand the risk management process   
~ Develop appropriate training materials  
~ Conduct security trainings and awareness programs catered to roles within the organization  
~ Incorporate risk assessment into training programs to educate the end users  
~ Encourage uses to report violations  

## Information Security Risk Management
- process of managing risks associated with the use of information technology

### Risk Definitions
- assets: antyhing value to company
- vulnerbility: weakness , absence of safeguard
- threat: something could pose loss to all or part of an asset
- threat agent: what carries out the attack
- exploit: an instance of compromise
- risk: probability of a threat materializing 
- controls: physical , administrative and technical protections (safeguards/countermeasure)
- total risk: risk that exists before any control is implemented
- residual risk: left over risk after appling a control
- secondary risk: when one risk response triggers another risk event
- incident: a risk event that has transpired/happened

### Identification
- Identify assets -> identify threats -> identify existing controls ->
 identify -vulnerabilities -> identify consequences -- feed into -> risk assessment process

- Methods to identify risk  
~ Sources of risk documentation  
~ Audit reports  
~ Interviews with SMEs Public media  
~ Annual reports  
~ Press releases  
~ Vulnerability assessments and penetration tests  
~ Business continuity and disaster recovery plans  
~ Interviews and workshops  
~ Threat intelligence services   

- Alignment with Business Goals and Objectives  
~ First and most important step for a CISM is to understand business . Review organizational vision and strategy   
~ Look beyond IT - Risk is measured by the impact the risk has on the business, not on a particular system  
~ In order for risk to be integrated into the enterprise, senior management must be supportive and involved  
~~ management funds and support the risk management process we will have what we need to be successful  
~~ good metrics = have attainable objectvies help us accomplish our goals  
~~ good communication and transparency help us make risk-aware business decisions

- Organizational structure and impact on risk
~ risk context  
~ risk management approach should be enterprise wide and a common framework should be shared across all department  
~ three lines of defense  
~ RACI Charts can be used to indicate responsibilities   
~ 1st line business unit -> 2nd line risk and compliance -> 3rd line audit  

### Assessment
- Qualitative  
~ Subjective analysis to help prioritize probability and impact of risk events  
~ May use Delphi Technique  
- Quantitative  
~ Providing a dollar value to a particular risk event    
~ Much more sophisticated in nature, a quantitative analysis if much more difficult and requires a special skill set  
~ Business decisions are made on a quantitative analysis  
~ Can't exist on its own. Quantitative analysis depends on qualitative information
- Qualitative Assessments  
~ Assess risks based on subjective input  
~ Uses terms like high, medium, low   
~ Inexpensive, and quick way to begin the prioritization and ranking of risks
- Quantitative Analysis Formulas and Terms  
~ Asset Value: Dollar figure that represents what the asset is worth  
~ Exposure Factor: The percentage of loss that is expected to result in the manifestation of a particular risk event  
~ Single Loss Expectancy: Dollar figure that represents the cost of a single occurrence of a threat instance  
~ Annual Rate of Occurrence: How often the threat is expected to materialize  
~ Annual Loss Expectancy: Cost per year as a result of the threat  
~ Total Cost of Owner: the total cost of implementing a safeguard. Often in addition to initial costs, there are ongoing maintenance fees as well  
~ Return on Investment: Amount of money saved by implementation of a safeguard. Sometimes referred to as the value of the safeguard/control.  


### Mitigation
- Steps for Quantitative Analysis   
~ AV -> EF -> SLE -> ARO -> ALE -> Perform cost/benefit analysis of countermeasures

- Loop
~ IT Risk Identification -> IT Risk Assessment -> Risk response and mitigation -> Risk and Control Monitoring and Reporting -> IT...

- Risk assessment : Dicatate risk response  
~ Reduce  
~ Avoidance  
~ Transfer  
~ Accept  
~ Rejection  

- Risk reduction:   
~ action is taken to lessen frequencey/ impact of a risk  
~ may require the use of several controls until it reaches levels of risk acceptance or risk tolerance  

- Examples  
~ strengthening overall risk management practices, e.g. implementing sufficiently mature risk management processes  
~ deploying new technical, management or operational controls that reduce either the likelihood or impact of and adverse event  
~ installing a new access control system  
~ implementing polices or operational procedures  
~ developing an effective incident response and business continuity plan  
~ using compensating controls  

- Ulitmate risk reduction = avoidance

- Risk Transference :  
~ decision to reduce loss through sharing that risk with another organization  
~ Service Level Agreements and contracts establish the degree of transference  
~ Cant transfer liability  

- Risk Acceptance examples :  
~ Provides no active mitigation  
~ based on a cost/ benefit analysis , it is determined the cost of the control is less than the potential for loss   
~ sometimes acceptance is the only choice  
~ risk acceptance still includes due diligence, and can still be used to indicate good business decisions were made   
~ level of risk and impact is always changing, so reglular reviews are needed

### Monitoring
- Risk Monitoring and Reporting  
~ Risk response designed and implemented based on a risk assessment that was conducted at a single point in time   
~ Because of changing nature of risk and associated controls, ongoing monitoring is an essential step of the risk management life cycle   
~ controls can become less effective    
~ operational environment may change   
~ new threats , tech , vulnerabilities may emerge  

- Key Risk Indicators   
~ Provide early warning  
~ Provide backward-looking view on risk events  
~ Enable documentation and analysis of trends  
~ Increase the likelihood of achieving strategic objectives  
~ Assist in optimizing risk governance

## Legal Considerations

### - Who is at fault
#### Failure of management to execute Due Care and/or Due Diligence can be termed negligence (Culpable neligence)
#### Prudent Man Rule
- Perform duties that prudent people would exercise in similar circumstances    
~ Example: Due Diligence, researching industry standards and best practices  
~ Due Care setting and enforcing policy to bring organization into compliance  
#### Downstream Libilities
#### Integrated technology with other companies can extend one's responsibility outside the normal bounds  

### - Criminal Law
- Beyond a reasonable doubt : can be difficult to meet this burden of proof in computer-related crimes
- Penalties : Financial, Jail-time, death  
~ Felonies(重罪) : More serious of the. Often penalty results in incaraceration of at least a year  
~ Misdemeanors(輕罪) : Normally the less serious of the two with fines or jail-time of less than one year  
- Goal of criminal penalties : Punishment, Deterrence

### - Administrative (Regulatory) Law
- Defines standards of performance and regulates conduct for specific  
~ Banking (Basel II)   
~ Energy (EPAct) of 2005   
~ Health Care (HIPAA)  
- Burden of Proof = "More likely than not"
- Penalties consist of financial or imprisonment

### Intellectual Property
- Intellectual Property Law  
~ Protecting products of the mind  
~ Company must take steps to protect resources covered by these laws or these laws may not protect them   
- Main international organization run by the UN is the World Intellectual Property Organization   
- Licensing is the most prevalent violation, followed by plagiarism, piracy and corporate espionage

## Knowledge Transfer
- Awareness, Training, Education
- Goal of Knowledge transfer is to modify employee behaviour  

### Knowledge transfer rules
- Security Awareness Training  
~ Employees cannot and will not follow the directives and procedures if they do not know about them   
~ Employees must know expectations and ramification
~ Employees recognition award program  
~ Part of due care  
~ Administrative control

--- 

## Business Continuity Planning
- Focuses on sustaning operations and protecting the viability of the business following a disaster , until normal business conditions can be restored.
- BCP ~= unbrella

### Categories of Disruptions
- Non-disaster: Inconvenience. e.g. Hard drive failure  
~ Disruption of service  
~ Device malfunction   
- Emergency/Crisis  
~ Urgent, potential for loss of life / property
- Disaster  
~ entire facilitiy unusable for a day or longer  
- Catastrophe  
~ Destroys facility

#### ~ Company should understand and prepared for each category

#### ~ Anyone can declare an emergency
#### ~ ONLY BCP coordionator can declare disaster (failover act)

### BCP frameworks
- Standards help solve issues of inconsistency in terms, definitions and documents (within the organization)  
- Following institutes will provide guidance on BCP / DRP:    
~ Disaster Recovery Institute international  
~ NIST 800-34 rev1   
~ ISO 27031  
~ ISC2.org four processes of business continuity

#### 7 Phases of Business Continuity Plan (NIST)
- BCP policy -> Business Impact analysis -> ID Preventative controls -> Create contingency strategies ---into 3 componenet loop---> develop on IS contingency plan -> testing , training and exercises -> maintenance

#### ISC four business continuity planning processes
1. Project scope and planning
2. Business impact assessment 
3. Continuity planning
4. Approval and implementation

##### 1 Project scope and planing
- Acquire BCP Policy Statement from senior management  
- Business Organization Anaylsis: Structured analysis of the business organizational assets  
- BCP team creation, including Project Manager. Should be cross-functional team, including representation of senior management  
- An assessment of the resources available and commitment to support BCP Process from Senior Management  
- An analysis of the legal and regulatory landscape that gov an organizations response to a catastrophic event

###### BCP team selection
- Representatives from each organization departments responsible for the core services perfromed by the business
- Representatives from key support departments identified by the organizational analysis
- IT representatives with technical expertise in areas covered by BCP
- Security representatives with knowledge of BCP process
- Legal representatives familiar with corporate legal , regulartory and contractual responsibilities
- Represtatives from senior management

###### Legal and Regulatory Compliance
- Senior management has the ultimate leagl responsibility 
- held responsible and liable under various laws and regulations
- sued by their stockholders if not mananing with due diligence and due care
- sued by employees or families in the event of injury or loss of life

##### 2 Business Impact Assessment
- Identifies and prioritizes all business processes/resources based on criticality
- Risk identification (interal vs 3rd party , probability and impact)
- Categorizes processes/resources based on criticality
- Defines quantitative metrics to assist with prioritizing recovery focus
- BIA will help prioritize recovery priorites

###### Identify priorities
- Create an in-depth list of business processes and their impact on the organization  
- Often delegated to individual departments for accuracy and buy-in  
- Criticality is driven by the amount of loss the organization will suffer if the resources is unavailable  
~ Maximum Toleratble Downtime/ Outage: Lonest time the function can be inoperable before causing a loss to senior management that is unacceptable   
~ Recovery time objective: This is amount of time in which you think you can feasibly recover the function is the event of disruption  
~ Recovery Point Objective: Tolerance for data loss  

##### 3 Continuity Planning
- Strategy development 
- Provisions and processes
- Plan approval
- Plan implementation
- Training and education

###### Strategy development
- Examines the BIA for metrics and map controls to meet objectives
- Determine appropriate response: [Reduce,Assign/Transfer,Accept,Reject]
- Some risks will have to be accepted(based on cost/benefit) while other require a more active strategy

###### Provisions and Processes
- BCP designs the specific procedures necessary to mitigate risks to level that is acceptable to senior management
- 3 assets :   
~ People (1st prioirty)  
~ Buildings/Facilties (Hardening provisions)  
~ Infrastructure (Systems,e.g. failover)

###### Facility Recovery
- Dedicated site owned or operated by the organization
- Reciprocal agrement or memorandum of agreement with an internal or external entity
- commercially leased faciltiy [Hot,Warm,Cold]
- MOAs or SLAs should be obtained from the provier

###### Infrastructure
- supports critical elements of the business
- High availbailty [redundancy,resilitency,fault tolerance]
- hardened systems

##### 4 Plan approval and implementation
- Plan approval  
~ if possible , CEO should endorse plan  , otherwise another senior officer  
~ indicates dedication of the business to the process of business continuity planning
- Plan implementation   
~ Create implementation guide/ schedule  
~ Deploy resources  
~ Supervise maintenance of plan
- Train and educate employees   
~ distribute plan on need to know basis  
~ everyone should get at least an overview


### Business Continuity Plan Sub-Plans
- 3 main purpose : 
#### Protect
~ Crisis Communication plan   
~~ Disseminate necessary information  
~ occupant emergency plan   
~~ provide coordinated procedures for minimizing loss of life or injury + protecting property damage in response to phtsical threat  

#### Recover
~ Business recovery plan  
~~ Provde procedures for recovering business operations immediately following a disaster  
~ Disaster recovery plan   
~~ provide detailed procedures to facilitate recovery of capabilityies at an alternative  
~ Continuity of support plan / IT contingency plan  
~~ Provide procedures and capabilities for recovering a major application or general support system  
~ Cyber incident response plan  
~~ provide strategies to detect, respond to and limit consequences of malicious cyber incident  
~~ focuses on information security responses to incidents affecting systems and networks

#### Sustain
~ Continuity of operations plan  
~~ provide procedures and capabilities to sustain an organization essential strategic functions ata an alternate site UP TO 30 days  
~~ Used in US gov  
~~ to adddress subset of an organization's missions that are deemed most critical , usually written at headquarters level , not IT focused  

#### Roles and Responsbilities
- Senior Executive management  
~ Consitent support and final approval of plans  
~ Setting the business continuity policy   
~ Priorizing critcal business functions  
~ Allocating sufficient resources and personnel  
~ Providing oversight for and approving the BCP  
~ Directing and reviewing test results   
~ Ensuring maintenacne of a current plan  

- Senior functional managemnet  
~ develop and document maintenance and testing strategy  
~ identify and prioritze mission-critical systems  
~ monitor progres of plan development and execution  
~ ensure periodic tests  
~ create the various teams necessary to execute the plans

- BCP steering commitee  
~ Conduct the BIA  
~ coordinate with department representatives  
~ include [business units , senior manegement, it department, security department, communications department, legal department]

- DRP teams  
~ Rescue : Responsible for dealing with the immediacy of disaster - employee evacuation   
~ Recovery : Responsible for getting alternate facility up and running and restoring the most critcal services first  
~ Salvage : Responsible for return of operations to original or permanent facility (reconstitution)  

### Developing the teams 
- Management should appoint members  
- Each member must understand the goals of the plan and be familiar with department they responsible for  
- Agreed upon prior to the event :  
~ Who will talk to media , customers , shareholders   
~ Who will setup alternative communcication methods  
~ Who will setup the offsite facility  
~ Established agreements with off-site facilities should be in place  
~ Who will work on the primary facility

## Disaster Recovery Planning
- Minimize the effect of disaster and to take the necessary steps to ensure the resource, personnel and business processes are able to resume operations in a timely manner  
- Deals with the immediate aftermath of the disaster , and is often IT focused  

## Types of Tests 
### Checklist Test
- Copies of plan distributed to different departments 
- Functional managers review 
### Structured wall-through (table top) Test
- Representative from each department go over the plan
### Simulation Test
- Going through a disaster scenario
- Continues up to the actual relocation to an offsite facility
### Parallel Test
- Systems moved to alternate site, and processing takes place there
### Full-Interruption Test  
- Original site shut down   
- All of processing moved to offsite facility  

## Post-incident review
- After a test or disaster has taken place  
~ Focus on how to improve  
~ What should have happened  
~ Not who's fault it was; this is not productive  

## Maintaining the BCP
- Keeping plan in date  
~ Make it a part of business meetings and decisions  
~ Centralize responsibility for updates  
~ Part of job description  
~ Personnel evaluations  
~ Report regularly  
~ Audits  
~ As plans get revised, original copies should be retrieved and destroyed  

### 7 Security Operations Objectives
- Incident Response, Evidence Collection and Forensics
- Fault tolerance and recovery strategies  
- Business Continuity and Disaster Recovery 

