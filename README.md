# EC Autoscaling and Load Balancing

![Enrollment](Images/ASG.png)

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

![Enrollment](Images/Vpc.png)


![Enrollment](Images/VPC2.png)

# Enable auto-assign public IPv4 address to your Public1 and Public2 subnet

![Enrollment](Images/publicipv4.png)

![Enrollment](Images/Enable-Auto-assgn.png)


# 2. Security Group Configuration:

Create 2 Security groups.

__1.__ ALB to accept HTTP inbound traffic from anywhere

![Enrollment](Images/ALB-sg.png)

__2.__ Web-sg-1 to accept HTTP inbound traffic from ALB

![Enrollment](Images/web-sg-1.png)



# 3. Target Group Setup: 

Set up a target group to route traffic to the registered EC2 instances within the autoscaling group. Define health checks and protocols.

__Vpc__ = Vpc you created

![Enrollment](Images/TG1.png)

# 4. Load Balancer Configuration:

Configure an Application Load Balancer to distribute incoming traffic across multiple EC2 instances. Define listeners and routing rules.

__1. Select ALB__

![Enrollment](Images/ALB.png)

__2. ALB Configuration__

![Enrollment](Images/ALB-setup.png)

# 5. Launch Template Creation:

Create a launch template to define the configuration settings for the EC2 instances launched by the autoscaling group.

__1. Choose an AMI from the Catalog__

![Enrollment](Images/Launch-temp1.png)

__2. Select the preferred instance from the Instance type__ 

![Enrollment](Images/launch-temp2.png)

__3. On Advance details scroll to the User data and paste the user data provided.__  

![Enrollment](Images/Launch-temp3.png)



# 6.Autoscaling Group Configuration:

Configure an autoscaling group to automatically adjust the number of EC2 instances based on metrics such as CPU utilization or network traffic. 

Associate the autoscaling group with the launch template and target group.


![Enrollment](Images/ASG1.png)

![Enrollment](Images/ASG2.png)

![Enrollment](Images/ASG3.png)

![Enrollment](Images/ASG4.png)

