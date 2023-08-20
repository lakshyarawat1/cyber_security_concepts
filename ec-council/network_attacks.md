# Network attacks

## Packet Sniffing

- Packet sniffing is the process of capturing data packets, which are in transit over a network.

- It is the process of monitoring and capturing all the packets passing through a given network using sniffing tools.

- It allows an attacker to observe and access the entire network traffic from a given point in order to gather sensitive information such as telnet passwords, email traffic, syslog traffic etc.

### Types of packet sniffing

- Passive Sniffing : 
    
    - Passive sniffing refers to sniffing through a hub, wherein the traffic is sent to all ports.
    - It involves monitoring packets sent by others without sending any additional data packets in the network traffic.

    - Passive sniffing is more stealthy and difficult to detect than active sniffing.

- Active sniffing : 

    - Active sniffings is used to sniff a switch-based network.
    - It involves injecting ARP packets to the network to flood the switch's Content Addressable Memory (CAM) table, which keeps track of host-port connections.
    - After flooding the CAM table, the switch starts to behave like a hub and forwards all the packets to all the ports.

    - Some active sniffing techniques are :

        - MAC Sniffing
        - DNS poisoning
        - ARP poisoning
        - DHCP Attacks
        - Switch Port Stealing
        - Spoofing attack

### How an attacker hacks the network using Sniffing ?

- An attacker connects his desktop to the switch port.
- He identifies a victim's machine to target his/her attacks.
- The traffic destined for the victim's machine is redirected to the attacker.
- He runs discovery tools to learn about network topology
- He poisons the victim's machine using ARP spoofing techniques.
- The hacker extracts passwords and sensitive data from the redirected traffic.


### Protocols vulnerable to Sniffing

- Telnet and Rlogin

    - Keystrokes including usernames and passwords are sent in clear text
    
- HTTP

    - Data is sent in clear text

- POP
- IMAP
- SMTP and NNTP
- FTP

## Techniques of Sniffing

### MAC flooding

- MAC flooding involves the flooding of the CAM table with fake MAC addresses and IP pairs until it is full.

- The switch then acts as a hub by broadcasting all the packets to all the ports, and therefore the attacker can sniff the traffic easily.

- __macof__ is a linux/unix tool that floods the switch's CAM tables(131,00 per min) by sending bogus mac entries.

### DHCP Starvation

- DHCP is a configuration protocol that assigns valid IP addresses to host systems out of a pre-assigned DHCP protocol.

- DHCP starvation attack is a process of inundating DHCP servers with fake DHCP requests and using all the available IP addresses.

- This results in a denail of service attack, where the DHCP server cannot issue new IP addresses to genuine host requests.

### ARP Spoofing 

- Address Resolution Protocol (ARP) is a protocol used for mapping an IP address to a physical address which is recognized in the local network.

- ARP Spoofing/poisioning is a technique whereby an attacker sends fake (spoofed) ARP messages onto a Local Area Network.

