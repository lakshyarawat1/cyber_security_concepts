# Pipeline automation

## Overview

- The pipeline automation is a set of scripts that automate the process of creating and updating pipelines in the CI/CD tool. 

- The scripts are written in Python and use the GitLab API to interact with the CI/CD tool.

## Source code storage

- Considerations when deciding where to store the source code :

    - Access Control
    - Tracked Changes
    - Integrate the source code system with the dev tools
    - Store and actively use different versions of our source code
    - Internal hosting of code, or external

### Version Control

- The version control system is a tool that allows you to manage changes to the source code over time.

- The version control system allows you to:

    - Track changes to the source code
    - Revert to a previous version of the source code
    - Collaborate with other developers
    - Track changes to the source code
    - Branching and merging

## Git

- Git is a distributed version control system that allows you to manage changes to the source code over time.

- Github : A web-based Git repository hosting service.

- Gitlab : A git product used to host your own git server

- Gittyleaks : A tool that searches for sensitive information in the source code.


## Dependency Management

- Dependency management is the process of managing the dependencies of a project.

- Dependency management allows you to:

    - Manage the dependencies of a project
    - Resolve conflicts between dependencies
    - Update dependencies
    - Add new dependencies
    - Remove dependencies

### External VS Internal Dependencies

- External dependencies are dependencies that are not part of the project.

- We don't have control over external dependencies.

- If the framework or CDN goes down, our project will be affected.

- Attackers can discover Zero day vulnerabilities.

- Internal dependencies are dependencies that are part of the project.

- We have control over internal dependencies.

- We can update the dependencies when we want.

- We can fix vulnerabilities in the dependencies.


### Common tools

- Package managers are used for dependency management

- Some of them are :
    
    - Pypi
    
    - NuGet

    - Gems

    For internal dependencies,

    - Artifactory

    - Azure Artifacts

## Automated Testing


### Unit Testing

- Unit testing is a software testing method by which individual units of source code are tested to determine whether they are fit for use.

- In modern pipelines, unit testing can be used as quality gates.

- The tests can be integrated using CI/CD part of the pipeline.

### Integration Testing

- It tests how the small units work when brought together.

- A subset of integration testing is regression testing. It tests if the new features affect the existing features.

These two testings are not performed for security reasons.


### Security Testing

#### Static Application Security Testing (SAST)

- Static Application Security Testing (SAST) is a type of security testing that is performed without executing the code.

- It scans the code for vulnerability. It can be integrated into the development process by developers.

- It is used not as quality gates, but as security gates.


#### Dynamic Application Security Testing (DAST)

- Dynamic Application Security Testing (DAST) is a type of security testing that is performed by executing the code.

#### Penetration Testing

- Penetration testing is a type of security testing that is performed by simulating an attack on the system.


### Common Tools

- Synk and Sonarqube are popular tools for SAST and DAST


## Continuous Integration / Continuous Deployment

- The automated process of integrating code changes into a shared repository and deploying the code to production.

- Instead of waiting until the end of the development cycle when all features are integrated, CI/CD allows developers to integrate code changes into a shared repository multiple times a day.

### Elements of CI/CD Pipeline

- Starting Trigger : The action that kicks off the pipeline process. Ex : Code commit, merge request

- Building Actions : Actions taken to build both the project and the new feature

- Testing actions : Test the project to ensure that new feature doesnot interfere in the existing features

- Deployment actions : Should the pipeline suceed, the deployment action details what should happen with the build

- Delivery actions : Like monitoring the deployment, sending notifications, etc.

- Build Orchestrator : The tool that manages the pipeline build process

- Build agents : Performs the builds

### Common tools

- Jenkins, Gitlab CI, Circle CI, Travis CI, etc.


## Environments

- Environments are the different stages of the pipeline.

- DEV : Development environment, most unstable, weakest security, No customer data should be contained

- UAT : User Acceptance Testing, tests the application before production. Can include security tests as well.

- PreProd : Pre-production environment, mimics the production. Stable and final tests are performed.

- Prod : Production environment, the final stage where the application is live. No updates should be possible here without proper change management. Security is strongest

- DR or HA : Disaster recovery or High Availability environment, used in case of a disaster in the production environment. This is often used for critial applications like banking. They should be exact copy of the Production environment.


### Other notable environments


- Green and Blue environments : Pushing the updates to production. There are two production envs. Blue is running the current version and green is running the newer version. All traffic is gradually shifted to the green env.

- Canary Env : Same as Green/Blue env.

## Common tools

- Kubernetes

