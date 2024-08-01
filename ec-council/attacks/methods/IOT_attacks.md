# IOT Attacks

## What is IOT?

- Internet Of Things , also known as Internet of Everything (IoE) refers to the network of devices having IP addresses and the capability of sense, collect, and send data using embedded sensors, communication hardware, and computer software.

- In IoT, the term thing is used to refer to a device that is implanted on natural, human-made or machine made objects and has the functionality of sensing and communicating.

### IoT Architecture

- The IoT architecture is divided into five layers :

    - __Application Layer__ : Delivery of various applications to different users in IoT

    - __Middleware Layer__ : Device management and information management.

    - __Internet Layer__ : Communication between devices and the internet.

    - __Access Layer__ : Access to the network. Protocols translation and messaging

    - __Edge Technology Layer__ : Sensors and actuators, intellegent edge nodes of various types


### Challanges in IoT

- Lack of security and privacy

- Vulnerable web interfaces

- Legal, regulatory and right issues

- Default, weak and hardcoded passwords

- Clear text protocols and unnecessary open ports

- Coding errors (buffer overflows)

- Storage issues

- Difficult to update firmware and OS


### IoT Security Problems

- __Application__ : Validation of the inputted string, AuthN, AuthZ, no automatic security updates, default passwords.

- __Network__ : Firewall, improper communications encryption services, lack of automatic security updates.

- __Mobile__ : Insecure API, lack of communication channels encryption, authentication and authorization, lack of storage security.

- __Cloud__ : Improper authentication, no encryption for storage and communication, insecure web interfaces

- __IoT__ : Application + Network + Mobile + Cloud = IoT


### OWASP IoT Top 10

- __Weak, guessable, or hardcoded passwords__ : Use of easily brute forced, publicly available, or unchangeable credentials, including backdoors in firmware or client software that grants unauthorized access to deployed systems.

- __Insecure network services__ : Unneeded or insecure network services running on the device itself, especially those exposed to the internet, that compromise the confidentiality, integrity/authenticity, or availability of information or allow unauthorized remote control.

- __Insecure ecosystem interfaces__ : Insecure web, backend API, cloud, or mobile interfaces in the ecosystem outside of the device that allows compromise of the device or its related components.

- __Lack of secure update mechanism__ : Lack of ability to securely update the device. This includes lack of firmware validation on device, lack of secure delivery (un-encrypted in transit), lack of anti-rollback mechanisms, and lack of notifications of security changes due to updates.

- __Use of insecure or outdated components__ : Use of deprecated or insecure software components/libraries that could allow the device to be compromised. This includes insecure customization of operating system platforms, applications, or libraries.

- __Insufficient privacy protection__ : User's personal information stored on the device or in the ecosystem that is used insecurely, improperly, or without permission.

- __Insecure data transfer and storage__ : Lack of encryption or access control of sensitive data anywhere within the ecosystem, including at rest, in transit, or during processing.

- __Lack of device management__ : Lack of security support on devices deployed in production, including asset management, update management, secure decommissioning, systems monitoring, and response capabilities.

- __Insecure default settings__ : Devices or systems shipped with insecure default settings or lack the ability to make the system more secure by restricting operators from modifying configurations.

- __Lack of physical hardening__ : Inadequate security measures taken to physically protect the device from tampering, theft, side channel attacks, or other actions that could lead to compromise of the device or system.


## Hacking IOT Devices

### General Scenario

- The attacker will first scan the network for the IOT devices. Once the IOT devices are identified, the attacker will try to exploit the vulnerabilities in the device. Once the attacker gains access to the device, he can use the device to pivot into the network and further compromise the network.


### DDoS

- Attacker initiates the attack by exploiting the vulnerabilities in the devices and installing a malicious software in their operating system.

- Multiple infected IoT devices are refered to as Army of Botnets.

- The target is attacked with a large volume of requests from multiple IoT devices present in system.


### Exploit HVAC

- Many organisations use Internet-connected Heating, Ventilation and air Conditioning (HVAC) systems to control the temperature in their buildings.

