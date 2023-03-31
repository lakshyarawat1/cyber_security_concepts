# Red Teaming Fundamentals

## Vulnerability Assessment

- Its main objective is to identify as many vulnerabilities in as many systems in the network as possible.
- A vulnerability assessment focuses on scanning hosts for vulnerabilities as individual entities so that security deficiencies can be identified and effective security measures can be deployed to protect the network in a prioritized manner.

### Penetration Tests

-  Penetration tests add to vulnerability assessments by allowing the pentester to explore the impact of an attacker on the overall network by doing additional steps that include :
    - Attempt to exploit the vulnerabilities found on each system. This is important as sometimes a vulnerability might exist in a system, but compensatory controls in place effectively prevent its exploitation. It also allows us to test if we can use the detected vulnerabilities to compromise a given host.
    - Conduct post-exploitation tasks on any compromised host, allowing us to find if we can extract any helpful information from them or if we might use them to pivot to other hosts that were not previously accessible from where we stand.

Some limitations of Penetration testing include : 
- Pen Tests are loud :  Usually, pentesters won't put much effort into trying to go undetected. Unlike real attackers, they don't mind being easy to detect, as they have been contracted to find as many vulnerabilities as they can in as many hosts as possible.
- Non-technical attack vectors might be overlooked: Attacks based on social engineering or physical intrusions are usually not included in what is tested.
- Relaxation of security mechanisms:While doing a regular penetration test, some security mechanisms might be temporarily disabled or relaxed for the pentesting team in favor of efficiency.