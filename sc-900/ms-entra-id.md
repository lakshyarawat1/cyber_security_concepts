# Microsoft Entra ID

## Introduction

- Former name is Azure Active directory.
- Cloud based identity and access management service.
- Organizations use MS Entra ID to enable their employees, guests and others to sign in and access the :
    - Internal resources
    - External services 

- Entra Id enables the secure usage of personal devices in a professional way.

### Identity secure score

- It is the percentage that functions as an indicator for how aligned you are with MS's best practices for security.

## Basic terminology

### Tenant 

- MS Entra Tenant is an instance of Entra ID in which information about a single organization resides including org. objects such as users, groups, devices and applications registrations.
- Tenant also contains access and compliance policies.
- Each tenant has unique ID ( tenant Id ) and a domain name.
- It serves as a security and administrative boundary, allowing the org to manage and control access to resources, apps, devices and services

### Directory

- Directory is a logical container within a tenant that holds and organizes that various resources and objects .
- Directory is like a database or catalog of identities and resources associated with an org's tenant.
- One tenant can have only one directory.

### Multi-tenant 

- A multi-tenant org is an org that has more than one instance of Entra ID.
- Reasons can be having multiple subsidiaries or business units.

## Types of Identities

- Entra Id's can be assigned to : 
    - People
    - Physical devices
    - Software-based objects like applications or VMs

### User

- User Identities represents people such as employees and external users.
- Users are characterized by how they authenticate and the user type property.
- The user type property describes the user's relationship with the org or its tenancy.
- Some types are :

    - Internal Member : Considered employees of the org. Authenticates internally via their org Entra ID, the object created has the user type of member.
    
    - External Guest : Includes consultants, vendors and partners. Authenticates using an external Entra account or Identity provider. UserType is Guest.

    - External member : This is common in multi-tenant org. Here the members of a subsidiary can login to main org's domain with their entra id. UserType is member.

    - Internal guest : When org collaborates with distributers, suppliers and vendors. They have guest Entra Ids i.e. internal, User Type is guest

### Workload Identities

- A workload identity is assigned to a software workload.
- It enables software to access other services and resources.
- Securing workload identity is more important as it deals with more credentials to access resources.

### Application and Service principal

- A service principal is essentially, an identity of an application.
- To get its IAM functions, application must be registered with MS Entra ID to enable its integration.
- Once registered, a service principal is created in each MS Entra tenant where the app is used,
- Service principal enables core features like authentication and authorization of app to resources that are secured by tenant.

xc### Managed Identities

- Type of service principal that are automatically managed in Entra Id
- No extra cost
- Does not require any developers to manage credentials.

- There are two types of managed identities :   
    
    - System assigned : Managed ids are enabled directly on the resource. System assigned ids are tied to the lifecycle of the resource. The id gets deleted with the resource is terminated.

    - User assigned : Here user creates a managed Id and assign it to one or more instance of Azure services. Deleting the resource doesnot delete the identity, it must be explicitly deleted. 

### Device

- Device identity gives admin info they can use when making access or config decisions.
- Ways of setting up devices are  :
    - MS Entra registered devices : personal devices registered
    
    - MS Entra Joined : A device joined to MS Entra Id   through an org account. These are usually owned by the org.

    - MS Entra hybrid joined devices : Orgs with existing on-premises AD implementation can benefit from functionality by implementing hybrid joined devices.

IT admins can use MS Intune, a cloud based service that focuses on mobile device management (MDM) and mobile application management (MAM) to control how an organization's devices are used.

### Groups

- If there are identities with same access needs, you can create a group
- Give access rights to a group instead of giving and revoking them individually to all members.
- There are two types of groups : 

    - Security group : Used to manage user and device access to shared resources. Members can include users, devices, other groups and service principals. Creating groups requires a MS Entra Admin role.
    
    - MS 365 group : Referred to as a distribution group, used for grouping users according to collaboration needs. The default is to allow users to create MS 365 groups, admin role not required.

### Hybrid identity

- MS Identity solutions span on-premises and cloud based capabilities. These solutions create common identities for all resources, apps and services.

- This identity is called hybrid identity.

- Hybrid identity is accomplished through provisioning and synchronization.

    - Provisioning : The process of creating user accounts and assigning them to resources.
    
    - Synchronization : The process of keeping user accounts and their attributes in sync across on-premises and cloud based directories.

- One method is through MS Entra Cloud Sync. It uses MS Entra Cloud provisioning agent.

- The agent acts as a bridge between on-premises AD and MS Entra ID.

