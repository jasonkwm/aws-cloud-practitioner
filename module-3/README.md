# Table of Content
- [AWS Global Infrastructure](#aws-global-infrastructure)
  - [Selecting a Region](#selecting-a-region)
  - [Availability Zones](#availability-zones)
- [Edge Locations CDN](#edge-locations-cdn)
- [How to Provision AWS Resources](#how-to-provision-aws-resources)
  - [AWS Elastic Beanstalk](#aws-elastic-beanstalk)
  - [AWS CloudFormation](#aws-cloudformation)
# AWS Global Infrastructure

## Selecting a Region
When `determining` the right `Region` for your services, data, and applications, `consider` the following `four business factors`.

- `Compliance` with `data governance` and `legal requirements`
  - `Location-specific` data regulations
- `Proximity` to your `customers`
  - `Faster content delivery` to customers
- `Available services` within a Region
  - Region might not have all the features that you want to offer to customers
- `Pricing`
  - `Cost of services` can `vary` from Region to Region.

## Availability Zones
- A `single data center` or a `group` of data centers `within a Region`
- `Availability Zones` are located `tens of miles apart` from each other
- `Close enough` to have `low latency` between **Availability Zones**
- `Distant enough` to reduce the chance of a `disaster` affecting **multiple Availability Zones**.

# Edge Locations (CDN)
**Amazon CloudFront** uses to `store cached copies` of your content closer to your customers for `faster delivery`.

# How to Provision AWS Resources

## Ways to interact with AWS services

#### AWS Management Console
- `Web-based interface` for accessing and managing AWS services
- `Quickly access` recently used services and `search for other services`
- `Includes wizards` and `automated workflows` that can `simplify` the process of `completing tasks`
- Use `AWS Console mobile application` to perform tasks such as `monitoring resources`, `viewing alarms`, and `accessing billing information`

#### AWS Command Line Interface (AWS CLI)
- `Save time` when making API requests
- `Control multiple AWS services directly` from the command line within one tool
- `Automate` the actions that your services and applications perform `through scripts`

#### Software Development Kit (SDK)
- Make it `easier` for you to `use AWS services through an API` designed for your `programming language` or `platform`

## AWS Elastic Beanstalk
`Provide code` and `configuration settings`, and **Elastic Beanstalk** deploys the resources necessary to perform the following tasks:
- `Adjust capacity`
- `Load balancing`
- `Automatic scaling`
- `Application health monitoring`

## AWS CloudFormation
- Treat your `infrastructure as code`
- Build an environment by `writing lines of code` instead of using the **AWS Management Console** to `individually provision resources`
- It `determines the right operations` to perform when `managing your stack` and `rolls back changes` automatically if it `detects errors`
