# Complete_VPC_Architecture
VPC-Architecture

This project demonstrates a complete AWS VPC architecture created to understand and implement real-world AWS networking concepts.

The architecture includes public and private subnets, routing, security controls, a bastion host, load balancing, and private application resources.

The main goal of this project is to understand how different AWS networking components communicate with each other securely.

# Architecture

The project contains the following major components:

- Amazon VPC
- Public Subnets
- Private Subnets
- Internet Gateway (IGW)
- NAT Gateway
- Route Tables
- Security Groups
- Network ACLs (NACL)
- Bastion Host
- Application Load Balancer (ALB)
- EC2 Instances
- Auto Scaling Group
- Availability Zones

  AWS Services Used

1. Amazon VPC

Created a custom VPC to provide an isolated networking environment for the application infrastructure.

2. Public Subnets

Public subnets are connected to the Internet Gateway through their route table.

Resources such as the Bastion Host and Load Balancer can be placed in public subnets when internet accessibility is required.

3. Private Subnets

Private subnets are used for application resources that should not be directly accessible from the internet.

EC2 instances running inside private subnets can receive traffic through the Load Balancer.

4. Internet Gateway

The Internet Gateway provides communication between the VPC and the public internet for resources located in public subnets.

5. NAT Gateway

The NAT Gateway allows resources in private subnets to access the internet for outbound connections without exposing those private resources directly to incoming internet traffic.

6. Route Tables

Route tables control where network traffic is sent.

Separate routing was configured for public and private subnets.

7. Security Groups

Security Groups were configured as instance-level virtual firewalls.

They control inbound and outbound traffic for EC2 instances and other supported AWS resources.

8. Network ACL

Network ACLs provide an additional layer of security at the subnet level.

They control inbound and outbound traffic entering or leaving the subnet.
