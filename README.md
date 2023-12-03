# AWS Cloud Practitioner Notes

  - [Module 1](#module-1)
    - [Cloud Computing](#cloud-computing)
    - [Benefits of cloud computing](#benefits-of-cloud-computing)
  - [Module 2](#module-2)
    - [Amazon EC2](#amazon-ec2)
    - [EC2 Instances Types](#ec2-instances-type)
    - [EC2 Pricing](#ec2-pricing)
  - [General QnA](#general-qna)


# Module 1
### Cloud Computing
[AWS Resource](https://explore.skillbuilder.aws/learn/course/134/play/93606/aws-cloud-practitioner-essentials)

#### Deployment models for cloud computing
When selecting a cloud strategy, a company must consider factors such as required cloud application components, preferred resource management tools, and any legacy IT infrastructure requirements.
- ##### Cloud-based Deployment
  - Run all parts of the application in the cloud
  - Migrate existing applications to the cloud
  - Design and build new applications in the cloud
- ##### On-premises Deployment
  - Deploy resources by using virtualization and resource management tools
  - Increase resource utilization by using application management and virtualization technologies
- ##### Hybrid Deployment
  - Connect cloud-based resources to on-premises infrastructure
  - Integrate cloud-based resources with legacy IT applications

### Benefits of cloud computing
Pay only what you use & No need for infrastructure setup.
- Trade upfront expenses for variable expenses
- Stop spending money to run or maintain data centers
- Stop guessing capacity
  - Don’t have to predict how much infrastructure capacity you will need before deploying an application
- Benefit from massive economic scale
  - Achieve a lower variable cost than you can get on your own
- Increase speed and agility
  - Easier for you to develop and deploy applications
- Go global in minutes
  - Deploy applications to customers around the world quickly, while providing them with low-latency

# Module 2

### Amazon EC2
A Virtual Machine with customizable hardware(Vertical Scaling).
Amazon Elastic Compute Cloud (Amazon EC2) provides secure, resizable compute capacity in the cloud as Amazon EC2 instances.

##### With traditional on-premises resources:
- Spend money upfront to purchase hardware.
- Install the servers in your physical data center.
- Make all the necessary configurations.
##### With an Amazon EC2 instance:
- Provision and launch an Amazon EC2 instance within minutes.
- Stop using it when you have finished running a workload.
- Pay only for the compute time you use when an instance is running, not when it is stopped or terminated.
- Pay only for server capacity that you need or want.

#### How Amazon EC2 works
- ##### Launch
  - Select a template with basic configuration for your EC2 instance.
  - Configuration could include `OS, Application Server, or Application`.
  - Select Instance type, which is the specific hardware configuration.
- ##### Connect
  - There are several ways to connect to the instance.
  - Programs and applications have multiple methods to connect directly to the instance and exchange data.
  - Can also connect to the instance by logging in and accessing the computer desktop.
- #### Use
  - Run commands, install software, add storage, copy and organize files, and more.

### EC2 Instances Type
There are 5 categories of Instance Type.  
When selecting an instance type, consider the specific needs of your workloads and applications. This might include requirements for compute, memory, or storage capabilities.

#### General purpose instances (Basic Computer Package)
Balance of compute, memory, and networking resources. 
- Application servers, gaming servers
- Backend servers for enterprise applications
- Small and medium databases

#### Compute-optimized instances (CPU)
Compute-optimized applications are ideal for
- High-performance web servers, compute-intensive applications servers, and dedicated gaming server
- Batch processing workloads that require processing many transactions in a single group

#### Memory-optimized instances (RAM)
Designed to deliver fast performance for workloads that process large datasets in memory.
-  Workload that requires large amounts of data to be preloaded before running an application
-  High-performance database
-  Performing real-time processing of a large amount of unstructured data

#### Accelerated computing instances (GPU, TPU, DPU)
Hardware accelerators, or coprocessors, perform some functions more efficiently than is possible in software running on CPUs.  
In computing, a hardware accelerator is a component that can expedite data processing.
- Floating-point number calculations, graphics processing, and data pattern matching
- Ideal for workloads such as graphics applications, game streaming, and application streaming

#### Storage-optimized instances (HDD, SSD)
Designed for workloads that require high, sequential read and write access to large datasets on local storage.  
Designed to deliver tens of thousands of low-latency, random IOPS to applications.  
In computing, the term input/output operations per second (IOPS) is a metric that measures the performance of a storage device.
- Application that has a high IOPS requirement
- Distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems

### EC2 Pricing

#### On-Demand

#### Instance Savings Plans

#### Reserved Instances

#### Spot Instances

#### Dedicated Hosts


# General QnA

### Module 1
1. What is cloud computing?
  - On-demand delivery of IT resources and applications through the Internet with pay-as-you-go pricing
2. What is another name for on-premises deployment?
  - Private cloud deployment
3. How does the scale of cloud computing help you to save costs?
  - The aggregated cloud usage from a large number of customers results in lower pay-as-you-go prices

