# IAM ( Identity Access Management )

- IAM is a web service that helps you securely control access to AWS resources for your users.

- It enables you to create and manage users and groups and use permissions to allow and deny their access to AWS resources.

- IAM is a feature of your AWS account offered at no additional charge.

- You can use IAM to control who can use your AWS resources (authentication) and what resources they can use and in what ways (authorization).

- IAM is a global service, and the permissions that you create in one region will apply to all regions.

## IAM Provides ..

### Authentication

- IAM provides a way to control access to AWS resources using the following authentication methods:

  - **Username and Password**: You can create a username and password for your AWS account.

  - **Access Key**: You can use access keys to sign programmatic requests that you make to AWS.

  - **Multi-Factor Authentication (MFA)**: You can add an extra layer of security to your account by using MFA.

### Authorization

- IAM provides a way to control access to AWS resources using the following authorization methods:

  - **Policies**: You can attach policies to users, groups, and roles to define the permissions that they have.

  - **Resource-based policies**: You can attach policies to resources to define the permissions that they have.

  - **IAM roles**: You can define roles that specify the permissions that the entity that assumes the role has.

  - **Identity-based policies**: You can attach policies to users, groups, and roles to define the permissions that they have.

### Best Practice

- Create IAM Policies, attach them to groups and assign users to groups. This allows you to manage user privileges more efficiently by managing the permissions of the group.

## IAM Terminologies

- **IAM Entity**: An IAM entity is a user, group, or role that has specific permissions.

- **IAM User**: An IAM user is an entity that you create in AWS to represent the person or service that uses it to interact with AWS.

- **IAM Identity**: An IAM identity is a user, group, or role that has specific permissions.

- **Principle**: An entity that uses an IAM identity to interact with AWS. External users.

## IAM requests

- IAM requests are authenticated using the AWS signature, which is a hash-based message authentication code (HMAC) that is calculated using the secret access key.

- The signature is used to verify the identity of the sender and the integrity of the message.

### Components

- **Actions or Operations**: The actions that the user is allowed to perform.

- **Resources**: The resources that the user is allowed to access.

- **Principal**: The user, group, or role that is allowed to perform the actions on the resources.

- **Environment data**: The data that is used to verify the identity of the sender and the integrity of the message.

- **Resource Data**: The data related to rosources.

### Endpoints

- To connect to AWS, you must use a URL of the entry point for that service.

- The AWS software development kits (SDKs) and the AWS Command Line Interface (CLI) use the default endpoint to connect to the service.

- You can use the default endpoint or specify a different endpoint to connect to the service.

- The endpoint policy is a JSON policy that specifies the permissions that are allowed or denied for a specific endpoint.

- The endpoint policy is used to control access to the endpoint.

## IAM Roles

- An IAM role is an entity that defines a set of permissions that an entity that assumes the role has.

- You can use roles to delegate permissions to entities that you trust.

- AWS security token service (STS) is a web service that enables you to request temporary, limited-privilege credentials for IAM users or for users that you authenticate (federated users).

- You can use STS to create roles that specify the permissions that the entity that assumes the role has.

### Principle of least privilege

- The principle of least privilege is a security best practice that states that you should grant only the permissions that are required to perform a task.

- You should grant the minimum permissions that are required to perform a task.

## IAM Policies

- An IAM policy is a JSON document that defines the permissions that are allowed or denied for a user, group, or role.

- You can attach policies to users, groups, and roles to define the permissions that they have.

- You can use policies to control access to AWS resources.

- There are two types of policies: identity-based policies and resource-based policies.

- **Identity-based policies**: You can attach policies to users, groups, and roles to define the permissions that they have.

- **Resource-based policies**: You can attach policies to resources to define the permissions that they have.

- You can use the AWS Management Console, the AWS Command Line Interface (CLI), or the AWS SDKs to create and manage policies.

## Identity Federation

- Identity federation is a way to allow users to access AWS resources using their existing credentials.

- Identity providers are trusted entities that provide authentication and authorization services.

- Service providers are entities that provide resource access to users.

- Two AWS services that support identity federation are AWS Single Sign-On (SSO) and AWS IAM.

### AWS Single Sign-On (SSO)

- AWS Single Sign-On (SSO) is a service that enables you to manage access to AWS accounts and business applications using a single set of credentials.

- You can use AWS SSO to manage access to AWS accounts and business applications.

- AWS SSO provides a single sign-on experience for users.

### AWS Directory Service

- AWS Directory Service is a service that enables you to connect your AWS resources to an existing on-premises Microsoft Active Directory or to set up a new, standalone directory in the AWS Cloud.

### Amazon cognito

- Amazon Cognito is a service that enables you to add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily.

- You can use Amazon Cognito to manage user access to your web and mobile apps.

- Amazon Cognito provides a secure, scalable, and reliable user directory that you can use to manage user access to your web and mobile apps.


## AWS Organizations

- AWS Organizations is a service that enables you to centrally manage and govern your AWS accounts.

