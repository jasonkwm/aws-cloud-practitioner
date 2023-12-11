# Table of Content
- [AWS Free Tier](#)
  - [Always Free](#)
  - [12 Months Free](#)
  - [Trials](#)
- [AWS Pricing Concepts](#)
  - [How AWS pricing works](#)
    - [Pay for what you use](#)
    - [Pay less when you reserve](#)
    - [Pay less with volume-based discounts when you use more](#)
  - [AWS Pricing Calculator](#)
  - [AWS pricing examples](#)
    - [AWS Lambda](#)
    - [Amazon EC2](#)
    - [Amazon S3](#)
- [Billing Dashboard](#)
- [Consolidated Billing](#)
- [AWS Budgets](#)
- [AWS Cost Explorer](#)
- [AWS Support Plans](#)
  - [Basic Support](#)
  - [Developer Support](#)
  - [Business Support](#)
  - [Enterprise On-Ramp Support](#)
  - [Enterprise Support](#)
  - [Technical Account Manager (TAM)](#)
- [AWS Marketplace](#)
- [](#)
- [](#)



# AWS Free Tier
- Enables you to begin using certain services without having to worry about incurring costs for the specified period.
- `Three types` of offers are available: `Always Free`, `12 Months Free`, `Trial`
### Always Free
These offers `do not expire` and are `available to all` AWS customers.  
**Example:**
- **AWS Lambda** allows *1 million* `free requests` and up to *3.2 million seconds* of `compute time` per month
- **Amazon DynamoDB** allows *25 GB* of `free storage` per month

### 12 Months Free
These offers are `free for 12 months` following your `initial sign-up` date to AWS.  
**Examples:**
- Specific amounts of **Amazon S3 Standard Storage**
- Thresholds for `monthly hours` of **Amazon EC2** `compute time`
- Amounts of **Amazon CloudFront** `data transfer out`

### Trials
`Short-term free trial` offers start from the date you `activate a particular service`. The `length` of each trial might vary by `number of days` or the `amount of usage` in the service.  
**Examples:**
- **Amazon Inspector** offers a `90-day` free trial
- **Amazon Lightsail** (a service that enables you to run virtual private servers) offers `750 free hours` of usage over a `30-day` period

# AWS Pricing Concepts

## How AWS pricing works
AWS offers a range of cloud computing services with `pay-as-you-go` pricing.

### Pay for what you use
For each service, you pay for exactly the amount of resources that you actually use, `without requiring long-term contracts` or `complex licensing`. 
### Pay less when you reserve
Some services offer `reservation options` that provide a `significant discount` compared to `On-Demand Instance pricing`.
### Pay less with volume-based discounts when you use more
Some services offer `tiered pricing`, so the per-unit cost is `incrementally lower with increased usage`.

## AWS Pricing Calculator
- `Explore AWS services` and create an `estimate for the cost` of your use cases on AWS
- `Organize` your AWS estimates `by groups` that you define
- When you have `created an estimate`, you can `save it` and `generate a link` to `share it` with others

# Billing Dashboard
Pay your AWS bill, monitor your usage, and analyze and control your costs.
- `Compare` your `current` `month-to-date balance` with the `previous` month, and get a `forecast` of the `next` month based on current usage
- View `month-to-date spend` by service
- View `Free Tier usage` by service
- Access `Cost Explorer` and `create budgets`
- Purchase and manage `Savings Plans`
- `Publish` AWS Cost and Usage `Reports`

# Consolidated Billing

The **consolidated billing** feature of **AWS Organizations** enables you to receive a `single bill` for `all AWS accounts` in your organization.
- You can `easily track` the `combined costs` of all the `linked accounts` in your organization
- The `default maximum number of accounts` allowed for an organization is `4`, but you can `contact AWS Support` to `increase your quota`, if needed
- `Review itemized charges` incurred by `each account` on your `monthly bill`
- Have greater `transparency` into your organization’s accounts while still maintaining the convenience of receiving a single monthly bill
- `Share bulk discount` pricing, **Savings Plans**, and **Reserved Instances** across the accounts in your organization


# AWS Budgets
- `Create budgets` to plan your `service usage`, `service costs`, and `instance reservations`
- `Information` in **AWS Budgets** `updates` three times a day
- Helps you to `accurately determine` how close your `usage` is to your `budgeted amounts` or to the `AWS Free Tier limits`
- You can also `set custom alerts` when your `usage exceeds` (or is forecasted to exceed) the `budgeted amount`
<img width="650" alt="example of aws budgets" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/2872bff5-a3c0-4861-8c84-18071e0aaff7"/>

# AWS Cost Explorer
- A tool that lets you `visualize`, `understand`, and `manage` your `AWS costs` and `usage over time`
- **AWS Cost Explorer** includes a `default report` of the `costs and usage` for your `top five cost-accruing` **AWS services**
- `Apply custom filters` and `groups` to analyze your data. For **example**, you can view `resource usage` at the `hourly level`
- By `analyzing` your **AWS costs** over time, you can `make informed decisions` about `future costs` and how to `plan your budgets`
<img width="529" alt="aws cost explorer" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/6651975c-3141-44f0-bebe-05f5ea0845f3">

# AWS Support Plans
**AWS** offers `four different` **Support plans** to help you `troubleshoot issues`, `lower costs`, and `efficiently` use **AWS services**.  
You can `choose` from the following **Support plans** to meet your company’s needs:  
- `Basic`, `Developer`, `Business`, `Enterprise On-Ramp`, `Enterprise`

The `Developer`, `Business`, `Enterprise On-Ramp`, and `Enterprise Support` plans have `pay-by-the-month pricing` and require `no long-term contracts`.  
In general, for `pricing`, the `Developer plan` has the `lowest cost`, the `Business` and `Enterprise On-Ramp plans` are in the `middle`, and the `Enterprise plan` has the `highest cost`.

## Basic Support
- `Free for all` **AWS customers**
- Includes access to `whitepapers`, `documentation`, and `support communities`
- You can also `contact AWS` for `billing questions` and `service limit increases`
- Have `access` to a `limited selection` of **AWS Trusted Advisor** checks
- You can use the **AWS Personal Health Dashboard**, a tool that `provides alerts` and `remediation guidance` when **AWS** is `experiencing events` that may affect you

## Developer Support
**Developer Support** plan have `access to features` such as:
- `Best practice` guidance
- Client-side `diagnostic` tools
- Building-block `architecture support`, which consists of guidance for `how to use` `AWS offerings`, `features`, and `services together`

## Business Support
**Business Support** plan have `access to additional features`, including: 
- `Use-case guidance` to identify `AWS offerings`, `features`, and `services` that can `best support` your specific needs
- All **AWS Trusted Advisor** checks
- `Limited support` for `third-party software`, such as common `operating systems` and `application stack components`

## Enterprise On-Ramp Support
`All the features` included in the `Basic`, `Developer`, and `Business Support plans`  
**Enterprise On-Ramp Support** plan also have access to:
- A pool of `Technical Account Managers` to `provide proactive guidance` and `coordinate access` to programs and **AWS experts**
- A `Cost Optimization workshop` (*one per year*)
- A `Concierge support team` for `billing` and `account assistance`
- Tools to `monitor costs` and `performance` through **Trusted Advisor** and **Health API/Dashboard**

**Enterprise On-Ramp Support** plan also `provides access` to a specific set of `proactive support services`, which are provided by a pool of `Technical Account Managers`.  
- `Consultative review` and `architecture guidance` (*one per year*)
- `Infrastructure Event Management` support (*one per year*)
- Support `automation workflows`
- *30 minutes or less* `response time` for `business-critical issues`


## Enterprise Support
`All features` included in the `Basic`, `Developer`, `Business`, and `Enterprise On-Ramp` support plans.  
`Enterprise Support` also have access to:
- A designated `Technical Account Manager` to provide `proactive guidance` and `coordinate access` to programs and **AWS experts**
- A `Concierge support team` for `billing` and `account assistance`
- `Operations Reviews` and tools to `monitor health`
- `Training` and `Game Days` to drive `innovation`
- Tools to `monitor costs` and `performance` through **Trusted Advisor** and **Health API/Dashboard**

Provides `full access` to designated **Technical Account Manager**:
- `Consultative review` and `architecture guidance`
- `Infrastructure Event Management` support
- `Cost Optimization Workshop` and `tools`
- Support `automation workflows`
- *15 minutes or less* `response time` for `business-critical issues`

## Technical Account Manager (TAM)
The `Enterprise On-Ramp` and `Enterprise Support plans` include access to a **Technical Account Manager (TAM)**.  
- **TAM** is your `primary point of contact` at **AWS**
- **TAM** `educates`, `empowers`, and `evolves` your cloud journey across the full range of **AWS services**
- **TAMs** provide `expert engineering guidance`, help you `design solutions` that `efficiently integrate AWS services`, assist with `cost-effective` and `resilient architectures`, and `provide direct access` to **AWS programs** and a broad community of experts

# AWS Marketplace
A digital catalog that includes thousands of software listings from independent software vendors
