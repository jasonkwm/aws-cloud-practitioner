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
- [](#)
- [](#)
- [](#)
- [](#)
- [](#)
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
