# Security engineering and architecture
09/06/2021 Cybrary

## Part 1 
- Content
1. Cyptography throughout history
2. Security Services provided by cryptography
3. Definitions and terms
4. Symmetric Cryptography
5. Asymmetric Cryptography
6. Hybrid Cryptography
7. Integrity through hashing , MACs & digital sign
8. Public key infra
9. IPSec
10. Attacks on Crpyto

### Cyptography throughout history
- Caseser Cipher
~ Simply Shift the character e.g. A=D  
- Scytale  
~ Spartans   
~ Wrapped tape around a rod  
~ Diameter of rod = key  
- Vignere
~ first polyalphabetic cipher  
- Cyptography in warfare
~ enigma machine/purple machine  
~ Germans/Japanese WWII  
- Vernam Cipher  
~ one time pad  
~ only mathematically unbreakable form of cryptography  
~ Key must be used only once
~ Pad length MUST message length
~ Key pad is unpredictable
~ Key pad must delivered & stored securely

### Security Services provided by Cryptography
- Privacy
~ Prevents unauthorized disclosure of info
- Authenticity 
~ Verifies the claimed identity
- Integrity 
~ Detects modification or corruption
- Non-Repudiation
~ Combine auth+integ . Sender cant dispute

#### Definitions + Concepts
~ Plain Txt + Initialization Vector + Algo(Cipher) + Key = Cipher Txt
- Initialization vector
~ different seed

#### Elements Of Cryptography
- Algo:  
- [x] Confusion 掩蓋明文與密文之間的關係
- [x] Diffusion 明文中任何一點小更動都會使得密文有很大的差異
- [x] Avalanche
- [x] Permutations
- [x] Open - Kerchhoff's principle 即使密碼系統的任何細節已為人悉知，只要密匙（key，又稱金鑰或密鑰）未洩漏，它也應是安全的。e.g. linux source code is open
- Key:  
- [x] Long
- [x] Random
- [x] Secret

### Crypto Elements

#### Symmetric
- Stream e.g. RC-4
- Block e.g. AES/3DES

#### Asymmetric
- Discrete Logarithms e.g. El Gamal , Diffie Hellman , ECC
- Factoriazation e.g. RSA

### Principles of Secure Desgin
- Security requirements for info system(security policy)
- Security Model (framework + math model)
- System Architecture (overall design e.g. hardware , os , app , networks)

#### Security Models
- State Machine Model
~ States: Startup , Function , Shutdown    
~ Startup is weak caz not much function is up and rookit can get in
~ Have to secure 3 ALL states

- *** Bell-LaPadula Model
~ By David Elloit Bell / Len LaPaDuLa (US Government)  
~ Focues on data dconfidentiality + access to classfied info  
~ Formal Model developed for DoD multilevel  
~ Divides entities in info sys into Subjects / Objects  
~ Model is built on concept of State Machine Model  
##### 3 Rules to enforce confidentially
- Simple Security Property
~ No read up  
- * Security Property
~ No write down  
- Strong * Property
~ No read/write up or down (stay where you are)   

- *** Biba Integrity Model
~ By Ken biba on set of access control rules ensure Integrity  
~ No subject can depend on object of lesser integrity  
~ hierachical lattice of integrity levels
~ authorized users must perform correct + safe procedures to protect data integrity  
##### 3 Rules to enforce integrity
- Simple integrity axiom  
~ No read down (dont trust lower integrity level stuff = dumb)  
- * Integrity Property  
~ No write up (cant override something smarter than you)  
- Invocation Property  
~  No read / write above

- Clark-Wilson
~ Keep user out of your stuff prevent them breaking it  
E.g amazon why dont let you access DB -> Caz you will break it + only front end can let you use  
~ Enforces well-formed transactions through the use of access triple:  
~ user -> transformation procedure -> Constrained Data Item  
##### 3 integrity goals (Separation of duties)
- Prevents unauthorized users from making modifications  
- Prevents authorized users from making improper modifications  
- Maintain internal+external consistency -> reinforces separation of duties

- Commercial Models: Brewer-Nash Model
~ a.k.a. Chinese Wall  
~ Developed to combat conflict of interest in db hhousing competitor information  
~ in 1989 to ensure fair competition  
~ defines a wall and set rules ensure no subject access objects on the other side of the wall  
~way separating competitors data within same db  

- Information Flow Model
~ data compartmentalized based on classifcation and need to know
~ seeks to elminate covert channels  
~ ensure info flows from low security level to high , vice versa.
~ whatever component directly affects the flow of info must dominatet all components involved with the flow of info

- Non-interference Model
~ Ensure higher level actions does not interfere action with lower level  
~ Goal : protect state of an entity of lower security level so data does not pass through covert or timing channels

- Lattice Model
~ upper bound is value that defines the least level of object access rights granted to a subject
~ Goal: protect confidentiality of an object and only allow access by an authorized subject

#### Security Architecture
- Computer architecture
~ Program = An Application  
~ Process = Program loaded into memory  
~ Thread = Each individual instruction within a process  
~ Multiprogramming/Multitasking = ?  
~ Multiprocessing = more than one CPU   
~ Multi Threading =   
~ Operating system architecture    
~ Process Activity  
~ Memory Management 
~ Memory Types - RAM , ROM ,etc
~ Virtual Memory  
##### CPU Modes & Protection Rings
~ Security mechanism creating boundaries between various processes ensure them do not affect each other
~ Ring 0 - Operating System Kernal    
~ Ring 1 - Remaining parts of OS  
~ Ring 2 - Operating system and I/O drivers and OS utilites   
~ Ring 3 - App/User activity  

#### System architecture 
- Defined subset of subjects and objects  
- Trusted Computing Base  
- Security Perimeter  
- Reference Monitor (laws)  
- Security Kernel (police) -: enforces refernce monitor concept  
~ Kernel facilitate isolation of process . 
~ kernel must be invoked at every access attempt
~ kernel must be small enough to be tested and verified in comprehensive manner  
- Security Policy = a set of rules on how resources are managed in system  
- Least Priviledge - one process has no more priileges than it needs  

- Secure modes of operation (can be type 1+ type 2)
~ Single State  (only 1 level)
~ Multi State  (different level e.g. top secret / secret / noormal)  

~ Compartmented   (categoriesing by ppl e.g. kelly only can access to kelly's box) 
~ Dedicated  (no categorizing)

#### Evaluation Criteria
- Examine the security related components of a system  
- Trust vs Assurance  
- CMMI
- Orange Book(TCSEC)
~ by National computer security center
~ based on bell-LaPadulla model(deals with only confidentiality)  
~ Uses a hierarchically ordered series of evaluation classes
~ Defines Trust and assurance
- Orange book & rainbow series
~ A1 - Veriied Protection  
~ B1,B2,B3 - Mandatory Protection  
~ C1,C2 - Discretionary Protection  
~ D - Min sec  
- ITSEC (1991
~ F1 to F10 rates functionality (Trust)  
~ E0 to E6 rates assurance  
- Common Criteria (international standard)
~ Protection profile: Requirements from agency or customer  
~ Target of evaluation: System Designed by Vendor  
~ Security target documentation : how ToE meets protection profile  
~ Evaluation assurance level(EAL 1~7)  : level of testing base on documentation of toe  
~ EAL 1 : Functionally tested (Lowest e.g.phone can survive drop from 2meters)  
~ EAL 7 : Formally verified designed and tested (highest e.g. phone can survive drop from Floor 40   
~ Why dont always EAL 7? It takes time and cost  
- Certification
~ by vendor  
~ ensure system and documents well documented and authorized

- Accreditation
~ approved to operate at an acceptable level of risk 