- The Entra Cloud Sync provisioning agent uses the System for Cross-domain Identity Management (SCIM) specification with Entra ID to provision and deprovision users and groups.

- SCIM is a standard that is used to automate the exchanging of user or group indentity between ID domains.

### External Identity

- Using external identity, one can allow external users to securely access your apps and resources.
- There are two ways to configure your tenant for external identities :

    - A workforce tenant configuration is for your employees, internal business apps and the organizational resources. You can invite business external partners and guests to your workforce tenant.

    - An external tenant configuration is used exclusively for External ID scenarios where you want to publish apps to consumers or business customers.

- Collaborate with business guests : 

    - Use External Id for B2B collaboration.
    - Share access to resources while maintaining control over your own corporate data.
    - Here, guests login with their home credentials / org credentials.

- Secure apps for consumers and business customers :

    - Use External ID to quickly add authentication and customer Identity and access management ( CIAM ) to your apps.

    - External ID includes CIAM solutions features like self-service registration, personalized sign-in experience including single sign-on (SSO).

## Authentication in Entra Id

- Different authentication methods in Entra are :

### Passwords

- Most common method for authentication.
- The use of passwords should be supplimented or replaced with other methods like MFA.

### Phone

- Phone based authentication can be of two types :

    - SMS-based authentication : User don't need to sign in with username and password, user instead enters their registered phone number and recieves a text message with verification code.

    - Voice call verification.

### OATH

- Open Authentication or OATH is an open standard for strong authentication.
- OATH specifies how time-based, one time passwords (TOTP) codes are generated.
- __Software OATH Token__ are typically applications. Entra Id generates secret key or seed, input into the app and used to generate the OTP.
- __OATH Hardware tokens__ are small hardware devices that look like a key fob that displays the code that refreshes every 30 or 60 seconds.

- OATH are supposed to be only secondary forms of authentication in MS Entra Id, to verify the identity during self-service password reset(SSPR) or multifactor authentication.

### Passwordless Authentication

- Biometrics like Windows hello for Business, or FIDO2 security keys can be used for passwordless authentication.

- Fast Identity Online (FIDO) is an open standard for passwordless authentication.
- FIDO allows users and organizations to leverage the standard to sign in to their resources using an external security key or a platform key build into the device.
- FIDO2 is the latest version of FIDO and is supported by MS Entra Id.
- FIDO2 security keys are an unphishable standards-based passwordless authentication method.
- USB drives, bluetooth or NFC based devices.
- Primary authentication 

### Microsoft Authenticator Application

- Primary form of authentication
- User must download a phone app and register their account.

### Certificate-based authentication

- MS Entra Id certificate-based authentication (CBA)
- authenticates directly with X.509 certificates against their Entra ID.
- Supported only as a primary form of passwordless authentication.
- X.509 certificates are part of Public key Infrastructure.
- They are digitally signed documents that binds an Id to its public key.

### Self Service Password reset

- Feature of MS Entra ID that allows the users to change or reset their passwords, without admin or help desk involvement
- Benefits include : 
    - Reduces IT support cost 
    - SSPR allows users to get back to work faster and be more productive.
    - Admin can change settings to accomodate new security requirements and roll these changes to users without disrupting their sign-in.
    - SSPR includes robust audit logs.

- If a user is locked or they forget or want to change their password, they can follow a prompt to reset it and get back to work.
- To use SSPR, user must be :
    - Assigned to MS Entra Id license.
    - Enabled SSPR by admin.
    - Registered with an authentication method.

### Password protection and management

- Reduces risk of setting weak passwords.
- Detects and blocks known weak passwords and their variants, and even passwords specific to the organization.
- Default global banned password lists are automatically applied to all users in a tenant.
- You can even set a custom banned list.
- Custom banned lists can include :
    - Brand names
    - Product names
    - Locations, such as company headquarters
    - Company-specific terms
    - Abbrevations that have specific company meanings.

### Protection against password spray

- Most spray attacks submits only a few weakest passwords against each of the accounts of the enterprise.
- Technique allows the attacker to quickly search for an easily compromised account and avoid potential detection threshold.

## Access Management in Entra Id

### Conditional Access

- Access based on the policies that are created and managed in Entra Id.
- A Conditional Access policy analyzes signals including user, location, device, application and risk to automate decisions for authorizing access to resources.
- Simple if-then statements.

