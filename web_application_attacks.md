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
- [DNS Amplification Attack](!https://i0.wp.com/securityaffairs.co/wordpress/wp-content/uploads/2012/03/dns-amplification-attack-big.jpg?resize=473%2C331)