# Windows active directory (AD)

- Active Directory is a directory service developed by Microsoft that is used to store information about resources on a network and to manage user access to those resources.

## Windows Domain

- A Windows domain is a collection of computers that share a common user account database. The computers in the domain can be part of a local network or can be located in different parts of the world. The domain is managed by a domain controller, which is a server that manages security and access to the resources in the domain.

### Advantages

- Centralized management of users and resources

- Simplified administration

- Enhanced security

- Scalability

## Active Directory Domain Service

- Active Directory Domain Services (AD DS) is a server role in Windows Server that allows you to manage users, groups, and computers in a network.

- AD DS provides a distributed database that stores and manages information about network resources and application-specific data from directory-enabled applications.

### Users

- Users are objects in AD DS that represent people who use the network.

- Users can log on to the network and access resources.

- Users can be members of groups, which can be used to assign permissions to resources.

- Users can be people or services.

### Machines

- Machines are objects in AD DS that represent computers that are part of the network.

- There is a specific naming scheme for machines in AD DS.

### Security Groups

- Security groups are objects in AD DS that are used to assign permissions to resources.

- Security groups can contain users and other security groups.

- Security groups include :

  - **Domain Admins** : Members of this group have full control of the domain.

    - **Server Operators** : Members of this group can administer domain controllers. Cannot get admin privileges

    - **Backup Operators** : Members of this group can back up and restore files on domain controllers.

    - **Account Operators** : Members of this group can administer domain user, group, and computer accounts.

    - **Domain Users** : Members of this group can perform most common tasks, such as running applications and using printers.

    - **Domain Controllers** : Members of this group are domain controllers.

## Managing users in AD

- Deleting existing OUs and users, need permissions to do so.

- Deletion is protected by accidental deletion, it needed to be disabled first.

- Any user inside the deleted OU will be deleted as well.

- Giving specific users control over a OU is called delegation.

- Delegation can be done by right clicking on the OU and selecting delegate control.

- Delegation can be done to a group or a user.

## Managing Computers in AD

- By default, all computers are added to the default Computers container.

- Devices can be divided into these categories :

  - **Workstations** : Computers that are used by users to perform tasks and work.

  - **Servers** : Computers that provide services to other computers.

  - **Domain Controllers** : Servers that manage the security and access to resources in the domain.

## Group policies

- Group policies are used to manage the settings of users and computers in a domain.

- Group policies can be used to manage :

  - Security settings
  - Software installation
  - Folder redirection
  - Scripts
  - Administrative templates
  - Group policy preferences
  - Group policy settings

- Security filtering is used to apply group policies to specific users or groups.

- By default, group policies are applied to all users and computers in the domain.

- GPO can be linked to a domain, site, or OU.

### GPO distribution

- GPOs are distributed to domain controllers using the SYSVOL folder.

- The SYSVOL folder is a shared folder that contains the public files that must be shared for common access and replication.

### Creating GPO

- Block non-IT users from accessing control panel.

- Make workstations and servers lock their screens after 10 minutes of inactivity.

## Authentication Method

- When using windows domains, all the passwords are stored in the Domain controller. Whenever anyone tries to authenticate using domain credentails, they have to do it through the domain controllers.

- Two protocols used for network authentication in windows domains are :

  - Kerberos : Default

  - NetNTLM : Legacy authentication method for backward compatibility

### Kerberos Authentication

- Users who log into a service using Kerberos will be assigned tickets.

- Think of tickets as proof of a previous authentication.

- Users with tickets can present them to a service to demonstrate they have already authenticated into the network before and are therefore enabled to use it.

## NTDS.DIT

- The NTDS.DIT file is the main database file for the Active Directory Domain Services.

- It is the main file that stores all the information about the domain, including users, groups, and computers.

- When attacking, this file is the target

- The file is located in the %SystemRoot%\NTDS folder.

## Working / Setting Up

- Create a domain controller in windows server.

- Create a new OU named groups and add all security groups to it.

- Add new users and groups.