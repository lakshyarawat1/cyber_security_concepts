# Password Cracking

- Password cracking is the process of recovering passwords from data that has been stored in or transmitted by a computer system.

- Most of the cracking techniques are successful because of the weak passwords.

## Password Complexity

- Password complexity is the measure of how difficult it is to guess a password.

- Password complexity is determined by the following factors:

    - Password length
    - Password character set
    - Password character types


## Microsoft Authentication

### Security Account Manager (SAM) Database

- Windows stores user account information in a database called the Security Account Manager (SAM) database or Active Directory (AD).

- These passwords are hashed and then stored.

### NTLM Authentication

- NTLM is a suite of Microsoft security protocols that provides authentication, integrity, and confidentiality to users.

- NTLM authentication protocol types are : 

    - NTLM Authentication Protocol
    - LM Authentication Protocol

- These protocols store the user's passwords in SAM database after hashing

### Kerberos Authentication

- Microsoft has upgraded its default authentication protocol from NTLM to Kerberos which provides stronger auth for client/server applications than NTLM.

## Types of password attacks

- Password attacks are classified into two types:

    - Non-electronic password attacks : 

        - These attacks are performed without the use of any electronic device.

        - These attacks are performed by the attacker by using the information about the target.

        - These attacks are also known as offline attacks.

        - For example, shoulder surfing, dumpster diving, social engineering, etc.

    - Active Online Attacks : 

        - The attacker performs password cracking by directly communicating with the victim's machine.

        - Some examples are : 
            - Brute force attack
            - Rule based Attacks
            - Dictionary Attacks
            - Hash injection
            - LLMNR/NBT-NS Poisoning
            - Trojan/Spyware/Keylogger
            - Password guessing

    - Passive online attacks : 

        - The attacker performs password cracking without communicating with the authorized party.

        - Examples are : 
            - Wire Sniffing
            - Man-in-the-middle attack
            - Replay attack

    - Offline Attacks : 

        - The attacker copies the target's password file and then tries to crack the passwords on his own system at a different location

        - Examples are :
            - Rainbow table attack
            - Distributed network attack

### Default passwords 

- A default password is a standard pre-configured password for a device supplied by the manufacturer.

- Attackers use default passwords to gain access to the device through password guessing attacks.

- Some online tools for default passwords are : 

    - [fortypoundhead.com](https://www.fortypoundhead.com/passwords.php)
    - [cirt.net](https://cirt.net/passwords)
    - [defaultpassword.com](https://defaultpassword.com/)
    - [default-password.info](https://default-password.info/)
    - [routerpasswords.com](https://www.routerpasswords.com/)

### Hash Injection / Pass the hash (PtH) attack

- Hash injection is a technique used to crack the password of a remote computer without sending any packets to the remote computer. 

- A hash injection allows the attacker to inject a compromised hash into a local session and use the hash to validate network resources.

- The attacker finds and extracts a logged-on domain admin account hash.

- The attacker uses the extracted hash to log on the domain controller.

### LLNMR/NBT-NS Poisoning

- Link-Local Multicast Name Resolution (LLMNR) and NetBIOS Name Service (NBT-NS) are two protocols that allow name resolution in the absence of a DNS server.

- The attacker cracks the NTLMv2 hash obtained from the victim's authentication process.

- The extracted credentials are used to log on the host system in the network.

### Pass the Ticket attacks

- Pass the ticket is a method of authenticating to a system using Kerberos tickets without having access to an account's password.

- To perform this attack, the attacker dumps Kerberos tickets of legitimate accounts using credential dumping tools.

- The attacker then launches a pass the ticket attack either by stealing the ST or TGT ticket from the end user machine, or by stealing the ST/TGT from a compromised authorization server.

- The attacker uses the retrieved ticket to gain access to the network.

- Tools such as Mimikatz, Rubeus and Windows credential Editor are used to attackers to launch such attacks.

### Wire Sniffing

- Attacker runs packet sniffer tools on the LAN to access and record the raw network traffic.

- The captured data may include sensitive information such as passwords and emails.

- Sniffed credentials are used to gain access to the system

### Rainbow table attacks

- A rainbow table is a precomputed table for reversing cryptographic hash functions, usually for cracking password hashes.

- The hash of the password is captured and compared to the precomputed hashes in the rainbow table.

- It is easy to recover passwords by comparing the hashes to precomputed tables.

## Password cracking tools

- Password cracking tools are used to recover passwords from data that has been stored in or transmitted by a computer system.

- Some of the password cracking tools are : 

    - L0phtCrack and Ophcrack : 

        - L0phtCrack is a tool designed to audit passwords and recover applications.
        
        - Ophcrack is a windows password cracker based on rainbow tables

    - RainbowCrack : 

        - RainbowCrack is a general propose implementation of Philippe Oechslin's faster time-memory trade-off technique.
        - It cracks hashes with rainbow tables.

    - John the Ripper : 

        - John the Ripper is a fast password cracker, currently available for many flavors of Unix, Windows, DOS, BeOS, and OpenVMS

    - Medusa : 

        - Medusa is a speedy, massively parallel, modular, login brute-forcer for network services created by the geeks at Foofus.net

    - hashcat : 

        - hashcat is the world's fastest and most advanced password recovery utility, supporting five unique modes of attack for over 200 highly-optimized hashing algorithms.


## Password Cracking Countermeasures

- Don't use same password for all accounts

- Don't use common passwords that are present in the dictionaries.

- Set password change policy to 30 days.

- Disallow password sharing.

- Don't use cleartext protocols and protocols with weak encryption.

- Dont use default passwords.

- Make passwords harder to guess.

- Ensure that applications neither store passwords in memory nor write them to disk in clear text.

- Use MFA, 2FA, and 3FA.