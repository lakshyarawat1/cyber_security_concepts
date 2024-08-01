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

## OWASP Top 10

### Injection 

- Injection flaws are web application flaws that allows untrusted data to be interpreted and executed as part of the command or query

- Attacker exploits injection flaws by constructing malicious commands or queries that result in data loss or corruption, lack of accountability or denail of access.

- Some types of injection attacks are :

    - SQL Injection : 

        - SQL injection is a type of injection attack that allows an attacker to execute malicious SQL statements to control a web application's database server.

    - Command Injection :

        - It involves injecting operating system commands into a web application.

    - LDAP Injection :

        - LDAP injection is a type of injection attack that allows an attacker to inject and execute malicious LDAP statements to control a web application's LDAP query.


### Broken Authentication

- Broken authentication is a type of vulnerability that allows an attacker to bypass authentication methods to gain unauthorized access to the web application.

- It is usually successful because of exposed accounts, session IDs, logout, password managements, timeouts etc.

- Session ID in URLs : 

    - Attackers can sniff the network traffic or trick users to get session IDs and then reuse those session IDs for malicious purposes.

- Password Exploitation : 

    - Attackers can gain access to a web applications's password database.
    - If user's passwords are not encrypted, the attacker can exploit any user's password.

- Timeout Exploitation : 

    - If an application's timeouts are not set properly and a user closes their browser without loggin out from site accessed through a public computer, an attacker can use the same browser later and exploit  that user's privileges.

### Sensitive Data Exposure

- Sensitive data exposure is a type of vulnerability that occurs when an application does not properly protect sensitive information.

- When an application uses poorly written encryption code to securely encrypt and store sensitive data in the database, the attacker can exploit this flaw and steal or modify weakly protected sensitive data such as credit card numbers, SSNs, and other authentication credentials.

### XML External Entities (XXE)

- XML External Entities (XXE) is a type of vulnerability that allows an attacker to read local files on the web server or perform a denial of service (DoS) attack.

- It is a server side request forgery attack that occurs when a misconfigured XML parser allows applications to parse XML input from unreliable sources.

- Attacker can refer a victim's web application to an external entity by including the reference in the malicious XML input.

- When this malicious input is processed by the weakly configured XML parser of a target web application, it enables the attacker to access protected files and services from servers or  connected networks.

### Broken access Control 

- Broken access control is a type of vulnerability that allows an attacker to bypass authorization methods to gain unauthorized access to the web application.

- It allows the attacker to act as authorized user or administrator with privileged functions and create, access, modify or delete every record. 

### Security Misconfiguration

- Security misconfiguration is a type of vulnerability that occurs when an application is configured with insecure default configurations.

- These include : 

    - Unvalidated Inputs
    - Parameter / Form Tampering
    - Improper Error handling
    - Insufficient Transport layer protection

### Cross Site Scripting (XSS)

- Cross Site Scripting (XSS) is a type of vulnerability that allows an attacker to inject malicious client-side scripts into web pages viewed by other users.

- It occurs when a web application gathers malicious data from an unsuspecting user's browser and then uses that data in dynamically generated web pages without validating it.

### Insecure Deserialization

- Insecure deserialization is a type of vulnerability that occurs when an application deserializes untrusted data without properly validating it.

- Data serialization and deserialization is an effective process of linearizing and de-linearizing data objects for transmission to other networks or systems

- Attacker injects malicious code into serialized data and forward the malicious serialized data to the victim

- Insecure deserialization deserializes the malicious serialized content along with the injected malicious code, compromising the system.

### Using Components with Known Vulnerabilities

- Using components with known vulnerabilities is a type of vulnerability that occurs when an application uses components with known vulnerabilities.

- Attackers search for vulnerabilities on exploit sites like exploit-db.com and then exploit them to gain unauthorized access to the web application.

- If a vulnerable component is used in the application, the attacker can exploit the vulnerability and gain unauthorized access to the web application.