- HVAC systems have many security vulnerabilities that are exploited by attackers to steal login credentials, gain access to the HVAC system, and perform further attack on organisation's network.


### Rolling Code Attack

- Rolling code is a security feature used in keyless entry systems for garage door openers, car doors, and remote entry systems for access to buildings.

- The system uses a randomly generated code that is sent to the receiver each time the transmitter button is pressed.

- The attacker can use a software-defined radio to capture the code and replay it to gain access to the system.

### BlueBorne Attack

- BlueBorne is an attack vector by which hackers can leverage Bluetooth connections to penetrate and take complete control over targeted devices.

- BlueBorne affects ordinary computers, mobile phones, and the expanding realm of IoT devices.

- A blueborne attack is performed on Bluetooth connections to gain access and take full control of the target device.

- After gaining access to the device, the attacker can penetrate any corporate network using the device to steal critical information about the organisation and spread malware to nearby devices.

### Jamming Attack

- Jamming is a type of attack in which the communication between wireless IoT devices are jammed so that they can be compromised.

- An attacker transmits radio signals randomly with the same frequency as the sensor nodes of communication

- As the result, the network gets jammed, which disables the endpoints from sending or recieving any messages.

### Hacking smart grid / Industrial devices : Remote Access using Backdoor

- The attacker can gain access to the smart grid or industrial devices by exploiting the backdoor in the device.

- Attacker sends a email to workers of the organization with a malicious file attached.

- Worker opens the legitimate looking email and downloads the attachment.

- The malicious file installs a backdoor in the device.

- Attacker gains access to the local network of the target organization.

- Attack enters the SCADA and disables the UPS

- Attacker disables the power supplies, leaving the city in the dark.

### SDR - Based Attacks on IoT

- Software Defined Radio (SDR) is a radio communication system where components that have been typically implemented in hardware are instead implemented by means of software on a personal computer or embedded system.

- The attacker uses SDR to examine the communication signals in the IoT network and sends spam content or texts to the interconnected devices.

- __Replay Attack__ : 

    - The attacker obtains the specific frequency used for sharing information between connected device and captures the original signal when a command is initiated by these devices.

    - The attacker segregates the command sequence and injects it into the IoT networks.


- __Cryptanalysis Attack__ : 

    - The attacker uses the same procedure as followed in a replay attack, along with reverse engineering the protocol to capture the original signal.
    
    - The attacker must be skilled in cryptography, communication theory, and modulation schemes to perform this attack.

- __Reconnaissance Attack__ : 

    - The attacker obtains information about the target device from the device's specifications.

    - The attacker then uses a multimeter to investigate the chipset and mark some identifications such as ground pins to discover the product Id and other information.

### Fault Injection Attack

- Fault injection is a technique used to test the robustness of a system by introducing faults to test code paths, in turn verifying that data is correctly preserved and that the system gracefully handles such faults.

- It is also known as Perturbation attack.

- Types of Fault Injection Attack : 

    - Optical, Electro Magnetic Fault Injection (EMFI), Body Bias Injection (BBI) :

        - Attackers inject faults into the device by using projecting lasers and electromagnetic pulses.

    - Frequency / Voltage Tampering : 

        - Attackers tamper with the operating conditions, modify the level of the power supply and/or alter the clock frequency of the chip.

    - Power/Clock/reset Glitching : 

        - Attackers inject faults or glitches into the power supply and clock network of the chip.

    - Temperature Attacks :

        - Attacker alters the temperature for operating the chip, affecting the whole operating environment.


### Capturing and analyzing IoT traffic using Wireshark

The steps are :

- Run Nmap to identify IoT devices using insecure HTTP, ports : 

    - `nmap -p 80,81,8080,8081 <Target IP address range>`

- Run ifconfig to identify your wireless card, here wlan0

- Run airmon-ng to put the wireless card in monitor mode : 

    - `airmon-ng start wlan0`

- Run airdump-ng to scan all the nearby wireless networks :

    - `airodump-ng start wlan0mon`

- Discover the target wireless network and note down the corresponding channel to sniff the target using wireshark.

