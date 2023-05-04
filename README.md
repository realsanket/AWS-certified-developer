# AWS-certified-Developer - Associate 
- [AWS-certified-Developer - Associate](#aws-certified-developer---associate)
  * [What is Cloud Computing?](#what-is-cloud-computing-)
    + [Benefits of Cloud Computing](#benefits-of-cloud-computing)
    + [Features of Cloud Computing](#features-of-cloud-computing)
      - [Elasticity vs Scalability](#elasticity-vs-scalability)
    + [Types of Cloud Computing](#types-of-cloud-computing)
    + [Types of Cloud Computing Deployment Models](#types-of-cloud-computing-deployment-models)
  * [AWS 🌤️](#aws----)
    + [History of AWS 📜](#history-of-aws---)
    + [AWS Numbers and Facts 🧑🏼‍🏭](#aws-numbers-and-facts--------)
    + [AWS Global Infrastructure 🌎](#aws-global-infrastructure---)
    + [AWS Global Infrastructure Map 🗺️](#aws-global-infrastructure-map----)
  * [AWS Identity and Access Management (IAM) 🔑](#aws-identity-and-access-management--iam----)
    + [Terminologies 🙋🏻‍♂️](#terminologies--------)
      - [IAM Entities](#iam-entities)
      - [IAM Permissions](#iam-permissions)
      - [IAM Policy Structure](#iam-policy-structure)
      - [IAM Roles](#iam-roles)
    + [Password Policy 😵](#password-policy---)
    + [Multi-Factor Authentication (MFA)🔐](#multi-factor-authentication--mfa---)
      - [How to enable MFA in AWS? 🤔](#how-to-enable-mfa-in-aws----)
    + [How Can Users Access AWS? 🤔](#how-can-users-access-aws----)
      - [AWS Command Line Interface (CLI) 🖥️](#aws-command-line-interface--cli-----)
        * [How to install AWS CLI? 🤔](#how-to-install-aws-cli----)
        * [How to configure AWS CLI? 🤔](#how-to-configure-aws-cli----)
        * [How to use multiple AWS accounts in AWS CLI? 🤔](#how-to-use-multiple-aws-accounts-in-aws-cli----)
      - [AWS Software Development Kits (SDKs) 🖥️](#aws-software-development-kits--sdks-----)
        * [How to install AWS SDKs? 🤔](#how-to-install-aws-sdks----)



## What is Cloud Computing?

Cloud computing is the on-demand delivery of compute power, database storage, applications, and other IT resources through a cloud services platform via the internet with pay-as-you-go pricing.

### Benefits of Cloud Computing

- Trade capital expense for variable expense
- Benefit from massive economies of scale
- Stop guessing capacity
- Increase speed and agility
- Stop spending money running and maintaining data centers
- Go global in minutes

### Features of Cloud Computing

- Shared Responsibility Model- Cloud provider is responsible for security of the cloud, customer is responsible for security in the cloud.
- Elasticity - Ability to scale up or down based on demand.
- Disaster Recovery - Ability to recover from a disaster.
- Scalability - Ability to scale up or down based on demand.
- High Availability - Ability to stay up and running.
- Fault Tolerance - Ability to stay up and running even when a component fails.
- Economies of Scale - Ability to provide a service at a lower cost due to size.
- Agility - Ability to move quickly.

#### Elasticity vs Scalability

Elasticity is growing up the existing resources on demand and shrinking them back when the demand decreases.Whereas Scalability is adding more resources on demand and removing them when the demand decreases.

### Types of Cloud Computing

- Infrastructure as a Service (IaaS) - Provides the infrastructure like servers, storage, network, etc.
- Platform as a Service (PaaS) - Provides the platform to build applications.
- Software as a Service (SaaS) - Provides the software as a service.
- Function as a Service (FaaS) - Provides the functions as a service.

### Types of Cloud Computing Deployment Models

- Public Cloud - Cloud resources owned and operated by a third-party cloud service provider, delivered over the public internet and available to anyone who wants to purchase them.
- Private Cloud - Cloud resources used exclusively by a single business or organization.
- Hybrid Cloud - Cloud resources that are a combination of public and private cloud resources.

## AWS 🌤️

Amazon Web Services (AWS) is a secure cloud services platform, offering compute power, database storage, content delivery and other functionality to help businesses scale and grow.

### History of AWS 📜

- 2002 - AWS started as a private service for Amazon.com.
- 2003 - AWS started offering services to other organizations.
- 2004 - AWS started offering SQS and EC2.
- 2006 - Relaunched S3 and EC2.
- 2007 - Lauched into Europe.
- and so on...

### AWS Numbers and Facts 🧑🏼‍🏭

- AWS is the market leader in cloud computing.
- AWS has 32% of the market share.
- AWS has 175+ services.
- AWS has 77 availability zones.
- AWS has 245 points of presence in 60 countries.
- AWS has 5 million active customers.
- AWS has 1 million active enterprise customers.

### AWS Global Infrastructure 🌎

- AWS Regions - A region is a geographical area that consists of two or more availability zones.us-east-1, us-east-2, us-west-1, us-west-2 are some examples of regions.
- AWS Availability Zones - An availability zone is one or more discrete data centers with redundant power, networking, and connectivity in an AWS region.us-east-1a, us-east-1b, us-east-1c, us-east-1d, us-east-1e are some examples of availability zones.
- AWS Data Centers - A data center is a physical building or an entire campus of buildings that house a large number of servers.
- AWS Edge Locations - An edge location is a data center owned by a third-party service provider that is used to cache content.

### AWS Global Infrastructure Map 🗺️

![AWS Global Infrastructure Map](https://d1.awsstatic.com/global-infrastructure/maps/Cloudfront-Map_9.24_2x.2eeac6e52bf404816c6d0aac3edbeb7b6b87fdaa.png)

## AWS Identity and Access Management (IAM) 🔑

AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources for your users. You use IAM to control who can use your AWS resources (authentication) and what resources they can use and in what ways (authorization).

### Terminologies 🙋🏻‍♂️

#### IAM Entities

- Users - End users such as employees of an organization.
- Groups - A collection of users under one set of permissions.
- Roles - You create roles and then assign them to AWS resources.
- Policies - A document that defines one or more permissions.
- Permission - Defines what actions are allowed or denied.

#### IAM Permissions

- Allow - Grants access to a resource.
- Deny - Explicitly denies access to a resource.
- Inherit - Inherits the permissions from the parent resource.

Example of IAM Permissions:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowAll",
            "Effect": "Allow",
            "Action": "*",
            "Resource": "*"
        },
        {
            "Sid": "DenyAll",
            "Effect": "Deny",
            "Action": "*",
            "Resource": "*"
        },
        {
            "Sid": "InheritAll",
            "Effect": "Inherit",
            "Action": "*",
            "Resource": "*"
        }
    ]
}
```

#### IAM Policy Structure

- Version - The policy language version.
- Statement - One or more individual statements.
- Sid - A statement identifier.
- Effect - Whether the statement allows or denies access.
- Principal - The user, account, service, or other entity that is allowed or denied access to a resource.
- Action - The specific action or actions that are allowed or denied.
- Resource - The resource or resources to which the statement applies.
- Condition - Condition keys that define when the statement is in effect.

Example of IAM Policy Structure:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowAll",
            "Effect": "Allow",
            "Action": 
            [
                "s3:ListAllMyBuckets",
                "s3:GetBucketLocation"
            ],
            "Principal": [
                "arn:aws:iam::123456789012:user/Alice",
                "arn:aws:iam::123456789012:user/Bob"
            ],
            "Resource":
            [
                "arn:aws:s3:::*"
            ],
            "Condition": {
                "DateGreaterThan": {
                    "aws:CurrentTime": "2021-01-01T00:00:00Z"
                }
            }
        },

    ]
}
```

#### IAM Roles

AWS Identity and Access Management (IAM) roles are a secure way to grant permissions to entities that you trust. Examples of entities include the following:

- IAM user in another account
- Application code running on an EC2 instance that needs to perform actions on AWS resources
- An AWS service that needs to act on resources in your account to provide its features


### Password Policy 😵

Password policy is a set of rules that define the strong password requirements for IAM users.

### Multi-Factor Authentication (MFA)🔐

Multi-Factor Authentication (MFA) is a security system that requires more than one method of authentication from independent categories of credentials to verify the user's identity for a login or other transaction.

#### How to enable MFA in AWS? 🤔

GO to IAM > Dashboard > Account Settings-> Activate MFA on your root account > Virtual MFA Device > Next Step > Show QR Code > Scan the QR Code using Google Authenticator > Enter the two consecutive codes from Google Authenticator > Assign MFA > Close

### How Can Users Access AWS? 🤔

To Access AWS, users can use:

- AWS Management Console - A web-based interface for accessing and managing AWS services.
- AWS Command Line Interface (CLI) - A command-line tool for accessing and managing AWS services.
- AWS Software Development Kits (SDKs) - A set of software development tools for accessing and managing AWS services.

#### AWS Command Line Interface (CLI) 🖥️

AWS Command Line Interface (CLI) is a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts.

##### How to install AWS CLI? 🤔

- Windows - [Download](https://awscli.amazonaws.com/AWSCLIV2.msi)
- Linux - [Download](https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip)
- macOS - [Download](https://awscli.amazonaws.com/AWSCLIV2.pkg)

##### How to configure AWS CLI? 🤔

- Open Command Prompt or Terminal.
- Type `aws configure`.
- Enter your AWS Access Key ID.
- Enter your AWS Secret Access Key.
- Enter your Default region name.
- Enter your Default output format.

##### How to use multiple AWS accounts in AWS CLI? 🤔

- Open Command Prompt or Terminal.
- Type `aws configure --profile <profile-name>`.
- Enter your AWS Access Key ID.
- Enter your AWS Secret Access Key.
- Enter your Default region name.
- Enter your Default output format.

#### AWS Software Development Kits (SDKs) 🖥️

AWS Software Development Kits (SDKs) are a set of software development tools for accessing and managing AWS services.

##### How to install AWS SDKs? 🤔

- [Download](https://aws.amazon.com/tools/) the AWS SDKs for your preferred programming language.