- Has two components : 
    - Assignments 
        - Assignment portion of policy controls who, what, where and when of conditional access policy (CAP).
        - All assignments are logically ANDed.
        - Assigments include :
            - Users assign who the policy will include or exclude. 
            - Target resources includes :
                - Cloud Apps : List of apps or services that include in-build MS Applications, like Office 365, Azure, Dynamics 365.

                - User Actions : Like register security info or register join device.
                
                - Global Secure Access (preview) : Secure the traffic that passes through GSA service.

                - Authentication Context : Further secure data and actions.

            - Network allows you to control user access on user's network or physical location.

            - Conditions define where and when the policy will apply. Multiple conditions can be fine-grained and specific CAP. Some conditions include : 
                
                - Sign-in risk and user risk : Suspecious actions related to user accounts in a directory and trigger a policy.

                - Insider risk : data governance, data security and risk and compliance config for MS purview.

                - Device Platform 
                - Client apps 
                - Filters for devices
                
    - Access Controls 
        - When access control is applied, an informal decision is reached on whether to block access, grant access with extra verification, or apply a session control to enable a a limited experience.

        - Common decisions are :
            - Block access
            - Grant access
            - Session : Limited access
        
### Global Secure Access

- Unifying term for both MS Entra Internet Access and Entra Private Access.
- ME Internet Access secures access to SaaS apps including MS Services, and public internet apps while protecting users, devices and data against internet threats.
- Provices secure access to private, coorporate resources.
- Called Security Service Edge (SSE) solution.
- Addresses challanges like : 
    - Need to reducing risk to lateral movement through a compromised VPN tunnel.
    - Need to put a perimeter around internet-based assets.
    - Need to improve service in remote office locations

- Solution employs a Global Secure Access client that gives an organization control over network traffic at the end-user computing device.
- Orgs gain ability to route specific traffic profiles through Internet Access and Private Access.

- __Private Access__ 
    - For VPN solutions
    - Can be deployed to block lateral attack movements, reduce excessive access, and replace legacy VPNs. 
    - Working explained :
        - Given a set of private resources you want to secure
        - You set up a new enterprise app that serves as a container for those private resources.
        - New app has a network connector that serves as a broker between Private Access service and the resource a user wants to access.
    
    - Entra Id provides two ways in which you can set up the private resources:

        - Quick Access : You determine which private resources to add to the 'container' or enterprise app. which we call Quick Access App. Private resources are defined by FQDN, IP addresses or address range and ports to access them. This info is reffered to as a Quick Access app segment.

        - Global Secure Access App : a.k.a. Per-app Access, more granular approach. Multiple containers can be created. For each, you define properties of the private resource, and you assign groups and users and assign conditional access policies.

    - __Internet Access__ 

        - Secure Web Gateway (SWG) protects users from web-based threats by filtering internet traffic and enforcing security policies.
        - Provides an identity centric SWG solution for SaaS app, including MS Services, and other traffic.
        - Some key features are :
            - Protection against user id or token theft
            - Tenant restrictions to prevent data exfiltration to other tenants.
            - Internet access traffic forwarding profile policies to control which sites can be accessed.
            - Web content filtering to regulate access to specific sites.
    
    - __Global Secure Access Dashboard__ 

        - Provides visualizations of the network traffic acquired by the Private and internet access services.
        - The dashboard compiles the data from your network configs, including devices, users, and tenants into widgets
        - Some widgets are :
            - GSA snapshot
            - Alerts and notifications
            - Usage profiling
            - Cross-tenant access
            - Web category filtering
            - Device status

### Roles and RBAC

- Built-in roles fixed with set of permissions.
- Some of them are :
    - Global Admin : Access to all admin features of Entra Id. Person who signs up for the tenant becomes the global admin.
    
    - User Admin : Can create and manage all aspects of users and groups. Manages support tickets and monitors service health.
    - Billing admin : Makes purchases, manage subscriptions, and support tickets, and monitors service health.

- Custom roles gives flexibility to create roles with specific permissions.
- Granting permission using custom roles is a two step process, create role, and assign the role to a user or group by creating role assignment.

- MS Entra RBAC VS Azure RBAC : 

    - Entra roles control access to MS entra resources such as groups, users, and apps.
    - Azure roles controls access to Azure resources like VMs and storage in Azure cloud.

## Identity governance

- Balancing identity security with user productivity
- As employees' roles change within an org, you can use MS Entra ID Governance to automatically ensure that the right people have right access to the right resources.
- Id governance gives :
    - Govern Id lifecycle
    - Govern access lifecycle
    - Secure privileged access for admin

### Identity lifecycle

Automating ID lifecycle in an organization

- Inbound provisioning from HR sources
- Lifecycle workflows to automate workflow task that run 