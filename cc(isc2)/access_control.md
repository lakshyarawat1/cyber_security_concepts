# Access Control Concepts

- A control is safeguard or countermeasure designed to preserve CIA of data.
- Access control involves limiting what objects can be available to what subjects according to what rules.

- Access is based on three elements :
    - Subjects : 
        - A subject is any entity that requests access to our assets.
        - Initiator or a request for service.
    - Objects :
        - An Object is a device, process or person that responds to the request of a service.
        - Subject is active but an object is passive in that it takes no action until called upon by the subject.
        - An object is a building, computer, file ,database, printer or scanner, server, memory.
        - Anything that provides the subject a service.
        - Object may have a classification
    - Rules :
        - An access rule is the instruction developed to allow or deny access to an object by comparing the validated identity of the subject to access control list.
        - Compares multiple attributes to determine appropriate access.
        - Allow access to the object.
        - Define how much access to be provided.
        - Apply time based access

## Privileged Accounts

- Privileged accounts are those with permissions beyond those of normal users, such as managers and administrators.
- Security analysts, system administrators and IT help support desks.

## Physical Access Control

- Badge system and gate entry
- Environmental design :  Crime prevention through environmental design
- Biometrics

## Logical Access Control 

A logical access control system requires the validation of an individual's identity through some mechanism, such as a PIN, card, biometric, or other token. It has the capability to assign different access privileges to different individuals depending on their roles and responsibilities in an organization.

## Principle of least privilege

-  the principle of least privilege is a crucial aspect of any security strategy as it helps to minimize the risk of data breaches, unauthorized access, and other security threats.
-  states that a user or process should only be granted the minimum level of access or permission necessary to perform their tasks or functions. 
- In other words, a user should only have access to the resources and information that they need to do their job and nothing more.
-  By granting the lowest level of access necessary, organizations can limit the damage that can be caused by an attacker who gains access to a user's account.

## Segregation of duties (SoD)

- Segregation of duties is a security principle that involves dividing critical functions and responsibilities among multiple individuals or teams to prevent any one person from having too much control or influence over a particular process.

-  This helps to prevent fraud, errors, and other security risks that may arise from having too much power concentrated in one individual.

## How users are provisioned

- A new employee : 
    - The hiring managers sends a request to the security administrator for new user ID
    - The admin sets the privileges of the user according to the role

- Change of position : 
    - When an employee is promoted, their permissions and access controls may change as defined by new role
    - Any access no longer needed will also be deleted.

- Seperation of employement :  
    - When employee leaves a company, their accounts must be disabled for a period before they are deleted to preserve the integrity of any audit trails or files that may be owned by the user.
    - Privilages should be repealed.



## Discretionary access control

Discretionary access control is the principle of restricting access to objects based on the identity of the subject 
- In DAC, the policy specifies that a subject who has been granted access to information can do one or more of the follwing activities :    
    - Pass the information to other subjects or objects
    - Grant its privilages to other subjects
    - Change security attributes on subjects, objects, info systems or system components
    - Choose the security attributes to be associated with new user pr objects

The user with access to the file can give its privilage to any other person.



## Mandatory access control (MAC)

A means of restricting access to system resources based on the sensitivity (as represented by a label) of the information contained in the system resource and the formal authorization (i.e., clearance) of users to access information of such sensitivity.