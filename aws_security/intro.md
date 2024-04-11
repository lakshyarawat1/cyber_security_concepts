# Cloud Security

## Objectives

- Controllability : Controlling the access to the resources

- Auditability : Tracking the access to the resources

- Visibility : Visibility into the security state of the resources

- Agility : Ability to quickly respond to security events

- Automation : Ability to automate security tasks

### Controllability

- AWS provides methods and tools to manage access control for users, groups and roles, provide temporary security credentials, and manage permissions for resources.

- The AWS IAM (Identity and Access Management) service enables you to control access to AWS services and resources for your users.

- You can use granular permissions for entitites such as users, groups and roles.

- We can allow access to different resources like S3, EC2, RDS, etc.

- You can use the AWS security Token Service(STS) to create and provide trusted users with temporary security credentials that can control access to your AWS resources.

- With AWS CloudHSM, you can manage your own encryption keys using FIPS 140-2 Level 3 validated HSMs.

### Auditability

- AWS services like AWS CloudTrail can help you answer questions such as what actions did a specified user take over a given time period ?

### Visibility

- AWS offers tools to monitor and log your AWS resources and services.

- For example, AWS CloudTrail provides a record of actions taken by a user, role, or an AWS service in your AWS account.

- AWS Config provides a detailed view of the configuration of AWS resources in your AWS account.

- AWS CloudWatch provides monitoring and alerting for your AWS resources and applications.

### Agility and Automation

- AWS provides tools to help you quickly respond to security events.

- For example, AWS CloudTrail can help you identify the actions that a user took over a given time period.

- AWS Config can help you identify the resources that were created or modified over a given time period.

## Shared responsibility Model

- AWS operates on a shared responsibility model.

- AWS is responsible for the security of the cloud, and the customer is responsible for the security in the cloud.

- AWS is responsible for the security of the underlying cloud infrastructure, and the customer is responsible for securing the workloads they deploy in AWS.

### Security in the Cloud

- The customer is responsible for securing the workloads they deploy in AWS.

- This includes securing the operating system, network, and firewall configuration, and the data.

- The customer is also responsible for managing the security configuration of the AWS services they use.

- For example, the customer is responsible for managing the security group and network ACL configurations.

### Security of the Cloud

- AWS is responsible for the security of the underlying cloud infrastructure.

- This includes the hardware, software, networking, and facilities that run AWS Cloud services.

- AWS is also responsible for the security configuration of the managed services that AWS provides.

- For example, AWS is responsible for the security configuration of Amazon S3, Amazon RDS, and Amazon DynamoDB.

