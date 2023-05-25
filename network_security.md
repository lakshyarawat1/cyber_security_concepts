# Network security

Network security is the deployment and monitoring of cyber security solutions to protect your organisation's IT systems from attacks and breaches. It also covers policies surrounding the handling of sensitive information.

## Network Tools 

### Ping

- To test whether the connectio to remote IP address is possible
- Ping uses ICMP protocol, which works on Network layer.
- Basic syntax for ping is :   ping <IP Address>
- Ping can also be used to get IP address of a website domain.
- Every device supports ping
- -i switch lets you change the intervals between packets sent
- -v switch increases the verbose

### TraceRoute

- Traceroute can be used to map the route to your request
- It allows you to see all intermediate steps of your request until to reaches its target.
- Uses ICMP in windows and UDP in unix
- -i : switch to specify the interface
- runs on internet layer

### WHOIS

- allows your to see the information about the domain name i.e the website address

### Dig

- dig allows us to manually query recursive DNS servers of our choice for information
- syntax : dig <domain> @<dns-server-ip>


## Network Security threats

- Internal Security Threats : Over 90% of cyberattacks are caused by human error. This can take the form of phishing attacks, careless decision-making, weak passwords, and more.

-  Distributed denial-of-service (DDoS) attacks : A DDoS attack causes websites to crash, malfunction, or experience slow loading times. In these cases, cybercriminals infect internet-connected devices (mobile phones, computers, etc.) and convert them into bots.

-  Rogue security software : Rogue security software tricks businesses into believing their IT infrastructure is not operational due to a virus. It usually appears as a warning message sent by a legitimate anti-malware solution.

- Ransomwares

- Malwares

- Phishing attacks

- Viruses

- Side Channels

### Identification of Threats

- Intrusion Detection systems
- Host-based Intrusion Detection systems : A host-based IDS is an intrusion detection system that monitors the computer infrastructure on which it is installed, analyzing traffic and logging malicious behavior.

- Network Intrusion Detection System

### Prevention 

- Firewalls
- Scans
- Antiviruses
- Intrusion prevention systems

## Network Security infrastructure 

Network security infrastructure refers to the collection of hardware, software, and protocols that are put in place to secure a computer network from unauthorized access, misuse, and damage.

Some of the essential components of network security infrastructure include:

- Firewalls
- IDS/IPS
- VPNs
- Access Control Systems
- Anti-virus Systems
- Encryption
- Disaster Recovery

