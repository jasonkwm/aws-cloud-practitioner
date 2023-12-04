# Table of Content

-   [Amazon EC2](#amazon-ec2)
    -   [How Amazon EC2 works](#how-amazon-ec2-works)
-   [EC2 Instances Types](#ec2-instances-type)
    -   [General purpose instances](#general-purpose-instances)
    -   [Compute-optimized instances](#compute-optimized-instances)
    -   [Memory-optimized instances](#memory-optimized-instances)
    -   [Accelerated computing instances](#accelerated-computing-instances)
    -   [Storage-optimized instances](#storage-optimized-instances)
-   [EC2 Pricing](#ec2-pricing)
    -   [On-Demand](#on-demand)
    -   [Reserved Instances](#reserved-instances)
    -   [Instance Savings Plans](#instance-savings-plans)
    -   [Spot Instances](#spot-instances)
    -   [Dedicated Hosts](#dedicated-hosts)
-   [Scaling Amazon EC2](#scaling-amazon-ec2)
    -   [Amazon EC2 Auto Scaling](#amazon-ec2-auto-scaling)

## Amazon EC2

A Virtual Machine with customizable hardware (Vertical Scaling).
Amazon Elastic Compute Cloud (Amazon EC2) provides secure, resizable compute capacity in the cloud as Amazon EC2 instances.

##### With traditional on-premises resources:

-   Spend money upfront to purchase hardware.
-   Install the servers in your physical data center.
-   Make all the necessary configurations.

##### With an Amazon EC2 instance:

-   Provision and launch an Amazon EC2 instance within minutes.
-   Stop using it when you have finished running a workload.
-   Pay only for the compute time you use when an instance is running, not when it is stopped or terminated.
-   Pay only for the server capacity that you need or want.

### How Amazon EC2 works

-   ##### Launch
    -   Select a template with a `basic configuration` for your EC2 instance.
    -   Configuration could include `OS, Application Server, or Application`.
    -   Select the `Instance type`, which is the specific `hardware configuration`.
-   ##### Connect
    -   There are several ways to connect to the instance.
    -   Programs and applications have multiple methods to connect directly to the instance and exchange data.
    -   Can also connect to the instance by logging in and accessing the computer desktop.
-   #### Use
    -   Run commands, install software, add storage, copy and organize files, and more.

## EC2 Instances Type

There are 5 categories of Instance Type.  
When selecting an instance type, consider the specific needs of your workloads and applications. This might include requirements for compute, memory, or storage capabilities.

### General purpose instances

Balance of compute, memory, and networking resources.  
(Basic Computer/VM Package)

-   Application servers, gaming servers
-   Backend servers for enterprise applications
-   Small and medium databases

### Compute-optimized instances

Compute-optimized applications are ideal for  
(CPU)

-   High-performance web servers, compute-intensive applications servers, and dedicated gaming server
-   Batch processing workloads that require processing many transactions in a single group

### Memory-optimized instances

Designed to deliver fast performance for workloads that process large datasets in memory.  
(RAM)

-   Workload that requires large amounts of data to be preloaded before running an application
-   High-performance database
-   Performing real-time processing of a large amount of unstructured data

### Accelerated computing instances

Hardware accelerators, or coprocessors, perform some functions more efficiently than is possible in software running on CPUs.  
In computing, a hardware accelerator is a component that can expedite data processing.  
(GPU, TPU, DPU)

-   Floating-point number calculations, graphics processing, and data pattern matching
-   Ideal for workloads such as graphics applications, game streaming, and application streaming

### Storage-optimized instances

Designed for workloads that require `high, sequential read and write access` to large datasets on local storage.  
Designed to deliver tens of thousands of low-latency, random IOPS to applications.  
In computing, the term `input/output operations per second (IOPS)` is a metric that measures the performance of a storage device.  
(HDD, SSD)

-   Application that has a high IOPS requirement
-   Distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems

## EC2 Pricing

### On-Demand
Start and stop an instance when you like
-   Short-term, irregular workloads that cannot be interrupted
-   No upfront costs or minimum contracts apply
-   Instances run continuously until you stop them
-   Developing and testing applications and running applications that have unpredictable usage patterns
-   Not recommended for workloads that last a year or longer
-   Better cost savings with **Reserved Instances** for longer usage

### Reserved Instances
Reserve an instance to use when u like
Reserved Instances come in `1-year or 3-year terms`.  
There are two available types of Reserved Instances:

-   **Standard Reserved Instances**:
    -   Good fit if you know the EC2 instance type and size you need
    -   And in which AWS Region do you plan to run them
    -   Standard Reserved Instances require you to state the following qualifications:
        -   Instance type and size: For example, `m5.xlarge`
        -   Platform description (operating system): For example, `Microsoft Windows Server or Red Hat Enterprise Linux`
        -   Tenancy: Default tenancy or dedicated tenancy
        -   Option to specify an `Availability Zone` for your `EC2 Reserved Instances`
-   **Convertible Reserved Instances**:
    -   Run EC2 Instances with different Availability Zones or different instance types
    -   Cost more when you require `flexibility` to run your EC2 instances

At the end of your Reserved Instance term you are charged On-Demand rates until you do one of the following:

-   Terminate the instance.
-   Purchase a new Reserved Instance that matches the instance attributes (instance family and size, Region, platform, and tenancy).

### Instance Savings Plans
Commit to a yearly plan to save cost 
- Reduce your EC2 instance costs when you `make an hourly spend commitment` to an instance family and Region for a `1-year or 3-year term`
- Any usage up to the commitment is charged at the discounted Savings Plans rate (for example, $1 per hour)
- Any usage beyond the commitment is charged at regular `On-Demand` rates
- Don't need to specify upfront what EC2 instance type and size (for example, `m5.xlarge`), OS, and tenancy to get a discount
- Savings Plans don't include an EC2 capacity reservation option

### Spot Instances
Utilizing unused EC2 instances.
- Ideal for workloads with `flexible start and end times`, or that can `withstand interruptions`
- Spot Instances use unused Amazon EC2 computing capacity
- Background processing job that can start and stop as needed (such as the data processing job for a customer survey)
- Spot Instance launches if you make a Spot request and Amazon EC2 capacity is available
- The request is not successful until Amazon EC2 capacity becomes available
- Unavailable capacity might delay the launch of your background processing job
- Instance may be interrupted if capacity is no longer available or demand for Spot Instances increases
- Might want to avoid unexpected interruptions when developing and testing applications

### Dedicated Hosts
Have a physical server dedicated to you
- Physical servers with Amazon EC2 instance capacity that is `fully dedicated to your use`
- Use your existing `per-socket, per-core, or per-VM software licenses` to help maintain license compliance
- Purchase `On-Demand Dedicated Hosts` or `Dedicated Hosts Reservations`
- `Most Expensive`

## Scaling Amazon EC2
Automatically add or remove Amazon EC2 instances in response to changing application demand.  
Maintain a greater sense of `application availability` by automatically scaling your instances in and out as needed.  
You can use two approaches: **dynamic scaling** and **predictive scaling**
- **Dynamic scaling** `responds` to changing demand
- **Predictive scaling** `automatically schedules` the right number of Amazon EC2 instances based on predicted demand.

### Amazon EC2 Auto Scaling
Auto Scaling component includes `Groups`, `Configuration Template`, and `Scaling Options`
- Create collections of EC2 instances, called Auto Scaling groups
- Specify the `minimum number` of instances in each Auto Scaling group, Amazon EC2 Auto Scaling ensures that your group never goes below this size
- Specify the `maximum number` of instances in each Auto Scaling group, Amazon EC2 Auto Scaling ensures that your group never goes above this size
- Specify the `desired capacity`, either when you create the group or at any time thereafter, Amazon EC2 Auto Scaling ensures that your group has this many instances. Defaults to minimum if number is not specified
- Specify scaling policies, Amazon EC2 Auto Scaling can launch or terminate instances as demand on your application increases or decreases
- Scaling policies adjust the number of instances, within your minimum and maximum number of instances, based on the criteria that you specify.

The following Auto Scaling group has a minimum size of one instance, a desired capacity of two instances, and a maximum size of four instances.  
![as-group-diagram](https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/c92e6da5-d0ac-40d1-84b5-a640af173170)
