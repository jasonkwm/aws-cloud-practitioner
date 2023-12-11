# Table of Content
- [AWS Cloud Adoption Framework (AWS CAF)](#aws-cloud-adoption-framework-aws-caf)
  - [Business Capabilities](#business-capabilities)
    - [Business Perspective](#business-perspective)
    - [People Perspective](#people-perspective)
    - [Governance Perspective](#governance-perspective)
  - [Technical Capabilities](#technical-capabilities)
    - [Platform Perspective](#platform-perspective)
    - [Security Perspective](#security-perspective)
    - [Operations Perspective](#operations-perspective)
- [Migration Strategies](#migration-strategies)
  - [6 strategies for migration](#6-strategies-for-migration)
    - [Rehosting](#rehosting)
    - [Replatforming](#replatforming)
    - [Refactoring/re-architecting](#refactoring/re-architecting)
    - [Repurchasing](#repurchasing)
    - [Retaining](#retaining)
    - [Retiring](#retiring)
- [AWS Snow Family](#aws-snow-family)
  - [AWS Snowcone](#aws-snowcone)
  - [AWS Snowball](#aws-snowball)
    - [Snowball Edge Storage Optimized](#snowball-edge-storage-optimized)
    - [Snowball Edge Compute Optimized](#snowball-edge-compute-optimized)
  - [AWS Snowmobile](#aws-snowmobile)
- [Innovation with AWS](#innovation-with-aws)
  - [Serverless Applications](#serverless-applications)
  - [Artificial Intelligence](#artificial-intelligence)
  - [Machine Learning](#machine-learning)

# AWS Cloud Adoption Framework (AWS CAF)
 **AWS Cloud Adoption Framework (AWS CAF)** organizes guidance into `six areas` of focus, called `Perspectives`. Each **Perspective** addresses `distinct responsibilities`.   
 **In general**, the `Business`, `People`, and `Governance Perspectives` focus on `business capabilities`.  
 Whereas the `Platform`, `Security`, and `Operations` **Perspectives** focus on `technical capabilities`.

 ## Business Capabilities
 
### Business Perspective
- Ensures that IT `aligns` with business needs and that `IT investments link` to `key business results`.  
- Create a `strong business case` for cloud adoption and `prioritize cloud adoption initiatives`.   
- `Common roles` in the **Business Perspective** include: 
  - `Business managers`, `Finance managers`, `Budget owners`, `Strategy stakeholders`

### People Perspective
- `Supports development` of an organization-wide change `management strategy` for `successful cloud adoption`
- `Evaluate organizational structures` and roles, new skill and process requirements, and identify gaps
- `Helps prioritize` training, staffing, and organizational changes
- `Common roles` in the **People Perspective** include:
  - `Human resources`, `Staffing`, `People managers`
### Governance Perspective
- Focuses on the skills and processes to `align IT strategy` with `business strategy`
- `Maximize` the `business value` and `minimize risks`
- `Understand how` to update the `staff skills` and processes necessary to ensure `business governance in the cloud`
- `Common roles` in the **Governance Perspective** include:
  - `Chief Information Officer (CIO)`, `Program managers`, `Enterprise architects`, `Business analysts`, `Portfolio managers`


 ## Technical Capabilities

### Platform Perspective
- Principles and patterns for `implementing new solutions` on the cloud, and `migrating on-premises workloads` to the cloud
- Use a variety of `architectural models` to `understand and communicate` the structure of `IT systems and their relationships`
- `Common roles` in the **Platform Perspective** include: 
  - `Chief Technology Officer (CTO)`, `IT managers`, `Solutions architects`
### Security Perspective
- Ensures that the organization meets `security objectives` for `visibility`, `auditability`, `control`, and `agility`
- `Structure` the `selection and implementation` of `security controls` that meet the organization’s needs
- `Common roles` in the **Security Perspective** include:
  - `Chief Information Security Officer (CISO)`, `IT security managers`, `IT security analysts`
### Operations Perspective
- `Enable`, `run`, `use`, `operate`, and `recover IT workloads` to the level agreed upon with your `business stakeholders`
- Define how `day-to-day`, `quarter-to-quarter`, and `year-to-year` business is conducted
- `Helps stakeholders` define current `operating procedures` and identify the `process changes` and `training needed` to implement `successful cloud adoption`
- `Common roles` in the **Operations Perspective** include:
- `IT operations managers`, `IT support managers`

# Migration Strategies
## 6 strategies for migration
`Six` of the most common `migration strategies` that you can implement are:
- `Rehosting`, `Replatforming`, `Refactoring/re-architecting`, `Repurchasing`, `Retaining`, `Retiring`

### Rehosting
- Also known as `lift-and-shift` involves `moving applications without changes`

### Replatforming
- Also known as `lift, tinker, and shift,` involves making a `few cloud optimizations` to realize a `tangible benefit`
- Optimization` is achieved `without changing` the `core architecture` of the application

### Refactoring/re-architecting
- Involves `reimagining how` an application is `architected and developed` by using `cloud-native features`
- Driven by a **strong business need** to `add features`, `scale`, or `performance` that would otherwise be difficult to achieve in the `application’s existing environment`

### Repurchasing
- `Moving` from a `traditional license` to a `software-as-a-service` model
### Retaining
- Keeping applications that are `critical` for the business in the `source environment`
- Include applications that `require major refactoring` before they can be `migrated`, or, work that can be postponed until a later time

### Retiring
- Process of `removing applications` that are `no longer needed`

# AWS Snow Family
- A `collection of physical devices` that help to `physically transport` up to exabytes of `data into and out of AWS`
- Composed of `AWS Snowcone`, `AWS Snowball`, and `AWS Snowmobile`
- These devices `offer different capacity` points, and most include built-in computing capabilities
- **AWS** `owns and manages` the **Snow Family** devices and integrates with **AWS** `security`, `monitoring`, `storage management`, and `computing capabilities`

### AWS Snowcone
- A small, rugged, and secure `edge computing` and `data transfer device`
- Features `2 CPUs`, `4 GB of memory`, and `up to 14 TB` of `usable storage` 
### AWS Snowball
Offers `two types of devices`:
#### Snowball Edge Storage Optimized: 
- `Well suited` for `large-scale data migrations` and `recurring transfer workflows`, in addition to `local computing with higher capacity needs`
- **Storage**:
  - `80 TB of hard disk drive (HDD)` capacity for `block volumes` and **Amazon S3** compatible `object storage`
  - `1 TB of SATA solid state drive (SSD)` for `block volumes`
- **Compute**:
- `40 vCPUs`
- `80 GiB of memory` to support **Amazon EC2** `sbe1` instances (equivalent to `C5`)
#### Snowball Edge Compute Optimized
- `Powerful computing resources` for use cases such as `machine learning`, `full motion video analysis`, `analytics`, and `local computing stacks`
- **Storage**:
  - `80-TB usable HDD` capacity for **Amazon S3** compatible `object storage` or **Amazon EBS** compatible `block volumes`
  - `28 TB of usable NVMe SSD` capacity for **Amazon EBS** compatible `block volumes`
- **Compute**:
  - `104 vCPUs`
  - `416 GiB of memory`
  - `optional NVIDIA Tesla V100 GPU`
  - Devices run **Amazon EC2** `sbe-c` and `sbe-g` instances, which are equivalent to `C5`, `M5a`, `G3`, and `P3` instances

### AWS Snowmobile
- An `exabyte-scale data transfer service` used to move large amounts of data to **AWS**
- Transfer up to `100 petabytes` of data per Snowmobile
- `45-foot long` ruggedized `shipping container`, pulled by a `semi trailer truck`

# Innovation with AWS
Consider some of the `paths you might explore` in the future as you continue on your `cloud journey`. 

## Serverless Applications
- Serverless refers to applications that `don’t require` you to `provision`, `maintain`, or `administer servers`
- Don’t need to worry about `fault tolerance` or `availability`
- **AWS Lambda** is an example of a service that you can use to `run serverless applications`
- Bypass the need to manage a fleet of servers
- Enables your developers to `focus` on their `core product` instead of managing and operating servers

## Artificial Intelligence
**AWS** offers a   variety of services   powered by   artificial intelligence (AI)`.
For example, you can perform the following tasks:
- `Convert speech to text` with **Amazon Transcribe**
- `Discover patterns in text` with **Amazon Comprehend**
- `Identify potentially fraudulent online activities` with **Amazon Fraud Detector**
- `Build voice and text chatbots` with **Amazon Lex**

## Machine Learning
**AWS** offers **Amazon SageMaker** to remove the difficult work from the process and `empower you to build`, `train`, and `deploy ML models quickly`.
