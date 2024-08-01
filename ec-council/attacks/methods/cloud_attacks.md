# Cloud Attacks

## Introduction to Cloud Computing

- Cloud Computing is an on-demand delivery of IT capabilities where IT infrastruture and applications are provided to subscribers as a metered service over a network.


### Characteristics of Cloud Computing

- On-demand self-service

- Distributed storage

- Rapid elasticity

- Automated management
 
- Broad network access

- Resource pooling

- Measured service

- Virtualization 


### Types of Cloud Computing Services

- Infrastructure as a Service (IaaS) :

    - SYS ADMINS

    - Provides virtual machines and other abstracted hardware and operating systems which may be controlled through a service API
    - Examples: Amazon EC2, Rackspace, GoGrid, Terremark, and Joyent, Microsoft Onedrive

- Platform-as-a-service (PaaS) :

    - DEVELOPERS

    - Offers development tools, configuration management, and deployment services to application developers on demand that can be used by subscribers to develop custom applications.

    - Eg : Google App Engine, Microsoft Azure, Heroku, Engine Yard, and Force.com


- Software-as-a-service (SaaS) :

    - END USERS

    - Offers software services on demand over the internet.

    - Examples are web-based applications like Google Docs or Calendars, Salesforce CRM, or Freshbooks.


- Identity-as-a-service (IDaaS) :

    - END USERS

    - Offers IAM services including SSO, MFA, IGA, and intelligent collection

    - Examples are Centrify Identity Service, Okta, and Ping Identity, Microsoft Azure AD, OneLogin, and Auth0.

- Security-as-a-service (SECaaS) :

    - SYS ADMINS

    - Provides penetration testing, authentication, intrustion detection, anti-malware, security incident and event management services.

    - Examples are Cloudflare, Zscaler, eSentire MDR, SwitchFast Technologies, OneNeck IT Solutions, or McAffe Managed Security services.

- Container-as-a-service (CaaS) :

    - SYS ADMINS

    - Offers virtualization of container engines, and management of containers , applications and clusters, throught a web portal or API.

    - Examples are Amazon Elastic Container Service, Azure Container Service, Google Container Engine, and IBM Bluemix Container Service.

- Function-as-a-service (FaaS) :

    - DEVELOPERS

    - Offers serverless computing, where the cloud provider runs the server and dynamically manages the allocation of machine resources.

    - Examples are AWS Lambda, Google Cloud Functions, and Microsoft Azure Functions.


### Cloud Deployment Models

- Public Cloud :

    - A public cloud is a cloud service offered by a cloud provider to multiple customers over the internet.

    - Examples are Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform, IBM Cloud, and Oracle Cloud.


- Private Cloud :

    - A private cloud is a cloud service offered by a cloud provider to a single customer over the internet or a private internal network.

    - Examples are Amazon Virtual Private Cloud (VPC), Microsoft Azure Virtual Network (VNet), Google Virtual Private Cloud (VPC), IBM Cloud Virtual Private Cloud (VPC), and Oracle Cloud Infrastructure (OCI).


- Hybrid Cloud :

    - A hybrid cloud is a combination of public and private cloud services.

    - Examples are Amazon AWS Outposts, Microsoft Azure Stack, Google Anthos, IBM Cloud Satellite, and Oracle Cloud at Customer.


- Community Cloud :

    - A community cloud is a cloud service offered by a cloud provider to a group of customers with shared interests over the internet or a private internal network.

    - Examples are Amazon AWS GovCloud, Microsoft Azure Government, Google Government Cloud, IBM Cloud Government, and Oracle Cloud at Customer.


- Multicloud :

    - A multicloud is a combination of multiple cloud services from multiple cloud providers.

    - Examples are Amazon AWS, Microsoft Azure, Google Cloud Platform, IBM Cloud, and Oracle Cloud.


## NIST Cloud Deployment Reference Architecture

- NIST Cloud Deployment Reference Architecture is a reference model that provides a common framework for the development of standards, guidance, and compliance assessment programs for cloud computing.

