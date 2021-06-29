# Communications and Network Security
10/06/2021 Cybrary

## OSI Reference Model
- Promotes inteorperatbility between vendors
- Enables standarlization
- Describes the encapsulation(packaging of data to enable it to get from A to B)

### Application Layer
- Layer 7
- Defines a protocol that two different programs or app understand
- E.g. HTTP , HTTPS, FTP
- Application proxies
- Non-repudiation
- Certificates
- Integration with directory services
- Time awareness

### Presentation Layer
- Layer 6
- Only layer without protocol
- Present data in universal format (every one understand)
- remove redundancy from files (compression)
- concern encryption , compression , formatting

### Session Layer
- Layer 5
- establishing connection between two applications 
- Dialogue control
- release connection

### Transport Layer
- Layer 4
#### UDP
- Connectionless
- Unreliable
- No handshaking
- Desirable when real time transfer is essential  
~ For Media Streaming , Gaming , Live Time Chat , etc     
~ FTP use TCP      
~ TFTP use UDP     

### Network Layer
- Layer 3
- Routers isolate traffic into broadcast domains and use IP addressing to direct traffic
#### VLANs
- Routers are expensive
- To get broadcast isolation on a switch
- Not all switches support VLANs
- Layer 2 Switch doesnt truly understand layer 3 IP addressing SO layer 3 switch is necessary
- Protocols (All protocols start with I except IMAP-email)
#### IP
#### ICMP - IP helpers (Like ping)
- Weak
- Threats:   
~ Ping Flood    
~ SMURF (Uses a spoofed source address target and directed broadcasts to launch ddos)

#### IGMP - Internet Group Message Protocol
#### IGRP
#### IPSEC
#### IKE
#### ISAKMP

### Data Link Layer
- Layer 2
- Only Layer have 2 sub layers 
#### LLC - Logical Link Control
- Error Detection
#### MAC - Media Access Control 
- Physical
- Good Local Identifier / Bad Global Identifier
- CSMA / CD sense mulitple access with collision detection for 802.3 ethernet
- CSMA / CA sense multiple access with Collision avoidence for 802.11 wireless
- Token Passing : 24 bit control frame passed around the network environemnt with purpose of determining which system can transmit data (e.g.輪流發言). Only 1 token + cannot communicate without token
#### Switch 
- Use Mac to direct traffic
- isolate trafficc into domains
- does not isolate broadcasts natively

#### ARP
- Find who belongs to this MAC addresss
- cache after success finding once
- Threats  
~ Posioning the cache  

### Physical Layer
- Layer 1   
- All hardware devices have a point of connection
- Threats:  
~ Theft    
~ Unauthorized Access    
~ Vandalism  
~ Sniffing   
~ Interference     
~ Data Emanation  

## TCP/IP model
### Application Layer
- App + Present + Session
### Transport Layer
### Internet Layer
- = Network Layer
### Network Access Layer
- Data Link + Physical

## Firewalls
- Provide isolation and separation
- create zones based on trust
- hardware firewalls VS software firewalls
- used rule-based access control
- enforce network layer
- usually firewalls put perimeter of network allow or deny traffic based on company or network policy
- must have ip forwarding turned off
- often creat DMZ

### Layer3 firewall
- Packet Filtering
- Screening Routers
- Fast & Cheap & dumb (not too much dicision making)
- Inspect Layer 3 & Layer 4 headers  
~ Source and destination IP  
~ Source and Destination Port  
~ Layer 4 Protocol (TCP or UDP)  
### Layer 5 firewall
- Stateful filtering  
~ Awareness of initiation of the session and the state    
~ Can block unsolicited replies    
~ Can understand syntax of lower layer protocols + block misbehaving traffic  
### Layer 7
- Smartest / Expensive / Slow
- Called application proxies/firewalls
- Deep Packet inspection
- Forward proxy inspects traffic from inside out
- Reverse Proxy inspects trafftic from outside going in
- Can inspect on content , time , application-awareness , certicates, etc
- Specific to application protocol

### Packet filter
- packet filters keep no state  
~ disadvantages : fragment  
~ each packet is evaluated own without regard to previous traffic
- Rule based access control
- used on edge of network before stateful firewall for performance reasons

### Stateful firewall
- router keeps track of connections in table knows which conversation are active
- allow return traffic come back where packet filter have rule to define returned traffic

### Proxy firewalls
- circuit level (Layer 5)
- Both hide internal host /addressing from outside world
- application  
~ understand each application when proxing  
~ allows for additional security since inspecting data for protocol violations
##### advantages
- extra sec  
- advanced loging / auditing / access control features
##### disadvatages
- extra processing CPU (slower)
- proxies only understand protocols they were written to understand -> separte app proxy for each protocol

### NAT/PAT
- Network address translation
- NAT  1 to 1 (internal:external address) ; PAT Many address(can be different ports) to 1 external (different ports)
- runs on proxy firewall
#### advantages
- allow use private addresss Internally
- allow use of RFC1918 IP addresss
- hides internal network structure
- transparent -> no need special software
#### disadvantages
- single point of failure/performance bottleneck
- doesnt protect from bad content

## LAN , WAN , MAN
### LAN
- local area network
- high speed
- small physical area
### WAN
- wide
- big area
### MAN

### Circuit switching
- PSTN
- ISDN
- DSL
- T-carriers

### Packet switching
- X.25
- Frame Relay
- ATM
- VOIP
#### VOIP threats
- Eavesdropping (greatest) -> enable S/RTP
- Toll fraud
- vishing
- SPIT
- Latency
- Jittering

#### Multi protocol labeled switching
- create cost effective , private wide area networks faster + more secure than regular router networks
- more secure than public internet caz end to end circuit (just built for your organization)
- Layer 3 
- provide QoS for VOIP + high priority traffic
- no configure and maintain encryption based  VPN . Avoid latency + delay inherent 

## Remote access
### Dial Up
- PPP   
~ PAP , CHAP , EAP
### Tunneling
- PPTP (not enough)  
~ PAP (plain txt , X use) , CHAP (challenge handshake , problem : only use password) , EAP (extensible authenication , not only password)  
~ MPPE (microsoft)  
- GRE (encapsulation / packaging)  
~ point to point link between two networks  
~ extra ip header to origin packet  

- L2TP (cisco, no security built , just encapsulation to use IPSec)  
~ IPSec  
- IPSec  
### Wireless
- Encryption  
~ WEP , WPA , WPA II  
### Authentication
- 802.1x  
 
## Wireless Communications

### wireless problems
- unauthorized access
- sniffing
- war driving
- unauthorized access points(Man in the middle)

### Encryption
- WEP  
~ Shared authentication passwords  
~ weak IV (24bits)  
~ IV transmitted in clear text  
~ RC-4  
~ Easily crackable  
~ Only option for 802.11b    
- WPA   
~ Stronger IV    
~ Introduced TKIP  (temporal key integrity protocol)  
~ Still RC-4    
- WPA2    
~ AES     
~ CCMP   
~ Not backwards compatible  

### Authentication
= Enterprice use 802.1X autehntication to have individual passwords for individual users (RADIUS)

## Bluetooth
- Personal area network protocol 
### modes
- discovery mode
- automatic pairing
- Blue jacking   
~ send spam to nearby bluetooth devices
- Blue snarfing   
~ copies information off of remote devices
- Blue bugging  
~ more serious   
~ allow full use of phone    
~ allow one to make calls    
~ eavesdrop on calls   