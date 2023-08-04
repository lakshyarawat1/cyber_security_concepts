# Web application Attacks

## Web Server Attacks

### Components of a web server

- Document Root : 

    - Stores critical HTML files related to web pages of a domain name that will be served in response to client requests.

- Server Root :

    - Stores server's configuration, errors and executable, log files.

- Virtual Document Tree : 

    - Provides storage on a different machine or disk after the original disk is filled up.

- Virtual Hosting :

    - Technique of hosting multiple domain names on a single server.

- Web proxy :

    - Proxy server that sits between the web client and web server to prevent IP blocking and maintain anonymity.


### Web server security issues

- Attackers usually target software vulnerabilities and configuration errors to compromise web servers

- Network and OS level attacks can be well defended using proper network security measures such as firewalls, IDS, etc. However, web servers can be accessed from anywhere via the internet, which renders them highly vulnerable to attacks.


### Impacts of Web Server attacks

- Compromise of user accounts

- Website defacement

- Secondary attack on other websites

- Root access to other applications or servers

- Data tampering and data theft

- Reputational damage of the company


### Why are web servers compromised ?

- Improper file and directory permissions

- Lack of proper security policies, procedures and maintainence

- Server installation with default settings

- Improper authentication with external systems

- Enabling of unnecessary services, including content management and remote administration

- Default accounts having default passwords or no passwords

- Security conflicts with business ease-of-use

- Misconfiguration in web server, operating system, and networks

### DNS Server Hijacking

- Attacker compromises the DNS Server and changes the DNS settings so that all the requests coming towards the target web server are redirected to the attacker's web server.

### DNS Amplification Attack

- Attacker takes advantage of the DNS recursive method of DNS redirection to perform the attack.
- ![DNS Amplification Attack](!https://i0.wp.com/securityaffairs.co/wordpress/wp-content/uploads/2012/03/dns-amplification-attack-big.jpg?resize=473%2C331)

### Director Traversal Attack

- Attacker exploits the web server by accessing files and directories that are stored outside the web root folder.

- In this attack, attacker uses the ../ (dot-dot-slash) sequence to access the restricted directories outside the web server root directory.

- Attackers can use the trial and error method to navigate outside the root directory and access sensitive data.

### Website defacement

- Attacker changes the visual appearance of the website or a webpage.

- It occures when an intruder maliciously alters the visual appearence of a web page by inserting or substituting provocative, and frequently, offending data

- Defaced websites expose visitors to propoganda or misleading information until the unauthorized changes are dicovered.


### Web Server Misconfiguration

- Web server misconfiguration is a common vulnerability that can be exploited by attackers to gain unauthorized access to the web server.

- Server misconfiguration weakness that can be exploited to launch various attacks on web servers such as directory traversal, server intrusion and data theft

- Some common misconfigurations are : 

    - Sample configuration and script files
    - Anonymous or default users and passwords
    -  Verbose debug or error messages
    - Remote administration enabled
    - Unnecessary services enabled
    - Misconfigured / Default SSL certificates


### HTTP response splitting attack

- HTTP response splitting is a web server vulnerability that allows an attacker to inject a malicious HTTP response header into the response sent by the web server.

- It involves adding header response data into the input field so that server splits the responses into two parts.

- The attacker can control the first response to redirect the user to a malicious website whereas the other responses are discarded by the browser.


### Web cache poisoning attack

- Web cache poisoning is a technique used to force a web cache to store the attacker's response and serve it to the victim.

- It involves injecting malicious data into a web cache so that the next time the victim requests the same data, the web cache serves the malicious data to the victim.

- The attacker can use this technique to redirect the victim to a malicious website.


### SSH Bruteforce Attack

- SSH bruteforce attack is a type of password guessing attack that involves repeated attempts to guess the password of an SSH account.

- These SSH tunnels can then be used to transmit malware.

### Web server password cracking attack

- Web server password cracking attack is a type of password guessing attack that involves repeated attempts to guess the password of a web server.

- Attacker tries to exploit weakness to hack well-chosen passwords.

- The most common password found are password, root, admin, demo, test etc.

- Attackers use social enginnering techniques, phishing, spoofing or trojan to steal passwords.

- Attackers mainly attack ftp servers, SMTP Servers, Web shares, SSH tunnels, etc.

### Server Side Request Forgery (SSRF)

- Server Side Request Forgery (SSRF) is a type of attack that can be carried out to compromise a server.

- Attacker exploit the SSRF vulnerabilities in a public web server to send crafted requests into the internal or back end servers

- Once the attack is successfully performed, the attacker can perform various activities such as port scanning, data exfiltration, etc.

### Web Server attack tools

- [MetaSploit](https://www.metasploit.com/)
- [Immunity Canvas](https://www.immunityinc.com/products/canvas/)
- [THC-Hydra]()
- [Hulk DDoS]()
- [MPack]()
- [w3af](http://w3af.org/)


### Web Server attack Countermeasures

- Apply restricted ACLs and block remote registry administration.
- Secure the SAM (Stand Alone Servers only)

- Ensure that security related settings are configured properly and access to metabase file is restricted with hardened NTFS permissions.

- Remove unnecessary ISAPI filters from the web server

- Remove all unnecessary file shares including default admin shares if not required

- Secure the shares with restricted NTFS permissions

- Relocate the sites and virtual directories to non-system partitions and use IIS Web permissions to restrict access to the content

- Remove all unecessary IIS script mappings for optional file extensions to avoid exploiting any bugs i the ISAPI extensions that handle these types of files


### Web server security tools

- [Fortify](https://www.microfocus.com/en-us/products/static-code-analysis-sast/overview)
- [Acunetix](https://www.acunetix.com/)
- [Retina](https://www.beyondtrust.com/products/retina-network-security-scanner/)
- [Nessus](https://www.tenable.com/products/nessus/nessus-professional)
- [NetIQ](https://www.netiq.com/products/vulnerability-manager/) 

## How a web application works

- Web application is a client-server application in which the client interacts with the server using a web browser and the server responds to the client's requests.

- Steps involved in a web application are :

    - User sends a request to the web server using a web browser.
    - The web server receives the request and sends it to the web application server.
    - The web application server processes the request and sends it to the database server.
    - The database server processes the request and sends the response back to the web application server.
    - The web application server processes the response and sends it back to the web server.
    - The web server processes the response and sends it back to the user's web browser.

## Web services

- Web services are a set of application programming interfaces (APIs) that can be accessed over the Internet.

- For example, SOAP, REST, WSDL etc.

### Types of web services

- SOAP Web Services :

    - SOAP (Simple Object Access Protocol) is a protocol that defines a set of rules for exchanging structured information over the Internet.

    - It is based on XML format and is used to transfer data between service provider and client.

- RESTful Web Services :

    - REST (Representational State Transfer) is an architectural style that defines a set of rules for creating web services.

    - Based on set of constraints using the underlying HTTP concepts to improve performance