### Insufficient Logging and Monitoring

- Web applications maintain logs to track usage pattern, such as user login credentials and admin login credentials.

- Insufficient loggin and monitoring refers to the scenario where the detection software either does not record the malicious event or ignores important details about the event

- Attackers usually inject, delete, or tamper the web application logs to engage in malicious activities.


## Web Application Attack Tools

### Burp Suite

- Burp Suite is a web application security testing tool that is used to intercept, modify, and test the web application's traffic.

- It is a Java-based software platform of tools for performing security testing of web applications.

### OWASP Zed Attack Proxy

- OWASP Zed Attack Proxy (ZAP) is a free, open-source penetration testing tool that is used to find vulnerabilities in web applications.

### Other Tools

- [Metasploit](https://www.metasploit.com/)
- [Nessus](https://www.tenable.com/products/nessus)
- [w3af](http://w3af.org/)
- [Nikto](https://cirt.net/Nikto2)
- [Sn1per]()
- [WSSiP]()

## Web Application Attack Countermeasures

### SQL Injection

- Limit the length of input data.
- Use stored procedures.
- Use custom error messages
- Monitor DB traffic using IDS, WAF

### Command Injection Flaws

- Perform input validation
- Use a white list of allowed characters
- Escape dangerous characters
- Use language-specific libraries that avoid problems due to shell commands

### LDAP Injection Flaws

- Perform type, pattern and domain value validation on all input fields.
- Make an LDAP filter as specific as possible
- Validate and restrict the amount of data returned to the user.

### Broken Authentication

- Use SSL for authenticated parts of the application
- Verify whether all the user's identities and credentials are stored in a hashed form
- Never submit session data as part of GET, POST

### XML External Entities (XXE)

- Avoid processing XML input containing reference to external entities by weakly configured XML parser.
- XML unmarshaller should be configured correctly.
- Parse the document with a securely configured parser.

### Broken Access Control

- Perform access control checks before redirecting the authorized user to the requested resource
- Avoid using insecure IDs to prevent attackers guessing them
- Provide a session timeout mechanism

### Sensitive Data Exposure

- Use strong encryption algorithms to encrypt sensitive data
- Generate strong encryption keys offline and store them securely.
- Ensure that encrypted data stored on disk is not easy to decrypt.

### Security Misconfiguration

- Configure all security mechanisms and disable all unused features.
- Setup roles, permissions, and accounts and disable all default accounts or change their default passwords.
- Scan for the latest security vulnerabilities  and apply the latest security patches.
- Non-SSL requests to web pages should be redirected to SSL pages.

### Cross Site Scripting (XSS)

- Validate all headers, cookies, query strings, form fields, and hidden fields against a rigorous specification
- Use testing tools extensively during the design phase to eliminate such XSS holes
- use a web application firewall to block the execution of malicious scripts
- Convert all non-alphanumeric to HTML character entities before displaying the user input  in search engines.

### Insecure Deserialization

- Validate untrusted input which is to be serialized to ensure trusted data input
- Deserialization of trusted data must cross a trust boundary
- Developers must re-architect their applications.

### Using Components with Known Vulnerabilities

- Regularly check the versions of both client side and server side components and their dependencies.
- Continuously monitor sources like national vulnerability database for vulnerabilities in your components
- regularly apply security patches.

### Insufficient Logging and Monitoring

- Define the scope of assets covered by log monitoring to include business critical areas
- setup a minimum baseline for logging and ensure that it is followed for all assets
- Ensure that logs are logged with users context, so that the logs are traceable to specific users.

## Web Application Security Testing tools

- [N-Stalker Application Security Scanner](https://www.nstalker.com/products/)
- [Acunetix Vulnerability Scanner](https://www.acunetix.com/)
- [Netsparker](https://www.netsparker.com/)
- [Metasploit](https://www.metasploit.com/)
- [PowerSploit]()
- [Watcher]()

