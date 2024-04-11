# Intro

## Dev Sec Ops

- DevSecOps is a set of practices that combines software development (Dev) and IT operations (Ops) with security (Sec).

- It aims to shorten the development life cycle and provide continuous delivery with high software quality.

- DevSecOps is a culture that promotes collaboration between development, security, and operations teams.

### Shifting left

- This means that DevOps teams focus on instilling security from the earliest stages in the development lifecycle and introducing a more collaborative culture between development and security.

- This approach is called "shifting left" because it moves security to the left of the development pipeline.

## Secure SDLC

- Secure Software Development Life Cycle (SDLC) is a systematic process for developing software that emphasizes security at every stage of the development process.

### Problems with SDLC

- Traditional SDLC models focus on security at the end of the development process.

- This approach leads to security vulnerabilities and bugs that are difficult to fix.

- Secure SDLC aims to address these issues by integrating security into every phase of the development process.

### Implementing SSDLC

- Perform gap analysis :

  - Identify security gaps in the current development process.

- Create Software Security Initiatives :

  - Establish realistic security goals and objectives.

- Formalize processes

- Invest in security training

### Processes

- Risk Assessment : Done in planning and design phase of SDLC

- Threat Modelling : Done in design phase of SDLC

- Code scanning / review : Done in coding phase of SDLC

- Security Assessments : Done in testing phase of SDLC

## Risk Assessment

- Risk assessment is the process of identifying, analyzing, and evaluating potential risks to an organization.

- Assume the target will be attacked and consider the motivating factor for the attack

- Then evaluate risks and cost on worst-case scenario

- Complexity of the attack

### Qualitative Risk Assessment

- Qualitative risk assessment is a subjective analysis of the risk based on the probability of occurrence and the impact of the risk.

- It is based on expert judgment and experience.

- Classify the risks

- Risk = Severity \* Likelihood

- Do not use numbers to quantify the risk

### Quantitative Risk Assessment

- Quantitative risk assessment is an objective analysis of the risk based on numerical values.

- It is based on data and statistics.

- Use numbers to quantify the risk

## Threat Modelling

- Threat modelling is the structured process of identifying potential security threats and prioritising techniques to mitigate attacks so that data or assets that have been classified as valuable or of higher risk during risk assessment, such as confidential data, are protected.

- Threat modelling is done in the design phase of the SDLC.

### Methods

- STRIDE

  - Spoofing identity

  - Tampering with data

  - Repudiation

  - Information disclosure

  - Denial of service

  - Elevation of privilege

- DREAD

    - Damage potential
    
    - Reproducibility
    
    - Exploitability
    
    - Affected users
    
    - Discoverability

- PASTA

    - Process for Attack Simulation and Threat Analysis

    - Asset identification
    
    - Identify threats
    
    - Identify vulnerabilities
    
    - Identify attack vectors
    
    - Identify security controls
    
    - Identify residual risk


## Security Assessments

- Security assessments are the process of evaluating the security of an organization's information system by identifying, analysing, and mitigating security vulnerabilities.

- Security assessments are done in the testing phase of the SDLC.

### Types of Security Assessments

#### Vulnerability Assessment

- Vulnerability assessment is the process of identifying, quantifying, and prioritizing vulnerabilities in a system.

- It is done by using automated tools to scan the system for known vulnerabilities.

- Vulnerability assessment is a proactive approach to security.

#### Penetration Testing

- Penetration testing is the process of simulating a cyber attack on a system to identify and exploit security vulnerabilities.

- It is done by using manual techniques to exploit vulnerabilities that cannot be detected by automated tools.

- Penetration testing is a reactive approach to security.


## Methodology


### Microsoft SDL

- Microsoft Security Development Lifecycle (SDL) is a software development process that helps developers build more secure software and address security vulnerabilities.

- It is a set of best practices, guidelines, and tools that help developers integrate security into the software development process.

- SDL principles include :

  - Secure by design

  - Security by default

  - Secure by deployment

  - Communications


### OWASP SDLC

- OWASP Software Development Life Cycle (SDLC) is a set of best practices, guidelines, and tools that help developers build more secure software.

- Data is collected to assess training effectiveness

- In-process metrics are used to confirm process compliance

- Post-release metrics are used to guide future changes

- SDL places heavy emphasis on understanding the cause and effect of security vulnerability.

- A development team must complete the sixteen mandatory security activities to comply with the OWASP SDLC.

