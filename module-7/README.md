# Table of Contents

- [Amazon CloudWatch](#)
  - [CloudWatch alarms](#)
  - [CloudWatch dashboard](#)
- [AWS CloudTrail](#)
  - [CloudTrail Insights](#)
- [AWS Trusted Advisor](#)
  - [AWS Trusted Advisor dashboard](#)



# Amazon CloudWatch
- A `web service` that enables you to `monitor and manage` various metrics and `configure alarm actions` based on data from those metrics
- `Metrics` are data about the performance of your systems
- CloudWatch uses metrics to represent the `data points` for your resources
- CloudWatch uses these metrics to `create graphs automatically` that show how `performance` has `changed over time`

## CloudWatch alarms
- You can `create alarms` that `automatically perform actions` if the value of your metric has `gone above or below` a `predefined threshold`
- You could create a **CloudWatch alarm** that `automatically stops` an **Amazon EC2 instance** when the `CPU utilization` percentage has remained below a `certain threshold` for a `specified period`
- You can specify to receive a `notification` whenever this `alarm is triggered`

## CloudWatch dashboard
- **CloudWatch dashboard** feature enables you to `access all the metrics` for your resources from a `single location`
- You can use a **CloudWatch dashboard** to `monitor`:
  - `CPU utilization` of an **Amazon EC2 instance**
  - Total `number of requests` made to an **Amazon S3 bucket**
- You can even `customize separate dashboards` for `different business purposes`, `applications`, or `resources`  
<img width="600" alt="cloudwatch dashboard" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/f32134bb-f9ec-485e-8299-fe1d9126d9b4">

# AWS CloudTrail
- `Records API calls` for your account
- `Recorded information` includes the `identity` of the API caller, the `time` of the API call, the `source IP address` of the API caller, and more
- You can think of **CloudTrail** as a “trail” of breadcrumbs (or a `log of actions`) that someone has left behind them
- You can view a `complete history` of `user activity` and `API calls` for your applications and resources
- `Events` are typically `updated` in **CloudTrail** within `15 minutes` after an API call
- `Filter events` by specifying the `time and date` that an API call occurred, the `user` who requested the action, the `type of resource` that was involved in the API call, and more
<img width="600" alt="cloudtrail" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/5a3e8b7b-ec49-44b9-84a5-be8862cc4e8d">

## CloudTrail Insights
- `Optional feature` allows **CloudTrail** to `automatically detect` unusual API activities in your **AWS account**

# AWS Trusted Advisor
- A `web service` that `inspects` your **AWS environment** and `provides real-time recommendations` in accordance with `AWS best practices`
- **Trusted Advisor** `compares its findings` to `AWS best practices` in `five categories`:
  - `cost optimization`, `performance`, `security`, `fault tolerance`, and `service limits`
- You can use **AWS Trusted Advisor** to `assist you` while you are `creating new workflows` and `developing new applications`
- You can also `use it` while you are `making ongoing improvements` to `existing applications and resources`

## AWS Trusted Advisor dashboard
- `Access` the **Trusted Advisor dashboard** on the **AWS Management Console**
- You can `review completed checks` for `cost optimization`, `performance`, `security`, `fault tolerance`, and `service limits`
- For each category:
  - The `green check` indicates the number of items for which it detected `no problems`
  - The `orange triangle` represents the number of `recommended investigations`
  - The `red circle` represents the number of `recommended actions`
<img width="600" alt="trusted advisor dashboard" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/d344db5d-4f0e-4dba-8351-1672bbeacc7d">