- It has five major actors :

    - __Cloud Consumer__  :  A person or organization that maintains a business relationship with, and uses service from, Cloud Providers.

    - __Cloud Provider__ : A person, organization, or entity responsible for making a service available to interested parties.

    - __Cloud carrier__ : A intermediary that provides connectivity and transport of cloud services from Cloud Providers to Cloud Consumers.

    - __Cloud Auditor__ : A party that can conduct independent assessment of cloud services, information system operations, performance and security of the cloud implementation.

    - __Cloud Broker__ : An entity that manages the use, performance, and delivery of cloud services, and negotiates relationships between Cloud Providers and Cloud Consumers.


### Cloud Storage Architecture

- Cloud storage is a data storage medium used to store digital data in logical pools using a network.

- The cloud storage architecture consists of three main layers namely, front-end, middleware and back-end.

- The front-end layer is accessed by the end user where it provides APIs for the management of data storage.

- The middleware layer performs several functions such as data de-duplication and replication of data.

- The back-end layer is where the hardware is implemented.


# Containerization

- A container is a package of an application/software including all its dependencies such as libraries, binaries, and configuration files. and other resources that run independently of the host operating system.

- CaaS is a service that includes virtualization of container and container management through orchestrators.


## Containers VS Virtual Machines

- Virtualization is the ability to run multiple operating systems on a single host machine and share the underlying resources such as the server, storage devices and network.

- Containers are placed on the top of one physical server and host operating system, and share the operating system's kernel binaries and libraries, thereby, reducing the need for reproducing the OS.


## Docker

- Docker is an open source technology used for developing, packaging and running applications and all its dependencies in the form of containers, to ensure that the applications works in a seamless environment.

- Docker performs a Platform-as-a-service through OS-level virtualization and delivers containerized software packages


### Microservices VS Docker

- Monolithic applications are broken down into cloud hosted sub-applications called microservices that work together, each performing a unique task.

- As each microservice is packaged into the Docker container along with the required libraries, frameworks, and configuration files, microservices belonging to a single application can be developed and managed using multiple platforms.


### Docker Architecture

- Docker architecture consists of three main components namely, Docker Client, Docker Host, and Docker Registry.

- Docker Client is a command line interface (CLI) tool that allows users to interact with Docker.

- Docker Host is a physical or virtual machine that runs the Docker daemon and containers.

- Docker Registry is a repository for Docker images.


### Docker Networking

- Docker connects multiple containers and services or other non-Docker workloads together

- The docker networking architecture is developed on a set of interfaces known as the Container Network Model (CNM)

- The CNM provides applications probability across heterogeneous infrastructures.

### Container Orchestration

- An automated process of managing the lifecycles of software containers and their dynamic environments.

- It is used for scheduling and distributing the work of individual containers for microservices-based applications spread across multiple clusters.


### Kubernetes

- Kubernetes or K8s, is an open-source, portable, extensive, orchestration platform developed by Google for managing containerized applications and microservices.

- Kubernetes provides resilient framework for managing distributed containers, generating deployment patterns, and performing failover and redundency for the applications.

- Some features of Kubernetes  are :

    - Service discovery
    - Load balancing
    - Storage orchestration
    - Automated rollouts and rollbacks
    - Automatic bin packing
    - Self-healing
    - Secret and configuration management.


### Kubernetes Cluster architecture

- Kubernetes cluster is a set of nodes that run containerized applications.

- A node is a physical or virtual machine that runs the Kubernetes application.

- A kubernetes cluster consists of a master node and worker nodes.

- The master node is responsible for managing the worker nodes and the pods in the cluster.

- A pod is a group of one or more containers that share storage, network, and information about how to run the containers.

- The worker nodes are responsible for running the pods and communicating with the master node.

### Kubernetes VS Docker

- Docker is open source software that can be installed on any host to build , deploy and run containerized applications on single OS.

- When docker is installed on multiple hosts with differnt OS, you can use kubernetes to manage these Docker Hosts.

- Kubernetes is a container orchestration platform that automates the process of creating, managing, updating, scaling and destroying containers.

- Kubernetes can be coupled with any containerization technology such as Docker, Rkt, RunC, and containerd.

- Both docker and kubernetes are based on microservices architecture, and built using the Go programming language to deploy small , lightweight binaries, and YAML files for specifying applications configuration and stacks.


# Container security challanges

- Inflow of vulnerable source code

- Large attack surface

- Lack of visibility

- Compromising secrets

