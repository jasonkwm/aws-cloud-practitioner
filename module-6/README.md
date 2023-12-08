# Table of Content

- [AWS Shared Responsibility Model](#)
- [AWS Identity and Access Management (IAM)](#)
  - [AWS account root user](#)
  - [IAM users](#)
  - [IAM policies](#)
  - [IAM groups](#)
  - [Multi-factor authentication](#)
    - [Available MFA methods for IAM](#)
- [AWS Organizations](#)
  - [Organizational units (OU)](#)
- [Compliance](#)
  - [AWS Artifact](#)
    - [AWS Artifact Agreements](#)
    - [AWS Artifact Reports](#)
  - [Customer Compliance Center](#)
- [Denial-of-Service Attacks](#)
  - [AWS Shield](#)
  - [AWS Shield Standard](#)
  - [AWS Shield Advanced](#)
- [Additional Security Services](#)
  - [AWS Key Management Service (AWS KMS)](#)
  - [AWS Web Application Firewall (WAF)](#)
- [](#)
- [](#)



# AWS Shared Responsibility Model
The shared responsibility model divides into `customer responsibilities` (commonly referred to as **“security in the cloud”**) and `AWS responsibilities` (commonly referred to as **“security of the cloud”**).

### Customers: Security in the cloud
- Customers are `responsible` for the `security of everything` that they `create and put` in the **AWS Cloud**
- You, the customer, `maintain complete control` over your content
- You are `responsible` for `managing security requirements` for your content and `who has access` to that content
- You also `control` how `access rights` are `granted`, `managed`, and `revoked`

### AWS: Security of the cloud
- AWS is `responsible` for security of the cloud
- AWS `operates, manages, and controls` the components at `all layers` of infrastructure
- AWS is `responsible` for protecting the `global infrastructure` that runs all of the `services offered` in the AWS Cloud
- AWS `manages` the security of the cloud, specifically the `physical infrastructure` that hosts your resources
- 
<img width="600" alt="who is responsible for which part" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/6a385922-8054-4816-ae51-d7bc3c3fdfdf" />

# AWS Identity and Access Management (IAM)
Enables you to manage access to AWS services and resources securely.  
IAM gives you the flexibility to configure access based on your company’s specific operational and security needs.  
IAM features includes: 
- IAM users, groups, and roles
- IAM policies
- Multi-factor authentication

## AWS account root user
When you first create an `AWS account`, you begin with an identity known as the `root user`.  
The root user is accessed by signing in with the email address and password that you used to create your AWS account.  
### Best practice:
- `Do not` use the `root user` for everyday tasks.
- Create your `first IAM` user and `assign it permissions` to create other users
- Continue to create `other IAM users`, and access those identities for `performing regular` tasks throughout AWS
<img width="600" alt="iam diagram" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/aef2ca56-a42a-4600-913c-042e3797edca">

## IAM users
An IAM user is an `identity` that you create in AWS.  
By default, when you create a `new IAM user` in AWS, it has `no permissions` associated with it.  
You must `grant` the `IAM user` the necessary `permissions` such as launching an **Amazon EC2 instance** or creating an **Amazon S3 bucket**.  
### Best practice:
- Create `individual IAM users` for `each person` who needs to access AWS
- If you have `multiple employees` who require the `same level of access`, you should create `individual IAM users` for each of them

## IAM policies
An IAM policy is a `document` that `allows or denies permissions` to AWS services and resources.  
Enable you to `customize users’ levels` of access to resources.  
### Best practice:
- Follow the security principle of `least privilege` when `granting permissions`
- `Prevent` users or roles from having `more permissions` than needed to `perform their tasks`.

<img width="300" alt="iam policy example" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/8b10766c-f8b1-419a-97cc-b3929192a217">  

*This example IAM policy allows permission to access the objects in the Amazon S3 bucket with ID: AWSDOC-EXAMPLE-BUCKET*

## IAM groups
An IAM group is a `collection of IAM users`. When you assign an `IAM policy` to a group, `all users` in the group are `granted permissions` specified by the policy.
<img width="300" alt="iam group" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/0e31d3dc-6be0-4ab9-894b-90a42e877224">

## IAM roles
An IAM role is an `identity` that you can assume to `gain temporary access` to permissions.  
`Before` an IAM user, application, or service can `assume an IAM role`, they must be `granted permissions` to switch to the role.  
When someone assumes an `IAM role`, they `abandon all previous permissions` that they had under a previous role and assume the permissions of the new role.  
### Best practice:
- IAM roles are `ideal for situations` in which access to services or resources needs to be `granted temporarily`, `instead of long-term`

## Multi-factor authentication
In IAM, multi-factor authentication (MFA) provides an extra layer of security for your AWS account.  
### Available MFA methods for IAM:
- FIDO security keys
- Virtual authenticator apps
- Hardware TOTP tokens
- Hardware TOTP tokens for the AWS GovCloud (US) Regions

# AWS Organizations
- You can use **AWS Organizations** to `consolidate and manage` multiple AWS accounts within a `central location`
- When you `create an organization`, **AWS Organizations** `automatically creates a root`, which is the `parent container` for `all the accounts` in your organization
- You can `centrally control permissions` for the accounts in your organization by using `service control policies (SCPs)`  
- `SCPs` enable you to `place restrictions` on the **AWS services, resources, and individual API** actions that users and roles in each account can access
- `Consolidated billing` is another feature of **AWS Organizations**

## Organizational units (OU)
- You can `group accounts` into `organizational units (OUs)` to make it easier to manage accounts with similar `business or security requirements`  
- When you apply a `policy to an OU`, all the accounts in the OU `automatically inherit` the `permissions` specified in the policy
- You can more `easily isolate workloads` or applications that have specific `security requirements`
- You can `attach a policy` to the OU that `blocks access` to all other AWS services that do not meet the `regulatory requirements`

# Compliance

## AWS Artifact
AWS Artifact is a service that `provides on-demand access` to `AWS security and compliance` reports and select online agreements
AWS Artifact consists of two main sections: *AWS Artifact Agreements* and *AWS Artifact Reports*

### AWS Artifact Agreements
In **AWS Artifact Agreements**, you can `review`, `accept`, and `manage agreements` for an individual account and for all your accounts in **AWS Organizations**  
`Different types` of agreements are offered to address the needs of customers who are subject to `specific regulations`, such as the *Health Insurance Portability and Accountability Act (HIPAA)*.  

### AWS Artifact Reports
- **AWS Artifact Reports** provide `compliance reports` from `third-party auditors`
- AWS is compliant with a variety of *global, regional, and industry-specific security standards and regulations*
- Provide **AWS audit artifacts** to your `auditors or regulators` as `evidence` of **AWS security controls**
- Remains `up to date` with the latest reports released

## Customer Compliance Center
The **Customer Compliance Center** contains resources to help you `learn more` about **AWS compliance**. 
- You can read `customer compliance stories` to discover how companies in regulated industries have `solved various compliance`, `governance`, and `audit challenges`
- You can also `access compliance whitepapers` and `documentation` on topics such as:
  - AWS answers to key compliance questions
  - An overview of AWS risk and compliance
  - An auditing security checklist
- Customer Compliance Center includes an `auditor learning path` designed for `individuals` in `auditing`, `compliance`, and `legal roles` who want to `learn more`

# Denial-of-Service Attacks
A `denial-of-service (DoS)` attack is a `deliberate attempt` to make a website or application `unavailable to users`.

### Distributed denial-of-service attacks
In a `distributed denial-of-service (DDoS)` attack, multiple sources are used to start an attack that aims to make a `website or application unavailable`

## AWS Shield
AWS Shield is a service that `protects applications against DDoS attacks`.  
AWS Shield provides `two levels` of protection: *Standard* and *Advanced*

### AWS Shield Standard
- `automatically` protects all AWS customers at `no cost`
- It `protects` your AWS resources from the `most common`, `frequently occurring` types of **DDoS** attacks
- **AWS Shield Standard** uses a variety of `analysis techniques` to `detect malicious traffic` in real time and `automatically mitigates` it.

### AWS Shield Advanced
- A `paid service` that provides detailed `attack diagnostics` and the ability to `detect and mitigate sophisticated` **DDoS** attacks.
- `Integrates` with other services such as **Amazon CloudFront**, **Amazon Route 53**, and **Elastic Load Balancing**
- You can integrate **AWS Shield** with **AWS Web Application Firewall (WAF)** by writing `custom rules` to mitigate complex **DDoS** attacks.

# Additional Security Services
## AWS Key Management Service (AWS KMS)
- Enables you to perform `encryption operations` through the use of `cryptographic keys`
- You can use **AWS KMS** to `create`, `manage`, and use `cryptographic keys`
- `Control` the `use of keys` across a wide range of services and in your applications
- `Choose` the `specific levels` of `access control` that you need for your keys
- Specify which IAM users and roles are able to `manage keys`
- Temporarily `disable keys` so that they are no longer in use by anyone
- Your keys `never leave` **AWS KMS**, and you are `always in control` of them

## AWS Web Application Firewall (WAF)
- `Web application firewall` that lets you `monitor network requests` that come into your web applications
- **AWS WAF** works together with **Amazon CloudFront** and an **Application Load Balancer**
- **AWS WAF** uses a `web access control list (ACL)` to protect your AWS resources
- Configure the `web ACL` to allow all requests except those from the IP addresses that you have specified
- Requests are checked against the list of rules that you have configured in the web ACL

## Amazon Inspector
- Amazon Inspector helps to `improve` the `security and compliance` of applications by running `automated security assessments`
- `Checks applications` for `security vulnerabilities` and deviations from `security best practices`, such as open access to Amazon EC2 instances and installations of vulnerable software versions
- It `provides` you with a `list of security findings`
- List prioritizes by `severity level`, including a `detailed description` of each security issue and a `recommendation` for how to fix it
- **AWS** `does not guarantee` that following the provided recommendations `resolves every potential security issue`

## Amazon GuardDuty
- Provides `intelligent threat detection` for your **AWS infrastructure** and resources
- Identifies threats by `continuously monitoring` the `network activity` and `account behavior` within your **AWS environment**
- You `do not` have to `deploy or manage` any additional security software
- **GuardDuty** `continuously analyzes` data from multiple **AWS sources**, including **VPC Flow Logs** and **DNS logs**
- You can `review` detailed findings about them from the **AWS Management Console**
- You can also `configure AWS Lambda` functions to `take remediation steps automatically` in response to GuardDuty’s security findings