- Next, setup your wireless card to listen to the traffic on the same channel using airmon-ng 

    - `airmon-ng start wlan0mon <channel>`

- Launch wireshark, and double-click the interface that was kept in monitor mode, here wlan0mon and start capturing the traffic.


## IOT Attack Tools

- [Firmalyzer]()
- [RIoT Vulnerability Scanner](https://www.beyondsecurity.com/iot-security-scanner/)
- [Foren6](https://foren6.com/)
- [IoT Inspector](https://iotinspector.princeton.edu/)
- [RFCrack](github.com/samyk/rfcat)
- [HackRF](https://greatscottgadgets.com/hackrf/)


## IoT Attack Countermeasures

- Disable the "guest" or "demo" user accounts if enabled

- Use the "lock out" feature to lock out accounts for excessive invalid login attempts

- Implement strong authentication mechanisms

- Locate control system networks and devices behind firewalls and isolate them from the business network.

- Implement end-to-end encryption and use Public key infrastructure (PKI)

- Patch vulnerabilities and update the device firmware regularly

### IoT Security Tools

- [SeaCat](https://www.teskalabs.com/products/seacat-mobile-secure-gateway)
- [Digicert IoT Device Manager](https://www.digicert.com/iot-security/)
- [Fortinet](https://www.fortinet.com/solutions/iot-security.html)
- [darktrace](https://www.darktrace.com/en/solution/iot-security/)
- [Symantec Critical system protection](https://www.symantec.com/products/iot-security)
- [Cisco IoT Threat Defense](https://www.cisco.com/c/en/us/products/security/iot-threat-defense.html)

 
 # OT Attacks

## What is OT?

- Operational technology (OT), is the software and hardware designed to detect or cause changes in industrial operations through direct monitoring and / or controlling of industrial physical devices.

- OT consists of Industrial Control System (ICS) to monitor and control the industrial operations.

## Terminologies

- __Assets__ : OT systems consists of physical assets such as sensors and actuators, servers, workstations, network devices, and PLCs, and logical assets such as flow graphics, program logic, databases, firmware and firewall rules

- __Zones and Conducts__ : A network segregation technique used to isolate the networks and assets to impose and maintain strong access control mechanisms.

- __Industrial Networks__ : A network of automated control systems is known as industrial network.

- __Business Network__ : It comprises of a network of systems that offer information infrastructure to the business.

- __Industrial Protocols__ : Protocols used for serial communication and communication over standard Ethernet ex : S7, CDA, CIP, Modbus etc.

- __Network parimeter__ : It is the outermost boundary of a network zone i.e. closed group of assets.

- __Electronic Security Perimeter__ : It is reffered to as the boundary between secure and inscure zones.

- __Critical infrastructure__ : A collection of physical or logical and assets that the failure or destruction of which will severely impact the security, safety, economy or public health.


## IT OT convergence

- IT/OT convergence is the integration of IT communicating systems and OT operation monitoring systems to bridge the gap between IT/OT technologies for improving overall security, effeciency and productivity.

- The IT/OT convergence can enable smart manufacturing known as industry 4.0, where IoT applications are used in industrial operations.

- Using internet of things for industrial operations such as monitoring supply chains, manufacturing and management systems is reffered to as Industrial Internet of Things (IIoT).

## Purdue Model

- The Purdue model is derived from the Purdue Enterprise Reference Architecture (PERA) model, which is widely used to describe internal connections and dependencies of important components in the ICS networks.

- It consists of three zones :

    - __Enterprise Zone__ : It is the topmost zone in the Purdue model. It consists of the business network and the business assets.

    - __Industrial Demilitarized Zone (IDMZ)__ : It is the middle zone in the Purdue model. It consists of the industrial network and the industrial assets.

    - __Manufacturing Zones__ : It is the bottommost zone in the Purdue model. It consists of the control network and the control assets.


## OT Security Problems

- Lack of visibility

- Plain text passwords

- Network complexity

- Legacy technologies

- Lack of anti-virus protection

- Lack of skilled security personnel

- Rapid pace of technology change

- Outdated systems

- Haphazard modernization

- Convergence with IT

- Unique production networks / Protocols

