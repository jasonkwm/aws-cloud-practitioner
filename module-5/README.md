# Table of Content
- [Instance Stores and Amazon Elastic Block Store (Amazon EBS)](#instance-stores-and-amazon-elastic-block-store-amazon-ebs)
  - [Instance Stores](#instance-stores)
  - [Amazon Elastic Block Store (Amazon EBS)](#amazon-elastic-block-store-amazon-ebs)
    - [Amazon EBS snapshots](#amazon-ebs-snapshots)


# Instance Stores and Amazon Elastic Block Store (Amazon EBS)

## Instance Stores
Block-level storage volumes behave like `physical hard drives`.
- Instance store provides `temporary` block-level storage for an Amazon EC2 instance
- `Physically attached` to the host computer for an EC2 instance, and therefore has the same `lifespan` as the instance

## Amazon Elastic Block Store (Amazon EBS)
- Provides block-level storage volumes that you can use with Amazon EC2 instances
- Data on the attached EBS volume `remains available` after Amazon EC2 instance termination
- You define the `configuration` (such as volume size and type) and provision it
- It can `attach` to an Amazon EC2 instance
- EBS volumes are for data that needs to persist, it’s important to `back up` the data
- Take incremental backups of EBS volumes by creating Amazon EBS `snapshots`

### Amazon EBS snapshots
1. An EBS snapshot is an incremental backup.
2. This means that the `first backup` taken of a volume copies all the data
3. For `subsequent backups`, only the blocks of data that have changed since the most recent snapshot are saved  
<img width="600"  src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/bd9b5562-70da-43e9-b820-8875e08f2c1e"/>

Incremental backups are different from full backups, in which all the data in a storage volume copies each time a backup occurs. The full backup includes data that has not changed since the most recent backup.
