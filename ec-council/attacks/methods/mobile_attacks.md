# Mobile Attacks

## Vulnerable Areas in Mobile Environment

- Smartphones offer broad Internet and network connectivity via different channels such as 3g/4g/5g, WiFi, Bluetooth, NFC, etc.

- Security threats may arise in different places along these channels during data transmission.

## OWASP TOP 10 Mobile

- Improper Platform Usage

- Insecure Data storage

- Insecure Communication

- Insecure authentication

- Insufficient Cryptography

- Insecure authorization

- Client Code Quality

- Code Tampering

- Reverse Engineering

- Extraneous Functionality

## Anatomy of a Mobile Attack

### The Device

- Browser :

  - Phishing
  - Framing
  - Man-in-the-middle
  - Clickjacking
  - Buffer overflow
  - Data Cacheing

- Phone / SMS :

  - Baseband Attacks
  - SMSishing

- Apps :

  - Sensitive Data Exposure
  - No encryption / weak encryption
  - Improper SSL Validation
  - Configuration Manipulation
  - Dynamic Runtime Injection
  - Unintended permissions
  - Escalation of Privileges
  - Access to device and user info
  - Third-party Code
  - Intent Hijacking
  - Zip directory Traversal
  - Side channel Attack

### The network

- Wifi
- Rogue AP Attack
- Packet Sniffing
- Man-in-the-middle
- Session Hijacking
- DNS Poisoning
- SSLStrip
- Fake SSL Certificate
- BGP Hijacking
- HTTP Proxy

### Data center or Cloud

- Platform Vulnerabilities
- Server misconfiguration
- XSS
- XSRF
- Weak input validation
- Brute force attacks
- Hypervisor attacks
- SQL Injection
- Privilege escalation
- OS Command Injection

## How a hacker can compromise your mobile phone

### Surveillance

- Audio
- Camera
- Call Logs
- location
- SMS Messages

### Data Theft

- Account Details
- Contacts
- Call logs
- Phone numbers
- Stealing data via app vulnerabilities
- Stealing international mobile equipment identity (IMEI) number

### Financial

- Sending premium SMS messages
- Stealing transaction authentication numbers (TANs)
- Extortion via ransomware
- Fake antivirus
- Making expensive calls

### Botnets

- Sending spam
- Launching DDoS attacks

### Impersonation

- SMS Redirection
- Sending email
- Posting to social media

## Mobile Platform Vulnerabilities

- Malicious Apps in Store
- Mobile Malware
- App sandboxing vulnerabilities
- Weak device and App encryption
- OS and App Update Issues
- Jailbreaking and rooting
- Mobile Application Vulnerabilities
- Privacy Issues
- Weak Data security
- Excessive permission
- Weak Communication security
- Physical attacks

### App Sandboxing Issues

- Sandboxing helps protect systems and users by limiting the resources the app can access to the mobile platform, however, malicious applications may exploit vulnerabilities and bypass the sandbox.

- Sandboxing is a security mechanism for separating running programs. It is often used to execute untested code, or untrusted programs from unverified third-parties, suppliers, untrusted users and untrusted websites.

### Agent Smith Attack

- An agent Smith attack is carried out by persuading the victim to install a malicious app designed and published by attacker.
- The malicious app replaces legimitate apps, like WhatsApp, with a malicious version, which is capable of displaying fake ads.

- The attacker produces a huge volume of ads on victim's device through malicious app for financial gains.

### SS7 Vulnerability

- Signaling System 7 (SS7) is a communication protocol that allows mobile users to exchange communication through another cellular network.

- SS7 is operated depending on mutual trust between operators without any authentication.

- Attackers can exploit this vulnerability to perform a man-in-the-middle attack, impeding the texts and calls between communicating devices.

### SIMJacker Attack

- SIMJacker is a vulnerability that allows attackers to remotely control victims' mobile phone by sending SMS messages to their devices.

- It is associated with SIM card's S@T browser, a pre-installed software on SIM cards that is designed to provide a set of instructions.

- The attacker exploits Simjacker to perform various malicious attacks, such as capturing location of devices, monitoring calls, forcing device browsers to connect to malicious websites and performing denial-of-service attacks.

## Android Hacking Tools

- [MetaSploit](https://www.metasploit.com/)
- [zANTI](https://www.zimperium.com/zanti-mobile-penetration-testing)
- [Network Spoofer]()
- [DroidSheep]()
- [PhoneSploit](www.github.com/Zucccs/PhoneSploit)

## iOS Hacking Tools

- [Elcomsoft iOS Forensic Toolkit](https://www.elcomsoft.com/eift.html)
- [Fing](https://www.fing.com/products/fing-app)
- [Spyic](https://spyic.com/phone-hack/iphone-hack/)
- [Frida](https://frida.re/)
- [iWebInspector](https://www.iwebinspector.com/)

## Mobile Device Management (MDM)

- Mobile Device Management (MDM) is a type of security software used by an IT department to monitor, manage and secure employees' mobile devices that are deployed across multiple mobile service providers and across multiple mobile operating systems being used in the organization.

- MDM is a great way to expand the capabilities of mobile devices in the workplace, but it also creates a number of security risks.

- MDM software is designed to help protect the privacy of employees, but it can also be used to monitor their personal activities.

## BYOD (Bring Your Own Device)

- BYOD is a policy that allows employees to use their own mobile devices and laptops for work.

- BYOD is a great way to increase productivity and reduce costs, but it also creates a number of security risks.

### BYOD Security Risks

- Data leakage

- Sharing confidential information

- Improper deposition of devices

- Support for many different devices

- Mixing personal and private data

- Lost or stolen devices

- Lack of awareness

- Ability to bypass organisation's network policies

## OWASP Top - 10 Mobile Control

- Identify and protect sensitive data on the mobile device 

- Handle password credentials securely on the device

- Ensure sensitive data are protected in transit

- Implement user authentication, authorization, and session management correctly

- Keep the backend API services and platform secure

- Secure data integration with third-party services and applications

- Pay specific attention to collection and storage of consent for the collection and use of the user's data

- Implement controls to prevent unauthorized access to paid-for resources

- Ensure secure distribution / provisioning of mobile app

- Carefully check any runtime interpretation of code of errors

## General guidelines for Mobile platform security

- Do not load too many applications and avoid auto-upload of photos to social networks.

- Perform a security assessment of the application architecture.

- Maintain configuration control and management

- Install applications from trusted applications stores

- Securely wipe or delete the data when deposing a device

- Do not share information within GPS-enabled apps unless it is necessary

- Disable wireless access, such as Wifi and Bluetooth, if not in use.

- Never connect two seperate networks, such as Wifi and Bluetooth, simulataneously.

### Mobile Security tools

- [Malwarebytes](https://www.malwarebytes.com/)
- [Lookout](https://www.lookout.com/)
- [Zimperium](https://www.zimperium.com/)
- [BullGuard](https://www.bullguard.com/)
- [Norton](https://us.norton.com/)
- [Comodo](https://www.comodo.com/)