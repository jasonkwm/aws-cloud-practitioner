# Table of Content

- [Connectivity to AWS](#connectivity-to-aws)
  - [Amazon Virtual Private Cloud (Amazon VPC)](#amazon-virtual-private-cloud-amazon-vpc)
  - [Internet gateway](#internet-gateway)
  - [Virtual private gateway](#virtual-private-gateway)
  - [AWS Direct Connect](#aws-direct-connect)
- [Subnets and Network Access Control Lists](#subnets-and-network-access-control-lists)
  - [Subnets](#subnets)
  - [Network traffic in a VPC](#network-traffic-in-a-vpc)
  - [Network ACLs](#network-acls)
    - [Stateless packet filtering](#stateless-packet-filtering)
  - [Security groups](#security-groups)
    - [Stateful packet filtering](#stateful-packet-filtering)
# Connectivity to AWS

### Amazon Virtual Private Cloud (Amazon VPC)
- A networking service that you can use to `establish boundaries` around your AWS resources
- Provision an `isolated section` of the AWS Cloud
- Within a virtual private cloud (VPC), you can organize your resources into subnets. A `subnet` is a section of a VPC that can contain resources such as Amazon EC2 instances

### Internet Gateway
To allow public traffic from the internet to access your VPC, you attach an internet gateway to the VPC.
- connection between a VPC and the internet  
<img width="600" alt="internet-gateway" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/e63247f1-4121-4646-97ea-68dc09129918">

### Virtual Private Gateway
Amazons habit of renaming things unnecessarily basically a `VPN`
- Enables you to establish a virtual private network (VPN) connection between your VPC and a private network, such as an on-premises data center or internal corporate network
- Allows traffic into the VPC only if it is coming from an approved network  
<img width="600" alt="vpn" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/86c3c925-0f00-4794-8b79-3a123930d246">

### AWS Direct Connect
- Establish a dedicated private connection between your data center and a VPC
- Helps you to reduce network costs and increase the amount of bandwidth that can travel through your network
<img width="600" alt="direct connect" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/a6647f6e-52b3-474a-ba9f-f162364668fe">


## Subnets and Network Access Control Lists

### Subnets
-  A section of a VPC in which you can group resources based on security or operational needs
-  Subnets can be public or private
-  A `Public Subnet` is a subnet that is associated with a route table that has a route to an Internet gateway
-  A `Private Subnet` doesn't have a route to an internet gateway

### Network traffic in a VPC
When a customer requests data from an application hosted in the AWS Cloud, this request is sent as a packet. A `packet` is a unit of data sent over the internet or a network. It enters into a VPC through an internet gateway.  
The VPC component that checks packet permissions for subnets is a [network access control list (ACL)](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html).


### Network ACLs
Network Access Control List is a virtual firewall that controls inbound and outbound traffic at the subnet level.
- Each AWS account includes a default network ACL
- You can use your account’s default network ACL or create custom network ACLs
- By default, your account’s default network ACL allows all inbound and outbound traffic, but you can modify it by adding your own rules
- For custom network ACLs, all inbound and outbound traffic is denied until you add rules to specify which traffic to allow
- All network ACLs have an explicit deny rule. This rule ensures that if a packet doesn’t match any of the other rules on the list, the packet is denied.

#### Stateless packet filtering
Network ACLs perform stateless packet filtering. They remember nothing and check packets that cross the subnet border each way: inbound and outbound. 

### Security groups
A security group is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance.
- By default, a security group denies all `inbound` traffic and allows all `outbound` traffic
- If you have multiple Amazon EC2 instances within the same VPC, you can associate them with the same security group or use different security groups for each instance.
#### Stateful packet filtering
Security groups perform stateful packet filtering. They remember previous decisions made for incoming packets.

**With both network ACLs and security groups, you can configure custom rules for the traffic in your VPC**  
<img width="600" alt=" acl and security" src="https://github.com/jasonkwm/aws-cloud-practitioner/assets/32697686/fe19e261-7a6e-4166-b093-d6ce01e22250">
