# SC-900 

## Shared responsibility model

- Shared responsibility model identifies which tasks are handled by the cloud provider, and which are handled by the user.

- Responsibilities : ( By customer )

    - On-premises < : 
        - Physical Datacenter
        - Physical Network
        - Physical hosts
    
    - IaaS < : 
        - Operating System
        - Network Controls

    - PaaS < : 
        - Applications
        - Identity and directory infrastructure

    - SaaS : 
        - Accounts and identities
        - Devices
        - Information and data

## Defense in Depth

- Layered approach
- Layers like : 
    
    - Physical security
    - Identity and access management, like MFA, Access Control lists
    - Perimeter security, like DDoS filters
    - Network security, like network segmentation, and network access controls
    - Compute layer security for virtual machines
    - Application layer 
    - Data layer like encrpytion

## CIA 

- Confidentiality :
    - Keep confidential sensitive data safe.

- Integrity :
    - Keep messages or data correct.
    - Data should not be tampered with or changed by unauthorized person.
    - SHould not lose its meaning,

- Availability :
    - Making data available

## Zero Trust model

- Assumes that everything is on open and untrusted network
- Even resources behind firewalls
- Trust no one, verify everything

- Principles include :
    - Verify Explicitly : Always authorize and authenticate based on available data points, like user identity, location, device, service or workload, data classification, and anomalies
    - Least privileged access : just-in-time and just-enough access (JIT/JEA)
    - Assume breaches : Segment access by network, user, devices and applications.

- Six Foundational Pillers are : 

    1. Identities : Users, services or devices. Identity must be verified with strong authentication, whenever accessing resources, following least privilege.
    2. Devices : Monitoring devices for health and compliance, they are bit attack surfaces.
    3. Applications : Managing permissions and access.
    4. Infrastructure : asseesing version, configuration, and JIT Access, and use telemetry to detect anomalies and attacks.
    5. Networks : should be segmented, including deeper in-network segmentation. Also, realtime threat protection, end-to-end encrption, monitoring and analytics.
    6. Data : Should be classified, labelled, and encrypted.

## Encrpytion / Hashing

### Encrpytion

- Symmetric Encrpytion : Uses same key for encrpytion and decryption of the data.
- Asymmetric encrpytion : Uses different keys ( public, private ) for encryption and decryption.

- Data at rest :
    - Data is stored on a physical device, like server.
    - Ensures that data is unreadable without the keys and secrets needed.

- Data in transit : 
    - Encrpytion of data at the application layer before sending it to the network.
    - Ex: HTTPS

- Data in use : 
    - Securing data in non-persistent storage like RAM or CPU caches.
    - Can be done by creating an enclave that protects the data and keeps it encrypted.

### Hashing

- Converts text to unique fixed-length value called hash.
- Irreversable
- Salting is another layer on top.

## GRC Concepts

- Governance, Risk and compliance

### Governance

- System of rules, practices and processes an organization uses to direct and control its activity.
- Arise from external standards, obligations and expectations.
- For ex: who, what, when and where users, and applications can access coorporate resources and who has admin privileges and for how long.

### Risk

- Risk management is process of identifying, assessing, and responding to threats or events that may impact company or customer objectives.

### Compliance

- country, state or region rules or laws and regulations that an org. must follow.
- Defines what types of data must be protected, what processes are required under the legislation and what penalties are issued to organizations that fails to comply.
- Compliance requires only that the legally mandated minimum standards are met.

- Some concepts include : 
    - Data residency : physical locations where the data can be stored and how and when it can be transfered, processed or accessed internationally. Depends on juridiction.
    - Data sovereignty : Data is subject to laws/regulations of the country where it is stored physically.
    - Data privacy : Providing notices and being transparent about data collection, processing, use and sharing of personal data.   