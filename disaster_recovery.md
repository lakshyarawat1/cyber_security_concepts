## Business Continuity (BC)

- Business Continuity is a business level of readiness to maintain critical functions after an emergency or disruption. These events include :
    - Security breaches
    - Natural disasters
    - Power outages
    - Equipment Failures
    - Sudden staff departure

### About

- If key business capability fails, then a quick recovery time is crutial.
- A business continuity has three considerations
    - Resiliency
    - Recovery
    - Contingency

### Components of Business continuity plan

- List of BCP team members, including multiple contact methods and backup members.
- Immediate response procedures and checklists ( security and safety procedures )
- Notification systems and call trees for alerting personnel that the BCP is being enacted.
- Guidance of management , including designation for authority for specific managers
- How and when to enact the plan
- Contact numbers for critical members of the supply chain


### Tools

- Some tools for BC are :

    - Back up : Backing up data is one of the simplest way to ensure BC.
    - Backup as a Service : Similar to backup but a third party service is used to backup data.
    - Point in time and Instant Recovery Copies : Point in time copies or snapshots copy the entire db at regular intervals. Instant recoveryc copies takes snapshots of entire Virtual machine. These copies are stored in off-site or on a virtual machine that is unaffected by the disaster.
    - Cold site : Businesses can set up a basic infrastructure in a second facility known as cold site, where workers can work after any disaster or fire. 
    - Hot site : Similar to cold site, but it also maintains a up-to-date copy of data all the time. More expensive that cold site , but reduces downtime.
    - Disaster Recovery as a Service (DRaaS) : DRaaS provider moves and organisation's computers processing to their own cloud infrastructure in a event of disaster. Businesses pay for these through subscription or a pay-per-use model.
    - Physical Tools :  Physical elements that can support business continuity include fire suppression tools to help data and computer equipment survive a fire, and a back-up power source that supports businesses through short-term power outages.
    - Virtualizaton : Virtualization is one of the few ways to back up a working replica of an organization’s entire computing environment. Businesses can also automate some disaster recovery processes on off-site virtual machines that are unaffected by physical disasters, bringing everything back online faster. Frequent transfer of data and workloads is essential for virtualization to be an effective disaster recovery tool.


## Disaster Recovery

Disaster recovery relies upon the replication of data and computer processing in an off-premises location not affected by the disaster.

## Incident Response

Incident response (IR) is the effort to quickly identify an attack, minimize its effects, contain damage, and remediate the cause to reduce the risk of future incidents.

- Breach is the loss of control, compromise, unauthorized disclosure, unauthorized acquisition or any similar occurance where a person other than an authorized user accesses or potentially accesses identifiable information.
- Event is any observable occcurance in a network or system.
- Incident is an event that actually or potentially jeopardizes the CIA of the system or information.
- Intrusion is the event or combination of events that constitutes a deliberate security incident in which intruder gains or attempts to gain access to a system.
- The Zero day is a previously unknown system vulnerability with the potential of exploitation without risk of detection or prevention because it doesnot, fit recogonized patterns, signatures or methods.

### Goal Of IR

- Primary goal of IR is to be prepared.
- It is aimed at reducing the impact of an incident so as to resume the operations of the system.


### Right plan for IR

- Prepare a team that can handle any type of threat
- Detect and identify the type and severity of the threat once it has occured
- Contain and limit the damage
- Determine its impact and associated risk
- Find and eradicate the root cause
- Mitigate and resolve the attack
- Analyze and modify the plan post-attack to prevent the future ones.

### Incident Response Policy

- Should reference an incident response plan that all employees must follow, depending on their roles in the process.
- The organization's vision, stragety and mission forms the policy.
- The procedure to implement the plan should define the technical process, techniques, checklists and other tools that team will use when responding to incident.

- Some of the components of  incident response plans are :

    - Preparation : 
        - Develop a policy approved by management.
        - Identify critical data and systems, single point of failure.
        - Train staff in incident response.
        - Implement an incident response team
        - Practice Incident identification
        - Identify roles and responsibilities.
        - Plan the coordination of communication between stakeholders.

    - Detection and analysis :
        - Monitor all possible attack vectors.
        - Analyse incident using known data and threat intelligence
        - Priotize incident response
        - Standardize incident documentation

    - Containment :
        - Gather evidence
        - Choose an appropriate containment stragety
        - Identify the attacker.
        - Isolate the attack

    - Post-incident Activity :
        - Identify evidence that may be retained.
        - Document lessons learned.