- ARP Spoofing tools include :

    - __arpspoof__ : arpspoof redirects packets from a target host (or all hosts) on the LAN intended for another host on the LAN by forging ARP replies.

    - [Ettercap](https://www.ettercap-project.org/)

    - [Bettercap](https://www.bettercap.org/)

    - [dsniff](https://www.monkey.org/~dugsong/dsniff/)

    - [MITMf](https://github.com)

### MAC Spoofing/Duplicating

- A MAC duplicating attack is launched by sniffing the network for MAC addresses of clients who are actively associated with the switch port and reusing one of those addresses.

- By listening to the traffic on the network, a malicious user can intercept and use a legimitate user's MAC address to recieve all the traffic destined for the users.

- This attack allows an attacker to gain access to the network and take over someone's identity on the network.

### DNS Poisoning

- Domain Name Server (DNS) poisoning is the unauthorized manipulation of IP addresses in the DNS cache.

- A corrupted DNS redirects a user request to the malicious website to perform illegal activities.

### Sniffing tools

- [Wireshark](https://www.wireshark.org/) : 

    - Wireshark lets you capture and interactively browse the traffic running on a computer network.

- [SteelCentral Packet Analyzer](https://www.riverbed.com/products/steelcentral/steelcentral-packet-analyzer.html)

- [Capsa Network Analyzer](https://www.colasoft.com/capsa/)

- [Observer Analyzer](https://www.viavisolutions.com/en-us/products/observer-analyzer)

- [PRTG Network Monitor](https://www.paessler.com/prtg)

- [SolarWinds Network Performance Monitor](https://www.solarwinds.com/network-performance-monitor)

### Sniffing Countermeasures

- Restrict physical access to network media to ensure that a packet sniffer cannot be installed.

- Use end-to-end encryption to protect the confidential information.

- Permanently add the MAC address of the gateway to ARP cache.

- Use static IP addresses and ARP tables to prevent attacker from adding spoofed ARP entries for machines in the network.

- Turn off network identification broadcasts, and if possible, restrict the network to authorized users to protect the network from being discovered with sniffing tools.

### Sniffer Detection Techniques

- Sends a ping request to the suspect machine with its IP address and incorrect MAC Address.
- The Ethernet adapter rejects it, as the MAC address does not match, whereas the suspect machine running the sniffer responds to it as it does not reject packets with a different MAC address.

- DNS Method : 

    - Most of the sniffers perform reverse DNS lookups to identify the machine from the IP address.

    - A machine gathering reverse DNS lookup traffic is very likely to be running a sniffer.

- ARP Method :

    - Only the machine in the promiscuous mode caches the ARP information.
    - A machine in promiscuous mode responds to the ping messages as it has the correct information about the host sending the ping requests in its cache, the rest of the machines sends an ARP probe to identify the source of the ping request.

## Denail Of Service (DOS)

### Introduction

- Denail-of-Service (DOS) is an attack on a computer or network that reduces, restricts or prevents accessibility of system resources to its legitimate users.

- Attackers flood the victims systems with non-legitimate service requests or traffic to overload its resources.

### Distributed Denail of Service (DDOS)

- Distributed Denail of Service (DDOS) is a type of DOS attack where multiple compromised systems, which are often infected with a Trojan or Botnet, are used to target a single system causing a Denail of Service (DOS) attack.

### DOS attack techniques

- UDP Flood Attack : 

    - An attacker sends spoofed UDP Packets at a very high packet rate to a remote host on random ports of a target server using a large source IP range.

    - The flooding of UDP packets causes the server to repeatedly check for non-existent applications at the ports

    - Legitimate applications are inaccessible by the system and give the error reply with an ICMP "Destination Unreachable" packet.

    - This attack consumes network resources and available bandwidth, exhausting the network until it goes offline.

- ICMP Flooding :

    - ICMP Flood Attacks are a type of attack in which attackers sends large volumes of ICMP echo requests packets to a victim system directly or through reflection networks.

    - These packets signal the victim's system to a reply, and the resulting combination of traffic saturates the bandwidth of the victim's network connection, causing it to be overwhelmed and denying access to legitimate users.

- Ping of Death :

    - In a Ping Of Death (PoD) attack, an attacker tries to crash, destabilize or freeze the targeted computer or service by sending malformed or oversized packets using a simple ping command.

    - For example, the attacker sends a packet which has a size of 65,538 bytes to target web server. This packet size exceeds the limit prescribed by RFC 791 IP, which is 65,535 bytes.

- Smurf Attack :

    - The attacker spoofs the source IP address with the victim's IP address and sends a large number of ICMP ECHO requests to an IP broadcast network.

    - This causes all the hosts on the broadcast networks to respond to the received ICMP ECHO requests. These responses will be sent to the victim's IP address, ultimately causing the machine to crash.

- SYN Flooding : 

    - The attacker sends a large number of SYN requests with fake source IP addresses to target server

    - The target machine sends back a SYN/ACK in response to the request and waits for the ACK to complete the session.

    - The target machine does not get the response because the source address is fake.

    - SYN Flooding take advantage of flaw in the implementation of three way handshake in most hosts

- DOS Fragmentation Attack :

    - Fragmentation attack is a type of network attack where an attacker breaks a packet into smaller fragments to bypass the target's firewall and IDS/IPS.

    - These attacks stops the victim from being able to re-assemble fragmented packets by flooding the target system with TCP or UDP packets, resulting in weak performance.


- Multi-Vector attacks : 

    - The attacker uses a combination of vectors, protocols and application layer attacks to disable the target.

    - The attacker rapidly and repeatedly change the form of their DDoS attacks to evade detection and mitigation efforts.

- Peer-to-peer attacks :

    - Attackers instruct clients of peer-to-peer file sharing hubs to disconnect from their peer-to-peer network and to connect to victim's fake website

    - Attackers exploit flaws found in the network using the DC++ (Direct Control) protocol, which is used for sharing all types of files between instant messaging clients.

    - Using this method, attackers launch massive denail-of-service attacks and compromise the targets.

- Permanent Denail-of-service attack :

    - also known as phlashing, pDoS refers to attacks that cause irreversible damage to a system.

    - Unlike other DoS attacks, it sabotages the system hardware, requiring replacement or reinstallation of hardware.

    - The attack is carried out using a method called __bricking a system__.

    - Using this method, attacker send fraudulent hardware updates to the victims.

- Distributed Reflection Denail-of-service attack :

    - DRDoS, also known as spoofed attack,  involves the use of multiple imtermediate and secondary machines that contribute to the actual DoS attack against the target.

    - Attacker launch this attack by sending requests to the intermediatery hosts, which then redirects the request to secondary machine, whcih in turn reflect the attack traffic to the target

### DoS Tools

- hping3 : 

    - hping3 is a command-line oriented TCP/IP packet assembler/analyzer.

    - It can scan and do packet crafting in TCP/IP, UDP, ICMP and RAW-IP protocols.

- High Orbit Ion Cannon (HOIC) :

    - HOIC is a free, open-source network stress application developed by Anonymous, a hacktivist collective, to replace the Low Orbit Ion Cannon (LOIC).

    - It carries out DDoS attacks on any IP address with a user selected port and user selected protocol.

- Low Orbit Ion Cannon (LOIC) :

    - LIOC can be used on a target site to flood the server with TCP packets, UDP packets, or HTTP requests with the intention of disrupting the service of a particular host.

- [XOIC](http://anonhacktivism.blogspot.com)
- [HULK](http://siberialaika.ru)
- [Tor's Hammer](https://sourceforge.com)
- Slowloris
- Pyloris
- R-U-Dead-Yet

### DoS Countermeasures

- Use strong encryption mechanisms for broadband networks to protect against eavasdropping.

- Ensure that the software and protocols are up-to-date, and scan the machines thoroughly to detect any anomalous behaviour.

- Disable unused and unsecure services.

- Block all inbound packets originating from service ports to block traffic from reflection servers

- Update each kernel to its latest release.

- Prevent transmission of fraudently addressed packets at the ISP level.

### DDoS Protection Tools

- A DDoS protection tool that protects IIS Servers, Apache server, game server etc.

- [Anti DDoS Guardian](http://beebyte.se)
- [Imperva DDoS Protection](https://www.imperva.com)
- [Cloudflare](https://www.cloudflare.com)
- [DOSarrest](https://www.dosarrest.com)
- [F5 Networks](https://www.f5.com)

## Session hijacking

- Session hijacking refers to an attack in which an attacker seizes control of valid TCP communicationn sessions between two computers.

- As most authentications only occur at the start of TCP session, this allows the attacker to gain access to a machine

- Attackers can sniff all the traffic from an established TCP session and perform identity theft, information theft, fraud etc.

### Why is session hijacking successful ?

- Absence of account lockout for invalid session IDs.

- Weak session-ID generation algorithms or small session IDs

- Insecure handling of session IDs

- Indefinite session timeout

- Most computer using TCP/IP are vulnerable

- Most countermeasures do not work without encryption


### Session hijacking process

- Command Injection : Start injecting packets to target server

- Session ID Prediction :  Take over the session

- Session Desynchronization : Break the connection to victim's machine

- Monitor : Monitor the flow of packets and predict the sequence number

- Sniff : Place yourself between the victim and the target 

### Sessin hijacking in OSI Model

- Network Level Hijacking :

    - Defined as the interception of packets during the transmission between a client and the server in a TCP or UDP session.

- Application Level Hijacking : 

    - Refers to gaining control over the HTTP's user session by obtaining the session IDs

### Session Hijacking Tools

- [OWASP ZAP](https://www.owasp.org)
- [Burp Suite](https://portswigger.net)
- [bettercap](https://www.bettercap.org)
- [netool toolkit]()
- [sslstrip]()


### Session Hijacking Countermeasures

- Use Secure Shell (SSH) to create a secure communication channel between the client and the server.

- Implement the log-out functionality for the user to end sessions

- Generate session ID after a successful login and accept session ID generated by server only

- Ensure that data in transit is encrypted using SSL/TLS and implment the defence in depth approach

- Use string or a long random number as a session key

- Use different usernames and passwords for different accounts.

### Sessiob Hijacking Detection Tools

- [WireShark](https://www.wireshark.org)
- [USM Anywhere](https://www.alienvault.com)
- [Check Point](https://www.checkpoint.com)
- [LogRhythm](https://logrhythm.com)
- [IBM Security QRadar](https://www.ibm.com)