# Terraform-project
This Terraform configuration creates a robust web app setup on AWS. It spreads EC2 instances across availability zones for reliability. Network Load Balancers (NLB) handle public traffic to NGINX proxies, while Application Load Balancers (ALB) route requests to private APACHE web servers. 


## Project Objective

The primary goal of this project is to design and deploy an AWS infrastructure that maximizes security and availability while optimizing cost-efficiency. The public-private subnet architecture, which segregates resources into distinct network segments based on their level of exposure to the internet, plays a pivotal role in achieving this objective.

## Key Components in the architecture

To achieve the project’s objectives, we will explore and implement the following key components:

1-Amazon Virtual Private Cloud (Amazon VPC): A logically isolated section of the AWS cloud where we will define our network and deploy our resources.

2-Public Subnet: A subnet within the VPC where resources that require direct internet access will reside. This includes components like load balancers and web servers.

3-Private Subnet: A subnet that is not directly accessible from the internet. Resources that store sensitive data or backend servers will be placed here, enhancing security.

4-Network Address Translation (NAT) Gateway: A mechanism used to allow resources in the private subnet to access the internet while maintaining a secure barrier from inbound connections.

5-Security Groups and Network ACLs: Security measures that control inbound and outbound traffic at the instance and subnet levels, bolstering the overall security posture.

6-Route Tables: Configuration tables that determine the routing of network traffic within the VPC.

7-Auto Scaling Group (ASG): Automatically adjusts the number of EC2 instances to meet demand, ensuring high availability and scalability for applications.

8-Launch Configuration: Defines the blueprint for EC2 instances in an Auto Scaling group, specifying the AMI, instance type, and other configuration details.

9-Target Group: A logical group of instances or resources that receive traffic from a load balancer, allowing for fine-grained routing and load balancing decisions based on health and routing rules.

10-Load Balancer: Distributes incoming network traffic across multiple servers or resources to ensure high availability, improve application performance, and prevent overloading of individual servers.

11-Application Load Balancer (ALB): Distributes incoming application traffic across multiple targets, such as EC2 instances, based on defined rules and supports advanced routing features.

12-Amazon EC2 (Elastic Compute Cloud): Provides resizable compute capacity in the cloud, allowing you to run virtual servers (EC2 instances) for various applications, services, and workloads.
