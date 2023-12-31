# AWS Cloud Practitioner Notes

-   [Module 1 (Introduction to Amazon web services)](#module-1)
    -   [Cloud Computing](#cloud-computing)
    -   [Benefits of cloud computing](#benefits-of-cloud-computing)
-   [Module 2 (Compute in the cloud)](./module-2)
    -   [Amazon EC2](./module-2#amazon-ec2)
    -   [EC2 Instance Type](./module-2#ec2-instances-type)
    -   [EC2 Pricing](./module-2#ec2-pricing)
    -   [Scaling Amazon EC2](./module-2#scaling-amazon-ec2)
    -   [Elastic Load Balancing](./module-2#elastic-load-balancing)
    -   [Message and Queuing](./module-2#message-and-queuing)
    -   [Additional Compute Services](./module-2#additional-compute-services)
-   [Module 3 (Global Infrastructure and Reliability)](./module-3)
    -   [AWS Global Infrastructure](./module-3#aws-global-infrastructure)
    -   [Edge Location CDN](./module-3#edge-location-cdn)
    -   [How to Provision AWS Resources](./module-3#how-to-provision-aws-resources)
-   [Module 4 (Networking)](./module-4)
    -   [Connectivity to AWS](./module-4#connectivity-to-aws)
    -   [Subnets and Network Access Control Lists](./module-4#subnets-and-network-access-control-lists)
    -   [Global Networking](./module-4#global-networking)
-   [Module 5 (Storage and Databases)](./module-5)
    - [Instance Stores and Amazon Elastic Block Store (Amazon EBS)](./module-5#instance-stores-and-amazon-elastic-block-store-amazon-ebs)
    - [Amazon Simple Storage Service (Amazon S3)](./module-5#amazon-simple-storage-service-amazon-s3)
    - [Amazon Elastic File System (Amazon EFS)](amazon-elastic-file-system-amazon-efs)
    - [Amazon Relational Database Service (Amazon RDS)](./module-5#amazon-relational-database-service-amazon-rds)
    - [Amazon DynamoDB](./module-5#amazon-dynamodb)
    - [Amazon Redshift](./module-5#amazon-redshift)
    - [AWS Database Migration Service (AWS DMS)](./module-5#aws-database-migration-service-aws-dms)
    - [Additional database services](./module-5#additional-database-services)
- [Module 6 (Security)](./module-6)
    - [AWS Shared Responsibility Model](./module-6#aws-shared-responsibility-model)
    - [AWS Identity and Access Management (IAM)](./module-6#aws-identity-and-access-management-iam)
    - [AWS Organizations](./module-6#aws-organizations)
    - [Compliance](./module-6#compliance)
    - [Denial-of-Service Attacks](./module-6#denial-of-service-attacks)
    - [Additional Security Services](./module-6#additional-security-services)
- [Module 7 (Monitoring and Analytics)](./module-7)
    - [Amazon CloudWatch](./module-7#amazon-cloudwatch)
    - [AWS CloudTrail](./module-7#aws-cloudtrail)
    - [AWS Trusted Advisor](./module-7#aws-trusted-advisor)
- [Module 8 (Pricing and Support)](./module-8)
    - [AWS Free Tier](./module-8#aws-free-tier)
    - [AWS Pricing Concepts](./module-8#aws-pricing-concepts)
    - [Billing Dashboard](./module-8#billing-dashboard)
    - [Consolidated Billing](./module-8#consolidated-billing)
    - [AWS Budgets](./module-8#aws-budgets)
    - [AWS Cost Explorer](./module-8#aws-cost-explorer)
    - [AWS Support Plans](./module-8#aws-support-plans)
    - [AWS Marketplace](./module-8#aws-marketplace)
- [Module 9 (Migration and Innovation)](./module-9)
    - [Migration Strategies](./module-9#migration-strategies)
    - [AWS Snow Family](./module-9#aws-snow-family)
    - [Innovation with AWS](./module-9#innovation-with-aws)
- [Module 10 (The Cloud Journey)](./module-10)
    - [The AWS Well-Architected Framework](./module-10#the-aws-well-architected-framework)
    - [Benefits of the AWS Cloud](./module-10#benefits-of-the-aws-cloud)
-   [General QnA](./QnA)

# Module 1

## Cloud Computing

[AWS Resource](https://explore.skillbuilder.aws/learn/course/134/play/93606/aws-cloud-practitioner-essentials)

### Deployment models for cloud computing

When selecting a cloud strategy, a company must consider factors such as required cloud application components, preferred resource management tools, and any legacy IT infrastructure requirements.

-   ##### Cloud-based Deployment
    -   Run all parts of the application in the cloud
    -   Migrate existing applications to the cloud
    -   Design and build new applications in the cloud
-   ##### On-premises Deployment
    -   Deploy resources by using virtualization and resource management tools
    -   Increase resource utilization by using application management and virtualization technologies
-   ##### Hybrid Deployment
    -   Connect cloud-based resources to on-premises infrastructure
    -   Integrate cloud-based resources with legacy IT applications

### Benefits of cloud computing

Pay only what you use & No need for infrastructure setup.

-   Trade upfront expenses for variable expenses
-   Stop spending money to run or maintain data centers
-   Stop guessing capacity
    -   Don’t have to predict how much infrastructure capacity you will need before deploying an application
-   Benefit from massive economic scale
    -   Achieve a lower variable cost than you can get on your own
-   Increase speed and agility
    -   Easier for you to develop and deploy applications
-   Go global in minutes
    -   Deploy applications to customers around the world quickly, while providing them with low-latency
