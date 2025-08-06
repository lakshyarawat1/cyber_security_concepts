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

 The most prominent threat actors are known as Advanced Persistent Threats (APT), which are highly skilled groups of attackers, usually sponsored by nations or organised criminal groups.

 ## Red teaming engagements

 - A group would take the role of a red team to simulate attack techniques to test the reaction capabilities of a defending team, generally known as blue team, against known adversary strategies. 
 - Every red team engagement will start by defining clear goals, often referenced as crown jewels or flags, ranging from compromising a given critical host to stealing some sensitive information from the target.
 -  Usually, the blue team won't be informed of such exercises to avoid introducing any biases in their analysis. 

 - Red team engagements also improve on regular penetration tests by considering several attack surfaces:

    - Technical Infrastructure: Like in a regular penetration test, a red team will try to uncover technical vulnerabilities, with a much higher emphasis on stealth and evasion.
    - Social Engineering: Targeting people through phishing campaigns, phone calls or social media to trick them into revealing information that should be private.
    - Physical Intrusion: Using techniques like lockpicking, RFID cloning, exploiting weaknesses in electronic access control devices to access restricted areas of facilities.

- The red team exercise can be run in several ways:

    - Full Engagement: Simulate an attacker's full workflow, from initial compromise until final goals have been achieved.
    - Assumed Breach: Start by assuming the attacker has already gained control over some assets, and try to achieve the goals from there. As an example, the red team could receive access to some user's credentials or even a workstation in the internal network.
    - Table-top Exercise:  An over the table simulation where scenarios are discussed between the red and blue teams to evaluate how they would theoretically respond to certain threats. Ideal for situations where doing live simulations might be complicated.

## Teams

- Red Cell : A red cell is the component that makes up the offensive portion of a red team engagement that simulates a given target's strategic and tactical responses.

- Blue Cell : The blue cell is the opposite side of red. It includes all the components defending a target network. The blue cell is typically comprised of blue team members, defenders, internal staff, and an organisation's management.

- White Cell : Serves as referee between red cell activities and blue cell responses during an engagement. Controls the engagement environment/network. 

### Roles 

- Red Team Lead : Plans and organises engagements at a high level—delegates, assistant lead, and operators engagement assignments.

- Red Team Assistant Lead : Assists the team lead in overseeing engagement operations and operators. Can also assist in writing engagement plans and documentation if needed.

- Read Team Operator : Executes assignments delegated by team leads. Interpret and analyse engagement plans from team leads.

