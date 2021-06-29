# Identity and Access Management
11/06/2021 Cybrary

- IAM is the set of processes , procedures, tools,and technology necessary to oversee and manage digital identities
- Goal of IAM to provide secure and auditable access to the digital resources with an organization
- Revolves around effective management of IAAA

### Identification (I)
- Identity Proofing
- Account Provisioning/Deprovisioning (開/刪)

### Authenication (A)
- Kerberos
- RADIUS
- IAM in the Cloud

### Authorization (A)
- Access control model e.g. DAC ,MAC,RBAC , RuBAC,ABAC

### Auditing / Accountability (A)

## Identity Management 
- Controls life cycle for all accounts in a system

## Access Management
- Controls the assignment of rights/ priviledges to those accounts

## Access Controls Objectives
- IAAA
- Single Sign On
- Access Control Models
- Access Control Methods
- Access Control Administration
- Data Emanation (e.g. bluetooth)

## Access 
- Subject verb Object

## Access Controls
- Control how people interact with systems
- Logical / Physical / Administrative

## Identification
- Public info
- identification must be unique for accountability
- standard naming schemes 
- identifier should not indicate extra information about user

## Authentication
### Type 1 : something you know
- Passwords/ Passphrases/ Cognitive Password
- No less than 8 char
- change on a regular basis
- enforce password history
- prevent brute force/ dict attacks 
- prevent ease of cracking cognitive passwords
- graphic image
- enable clipping levels and respond accordingly 

### Type 2 : somthing you have
- Token Devices
~ One time password 
~ can be costly
~ simple device to implement
~ Two types : Sync / Async
#### Async / challenge response 
~ user logs in   
~ Authentication returns challenge  
~ user types challenge string into token device and press enter   
~ token devices returns a reply  
~ only specific user's token device could respond with the expected reply  
~ more complex than sync  
~ may provide better protection against sniffing

- Smart card
### smart card attack
1. Fault generation
- manipulate environmental controls and measure errors in order to reverse engineer logic
2. side channel attacks 
- measure the cards while they work
- differential power analysis (power emissions)
- electromagnetic analysis (example frequencies emitted)
3. micro probing 
- using needles to vibrations to remove outer protection on cards circuits , then tap into ROMS if possible or die ROMS to read data

- memory card
- hardware key
- Cryptographic key
- certificate
- cookies

### Type 3 : something you are
- Biometrics
~ Static : not significantly change over time e.g. finger print , hand geometry , iris , retina
~ Dynamic : Based on behavioral traits e.g voice , gait , signature , keyboard cadence
- Biometrics Concerns
#### Accuracy
~ Type I Error: False rejection
~ Type II error: False acceptance
~ As FRR goes down , FAR goes up , vice versa
~ Level which two meet = CER ( Crossover error rate). Lower CER = more accurate
~ Iris Scans = most accurate

### Type 4 : something you do

## Authorization
- Ensure someone authenticaed is allowed access toresource
- preventative control
- race conditions would try to cause authorization to happen before authentication
### Authorization principals
- No access unless explicity give you WHICH implicity denied access
- need to know 
- content based
### Authorization Creep
- Role based control > identity based
- subjects stays in an environment over time , their permissions accumlate even after they are no longer needed
- SOX requires yearly auditing

## Auditing 
- Logging / reviewing accesses to objects

## Kerberos
- network authenication protocol from MIT's project athena
- Ensure authentication secuirty in an insecure environemnt
- used windows 2000+ / some Unix
- allows for single sign on
- never transfers passwords
- symmetric encryption -> verify identifications
- avoid replay attacks

### Kerberos components
- Authentication Server : allows authentication of the user and issues a TGT
- Ticket Granting Service : after receiving TGT from Servver , TGS issues a ticker for a particular user to access a particular sefrvice
- Key Distribution Center : runs TGS and AS
- Ticket : means of distributing session key
- Principles : Users/ applications / services
- Kerberos software 
- Main Goal : user needs to authenitcate without sending password across the network to prove knowledge of the password
