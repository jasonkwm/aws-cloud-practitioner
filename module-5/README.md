# Table of Content
- [Instance Stores and Amazon Elastic Block Store (Amazon EBS)](#instance-stores-and-amazon-elastic-block-store-amazon-ebs)
  - [Instance Stores (Block Storage)](#instance-stores)
  - [Amazon Elastic Block Store (Amazon EBS)](#amazon-elastic-block-store-amazon-ebs)
    - [Amazon EBS snapshots](#amazon-ebs-snapshots)
- [Amazon Simple Storage Service (Amazon S3)](#amazon-simple-storage-service-amazon-s3)
  - [Object Storage](#object-storage)
  - [Amazon S3 storage classes](#amazon-s3-storage-classes)
    - [S3 Standard](#s3-standard)
    - [S3 Standard-Infrequent Access (S3 Standard-IA)](#s3-standard-infrequent-access-s3-standard-ia)
    - [S3 One Zone-Infrequent Access (S3 One Zone-IA)](#s3-one-zone-infrequent-access-s3-one-zone-ia)
    - [S3 Intelligent-Tiering](#s3-intelligent-tiering)
    - [S3 Glacier Instant Retrieval](#s3-glacier-instant-retrieval)
    - [S3 Glacier Flexible Retrieval](#s3-glacier-flexible-retrieval)
    - [S3 Glacier Deep Archive](#s3-glacier-deep-archive)
    - [S3 Outposts](#s3-outposts)
- [Amazon Elastic File System (Amazon EFS)](amazon-elastic-file-system-amazon-efs)
  - [File Storage](#file-storage)
  - [Comparing Amazon EBS and Amazon EFS](#comparing-amazon-ebs-and-amazon-efs)
- [Amazon Relational Database Service (Amazon RDS)](#amazon-relational-database-service-amazon-rds)
  - [Relational databases](#relational-databases)
  - [Amazon RDS database engines](#amazon-rds-database-engines)
  - [Amazon Aurora](#amazon-aurora)
- [Amazon DynamoDB](#amazon-dynamodb)
  - [Non-relational Databases](#non-relational-databases)
- [Amazon Redshift](#amazon-redshift)
- [AWS Database Migration Service (AWS DMS)](#aws-database-migration-service-aws-dms)
- [Additional database services](#additional-database-services)

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
1. An EBS snapshot is an `incremental backup`.
2. This means that the `first backup` taken of a volume copies all the data
3. For `subsequent backups`, only the blocks of data that have changed since the most recent snapshot are saved  
<img width="600"  src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/bd9b5562-70da-43e9-b820-8875e08f2c1e"/>

Incremental backups are different from full backups, in which all the data in a storage volume copies each time a backup occurs. The full backup includes data that has not changed since the most recent backup.

# Amazon Simple Storage Service (Amazon S3)
Amazon S3 provides `Object-level storage`. Amazon S3 stores data as objects in buckets.  
- You might use Amazon S3 to store `backup files`, `media files` for a website, or `archived documents`
- The `maximum file size` for an object in Amazon S3 is 5 TB
- You can set `permissions` to control visibility and access to it
- You can also use the Amazon S3 `versioning` feature to track changes to your objects over time
- You can `upload any type` of file to Amazon S3, such as images, videos, text files, and so on

## Object Storage
In object storage, each object consists of `data`, `metadata`, and a `key`.  
- The `data` might be an `image, video, text document, or any other type of file`
- `Metadata` contains information about what the data is, how it is used, the object size, and so on
- An object’s `key` is its `unique identifier`

## Amazon S3 storage classes
Choose from a range of [storage classes](https://aws.amazon.com/s3/storage-classes/) to select a fit for your business and cost needs.  
When selecting an Amazon S3 storage class, consider these two factors:
- `How often` you plan to `retrieve` your data
- `How available` you need your data to be

### S3 Standard
- Designed for `frequently accessed data`
- Stores data in a `minimum` of `three Availability Zones`
- Good choice for a wide range of use cases, such as `websites, content distribution, and data analytics`
- Has a `higher cost`

### S3 Standard-Infrequent Access (S3 Standard-IA)
- Ideal for `infrequently accessed data`
- Similar to *Amazon S3 Standard* but has a `lower storage price` and `higher retrieval price`
- Ideal for data `infrequently accessed` but `requires high availability` when needed
- Stores data in a `minimum` of `three Availability Zones`

### S3 One Zone-Infrequent Access (S3 One Zone-IA)
- Stores data in a `single Availability Zone`
- Has a `lower storage price` than *Amazon S3 Standard-IA*
- Good storage class to consider if the following conditions apply:
  - You want to `save costs on storage`
  - You can `easily reproduce` your data in the event of an `Availability Zone failure`\

### S3 Intelligent-Tiering
- Ideal for data with `unknown or changing access patterns`
- `Requires` a small `monthly monitoring` and `automation fee` per object
- If you `haven’t accessed` an object for `30 consecutive days`, Amazon S3 `automatically moves` it to the `infrequent access tier`, *S3 Standard-IA*
- If you `access` an object in the `infrequent access tier`, Amazon S3 `automatically moves` it to the `frequent access tier`, *S3 Standard*

### S3 Glacier Instant Retrieval
- Works well for `archived data` that `requires immediate access`
- Can `retrieve objects` within a `few milliseconds`
- You can `retrieve objects` stored in the *S3 Glacier Instant Retrieval* storage class `within milliseconds`, with the `same performance` as *S3 Standard*.

### S3 Glacier Flexible Retrieval
- *Low-cost* storage designed for `data archiving`
- Able to `retrieve objects` within a `few minutes to hours`
- You might use this storage class to store archived customer records or older photos and video files

### S3 Glacier Deep Archive
- `Lowest-cost` object storage class ideal for archiving
- Able to `retrieve objects` within `12 hours`
- Supports `long-term retention` and `digital preservation` for data that might be `accessed once or twice in a year`
- Lowest-cost storage in the *AWS Cloud*, with `data retrieval` from `12 to 48 hours`

### S3 Outposts
- Creates *S3 buckets* on *Amazon S3 Outposts*
- Makes it easier to retrieve, store, and access data on *AWS Outposts*
- Delivers `object storage` to your `on-premises` *AWS Outposts* environment
- Store data `durably and redundantly` across `multiple devices and servers` on your *Outposts*
- Works well for workloads with `local data residency requirements` that must satisfy demanding performance needs by keeping data close to on-premises applications

# Amazon Elastic File System (Amazon EFS)
`Scalable file system` used with *AWS Cloud* services and *on-premises* resources.  
*Amazon EFS* `grows and shrinks automatically`. It can `scale on demand` to `petabytes` without disrupting applications. 


## File Storage
In file storage, `multiple clients` (such as users, applications, servers, and so on) can `access data` that is stored in `shared file folders`.  
`Storage server` uses **block storage** with a `local file system` to organize files. Clients `access data` through `file paths`.
Compared to **block storage** and **object storage**, `file storage` is ideal for use cases in which a large number of `services and resources` need to `access` the `same data at the same time`.

### Comparing Amazon EBS and Amazon EFS

|Amazon EBS|Amazon EFS|
|:---|:---|
|Stores data in a `single Availability Zone`|Stores data in and across `multiple Availability Zones`|
|`Amazon EC2`` instance and the `EBS volume`` must reside within the `same Availability Zone`|`Access data concurrently` from `all Availability Zones` in the Region where a file system is located|
||*on-premises* servers can access `Amazon EFS` using `AWS Direct Connect`|


# Amazon Relational Database Service (Amazon RDS)
**Amazon RDS** is a managed service that `automates tasks` such as `hardware provisioning, database setup, patching, and backups`
- You can spend less time completing administrative tasks
- Many Amazon RDS database engines offer:
  -  Encryption at `rest` (protecting data while it is stored)
  -  Encryption in `transit` (protecting data while it is being sent and received)

## Relational databases
A `relational database` stores information in `tabular form`.  
Relational databases use `structured query language (SQL)` to store and query data.

## Amazon RDS database engines
**Amazon RDS** is available on `six database engines`, which `optimize` for `memory`, `performance`, or `input/output (I/O)`  
Supported database engines include:
- `Amazon Aurora`, `PostgreSQL`, `MySQL`, `MariaDB`, `Oracle Database`, `Microsoft SQL Server`

## Amazon Aurora
- Enterprise-class relational database
- Compatible with `MySQL` and `PostgreSQL` relational databases
- Up to `five times faster` than standard `MySQL` databases
- Up to `three times faster` than standard `PostgreSQL` databases
- Helps to `reduce your database costs` by reducing unnecessary input/output (I/O) operations, while ensuring that your database resources `remain reliable and available`
- Consider Amazon Aurora if your `workloads` require `high availability`
- It replicates `six copies` of your data across `three Availability Zones` and `continuously backs up` your data to **Amazon S3**


# Amazon DynamoDB
- **Amazon DynamoDB** is a `key-value database service`. It delivers `single-digit millisecond` performance at any scale
- *DynamoDB* is `serverless`, which means that you `do not` have to `provision, patch, or manage servers`
- *DynamoDB* `automatically scales` to adjust for `changes in capacity` while `maintaining consistent performance`
- Suitable choice for use cases that `require high performance while scaling`

## Non-relational Databases
One type of structural approach for **nonrelational databases** is `key-value pairs`. With key-value pairs, data is organized into items (keys), and items have attributes (values).  
You can `add or remove attributes` from items in the table at any time and `not every item` in the table has to have the `same attributes`

# Amazon Redshift
**Amazon Redshift** is a `data warehousing service` that you can use for `big data analytics`. It offers the ability to `collect data from many sources` and helps you to understand relationships and trends across your data.

# AWS Database Migration Service (AWS DMS)
Enables you to migrate relational databases, nonrelational databases, and other types of data stores.  
With AWS DMS, you move data between a source database and a target database.  

# Additional Database Services

**Amazon DocumentDB** is a document database service that supports MongoDB workloads. (MongoDB is a document database program.)  

**Amazon Neptune** is a graph database service.  
You can use Amazon Neptune to build and run applications that work with highly connected datasets, such as recommendation engines, fraud detection, and knowledge graphs.  

**Amazon Quantum Ledger Database (Amazon QLDB)** is a ledger database service.  
You can use Amazon QLDB to review a complete history of all the changes that have been made to your application data.  

**Amazon Managed Blockchain** is a service that you can use to create and manage blockchain networks with open-source frameworks.  
Blockchain is a distributed ledger system that lets multiple parties run transactions and share data without a central authority.  

**Amazon ElastiCache** is a service that adds caching layers on top of your databases to help improve the read times of common requests.  
It supports two types of data stores: Redis and Memcached.  

**Amazon DynamoDB Accelerator (DAX)** is an in-memory cache for DynamoDB.  
It helps improve response times from single-digit milliseconds to microseconds.  
