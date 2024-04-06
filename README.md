# EC2-Autoscaling-and-Load-Balancing-Project

Welcome to the EC2 Autoscaling and Load Balancing project repository! This project is designed to showcase the implementation of autoscaling and load balancing for EC2 instances on AWS. Below, you'll find an overview of the project, including resources utilized and setup instructions.

# Overview

The EC2 Autoscaling and Load Balancing project leverages AWS services to ensure high availability, scalability, and fault tolerance for applications running on EC2 instances. 

By combining autoscaling and load balancing, the project achieves dynamic scaling of resources based on demand and distributes incoming traffic evenly across multiple instances.

# Resources Utilized

The following AWS resources are utilized in this project:

__VPC (Virtual Private Cloud):__ A new VPC is created to isolate the network environment for the EC2 instances.

__Security Group:__ Security groups are configured to control inbound and outbound traffic to the EC2 instances.

__Target Group:__ Target groups are used to route traffic to the registered EC2 instances within the autoscaling group.

__Load Balancer:__ Application Load Balancer is configured to distribute incoming traffic across multiple EC2 instances.

__Launch Template:__ A launch template is created to define the configuration settings for the EC2 instances launched by the autoscaling group.

__Autoscaling Group:__ An autoscaling group is configured to automatically adjust the number of EC2 instances based on metrics such as CPU utilization or network traffic.

# Benefits:

__Scalability:__ The autoscaling group automatically provisions additional instances when traffic increases, ensuring smooth performance even during peak loads.

__High Availability:__ The load balancer distributes traffic across healthy instances, preventing a single point of failure. If an instance becomes unhealthy, the autoscaling group automatically replaces it.

__Cost Optimization:__ By automatically scaling resources based on demand, you only pay for the compute power you actually use.

# Setup :

# 1. VPC Creation: 
Create a new VPC in the AWS Management Console to isolate the network environment for the EC2 instances.

# 2. Security Group Configuration:

Configure security groups to control inbound and outbound traffic to the EC2 instances. Define rules to allow necessary communication.

# 3. Target Group Setup: 

Set up a target group to route traffic to the registered EC2 instances within the autoscaling group. Define health checks and protocols.

# 4. Load Balancer Configuration:

Configure an Application Load Balancer to distribute incoming traffic across multiple EC2 instances. Define listeners and routing rules.

# 5. Launch Template Creation:

Create a launch template to define the configuration settings (e.g., AMI, instance type, key pair) for the EC2 instances launched by the autoscaling group.

# 6.Autoscaling Group Configuration:

Configure an autoscaling group to automatically adjust the number of EC2 instances based on metrics such as CPU utilization or network traffic. Associate the autoscaling group with the launch template and target group.