- DevOps speed

- Noisy neighbour containers

- Container breakout to the host

- Network-based attacks

- Bypassing isolation

- Ecosystem complexity.


## Container management platforms

- [Docker](https://www.docker.com/)

- [Amazon Elastic Container Service](https://aws.amazon.com/ecs/)

- [Microsoft Azure Container Instances](https://azure.microsoft.com/en-us/services/container-instances/)

- [Red Hat OpenShift](https://www.openshift.com/)

- [Portainer](https://www.portainer.io/)

- [HPE Ezmeral Container Platform](https://www.hpe.com/us/en/software/containers.html)

## Kubernetes Platforms

- [Kubernetes](https://kubernetes.io/)

- [Amazon Elastic Kubernetes Service](https://aws.amazon.com/eks/)

- [Docker Enterprise](https://www.docker.com/products/kubernetes)

- [Knative](https://knative.dev/)

- [IBM Cloud Kubernetes Service](https://www.ibm.com/cloud/kubernetes-service)

- [Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine)


## OWASP Top 10 Cloud Security Risks

- __Accountability and Data ownership__ : The cloud provider is responsible for the security of the cloud, while the cloud consumer is responsible for the security of the data. Using public cloud for hosting business services can cause severe risks for the recoverability of data

- __User Identity Federation__ : Creating multiple user identities for different cloud providers makes it complex to manage multiple users IDs and credentials.


- __Regulatory Compliance__ : There is a lack of transparency, and there are different regulatory laws in different countries.

- __Business Continuity and risiliency__ : There can be busniess risk or monentary loss if the cloud provider handles the business continuity improperly.

- __User privacy and secondary usage of data__ : The default share feature in social web sites can jeopardize the privacy of user's personal data.

- __Service and Data Integration__ : Unsecured data in transit is suspectible to eavasdroping and interception attacks.

- __Multi Tenancy and Physical Security__ : Poor logical segregation may lead to tenants interfering with the security features of other tenants.

- __Incidence Analysis and Forensic Support__ : Due to distributed storage of logs across the cloud, law enforcement agencies may face problems in forensic recovery.

- __Infrastructure Security__ :  Misconfiguration of infrastructure may allow network scanning for vulnerable applications and services.

- __Non-production Environment Exposure__ : Using non-production environments increases the risk of unauthorized access, information disclosure and information modification.


## Cloud Computing Threats

- Data breach/loss

- Abuse and nefarious use of cloud services

- Insecure interfaces and APIs

- Insufficient due diligence

- Shared technology issues

- Unknown risk profile

- Unsynchronized system clocks

- Inadequate infrastructure design and planning

- Conflicts between client hardening procedures and cloud environment

- Loss of operational and security logs

- Malicous insiders

- Illegal access to cloud systems

- Loss of business reputation due to co-tenant activities

- Privilege escalation

- Natural disasters

- Hardware failure

- Supply chain failure

- Modifying network traffic

- Isolation failure

- Cloud provider acquisition

# Cloud Attacks

## Side channel attacks or Cross-guest VM breaches

- The attacker compromises the cloud by placing a malicious virtual machine near to a target system and then launches a side channel attack.

- In a side-channel attack, the attacker uses the information gathered from the system's side channel to infer the secret key.

- The attacker runs a virtual machine on the same physical host as the victims virtual machine and takes advantage of the shared resources to steal data from the victim

- Side channel attacks can be implemented by any co-resident user due to the vulnerabilities in shared technology resources

- Some of these attacks are :

    - Timing attacks

    - Data remanence attacks

    - Acoustic Cryptoanalysis

    - Power monitoring attacks

    - Differential fault analysis


## Wrapping attacks

- A wrapping attack is performed during the translation of the SOAP message in the TLS layer where attacker duplicates the body of the message and sends it to the server as a legitimate user.


## Man-in-the-cloud (MITC) attacks

- MITC attacks are advanced versions of man-in-the-middle (MITM) attacks where the attacker intercepts the communication between the user and the cloud service provider.

- The attacker tricks the victim to installing a malicious code, which plants the attacker's synchronization token to the victim's drive

- then, the attacker steals the victim's synchronization token and uses the stolen token to gain access to the victim's files

- Later, the attacker restores the malicious token with the original token of the victim, thus returning the drive application to its original state and stays undetected.


## Cloud hopper attack

- Cloud Hopper attack are triggered at the managed service providers(MSPs) and their users

- Attackers initiate spear-phishing emails with custom-made malware to compromise the accounts of staff or cloud service firms to obtain confidential information


##  Cloud Cryptojacking

- Cryptojacking is the unauthorized use of a user's computer to mine cryptocurrency.

- Cryptojacking attacks are highly lucrative, which involves both external and rogue internal actors.

- To perform this attack, the attackers leverage attack vectors like cloud misconfigurations,  compromised websites and client or server side vulnerabilities.  


## Cloudborne attacks

- The cloudborne is a vulnerability residing in a bare-metal cloud server that enables the attackers to implant a malicious backdoor in its firmware.

- The malicious backdoor can allow the attacker to bypass the security mechanism and perform various activities such as watching new user's activities or behavior, disabling the app or server, and intercepting or stealing the data.

### Steps are :

- Attacker injects malicious backdoor on bare-metal server

- Server assigned to new customer with persistent backdoor

- Attacker monitors custormer activities

- Attacker exfilterates customer's data via persistent backdoor.


## Enumerating S3 Bucket using lazys3

- Simple storage service (S3) is a scalable cloud storage service used by Amazon AWS where files, folders, and objects are stored via web APIs

- Attackers often try to the find the bucket's location and name to test its security and identify vulnerabilities in the bucket implementation.

- lazys3 is a Ruby script tool that is used to brute-force AWS S3 buckets using different permutations.

- General syntax is :

    - `ruby lazys3.rb HackerOne` : This finds the bucket name for the domain hackerone.com

    - `ruby lazys3.rb HackerOne -p wordlist.txt` : This finds the bucket name for the domain hackerone.com using the wordlist.txt file

    - `ruby lazys3.rb HackerOne -p wordlist.txt -r` : This finds the bucket name for the domain hackerone.com using the wordlist.txt file and also checks the permissions of the bucket.


## Cloud Attack Tools

- [Nimbostratus]()  : A tool used for
- [S3Scanner](https://github.com/sa7mon/S3Scanner)
- [Cloud Container Attack Tool (CCAT)](https://github.com/OWASP/CCAT)
- [Pacu](https://github.com/RhinoSecurityLabs/pacu)


# Cloud Security Countermeasures

## Some of the best practices for securing cloud are :

- Enforce data protection, backup, and retention mechanism

- Enforce SLAs for patching and vulnerability management

- Vendors should regularly undergo AICPA SAS 70 TYPE II audits

- Prohibit user credentials sharing among users, applications and services

- Implement strong authentication and auditing controls

- Implement strong key generation, storage and management, and destruction practices

- Ensure that the cloud undergoes regular security checks and updates

- Ensure that physical security is a 24 * 7 * 365 affair

- Ensure security standards in installation/configuration

- Ensure that the memory, storage, and network access is isolated

- Implement a baseline security breach notification process

- Analyze API dependency chain software modules

### Side channel attacks countermeasures

- Implement a virtual firewall in the cloud server back-end of the cloud computing

- Implement the random encryption and decryption

- Lockdown OS images and applications instances to prevent compromising vectors that might provide access.


### Wrapping Attack Countermeasures

- Use XML schema validation to detect SOAP messages

- Apply authenticated encryption in the XML encryption specification

### MITC Attack Countermeasures

- Use an email security gateway to detect the social engineering attacks

- Harden the policies of token expiration

- Implement cloud access security broker (CASB) to detect the malicious token and monitor the user's behavior

### Cloud Hopper Attack Countermeasures

- Implement multi-factor authentication to prevent compromise of credentials

- Ensure mutual co-ordination between customers and CSPs in case of abnormal incidents or activities.

- Ensure customers are aware and follow the cloud services policies

### Cloud Cryptojacking Countermeasures

- Ensure to implement a strong password policy

- Always preserve three different copies of the data in different locations and one copy off-site

- Implement CoinBlocker URL and IP Blacklist/blackholing in the firewall

### Cloudborne Attack Countermeasures

- CSPs should keep the firmware up-to-date

- Sanitize the server firmware before it is assigned to new customers