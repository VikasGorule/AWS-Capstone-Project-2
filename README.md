# AWS-Capstone-Project-2
This project involves designing &amp; implementing a highly available &amp; scalable web application infrastructure on AWS. Architecture will leverage AWS services to ensure Fault tolerance,Load balancing,Secure user access. Project core is to deploy  web application that can handle varying loads efficiently &amp; maintain high availability across multiple AZs

## 🧱 Architecture Components

The solution is designed using the following AWS services:

- **Amazon EC2**: Hosts the PHP-based web application.
- **Auto Scaling Group (ASG)**: Automatically adjusts the number of EC2 instances based on traffic demand.
- **Application Load Balancer (ALB)**: Distributes incoming traffic across EC2 instances in multiple Availability Zones.
- **Amazon VPC**: Custom Virtual Private Cloud for network isolation and security.
- **Public and Private Subnets**: Public subnets for web servers; private for NFS and backend components.
- **NAT Gateway**: Allows instances in private subnets to access the internet securely.
- **NFS Server**: Provides shared storage for EC2 instances to maintain consistency of application data (e.g., user uploads).
- **Security Groups and NACLs**: Enforce fine-grained traffic control.

## ⚙️ Features

- ✅ High Availability using Multi-AZ deployment for EC2 and NFS
- ✅ Auto Scaling Group for handling fluctuating web traffic
- ✅ Load Balancer for traffic distribution and health checks
- ✅ Shared file storage using NFS for consistent data across instances
- ✅ Secure network segmentation using VPC

## 🚀 Deployment Steps

1. **Set up the VPC**  
   - Create a custom VPC with public and private subnets across multiple Availability Zones.

2. **Deploy NFS Server**  
   - Launch an EC2 instance in a private subnet and configure it as an NFS server.

3. **Configure Auto Scaling Group and Launch Template**  
   - Install PHP and mount the NFS volume via user-data script.
   - Ensure all instances connect to the same shared storage.

4. **Create Application Load Balancer (ALB)**  
   - Register EC2 instances in target groups.
   - Configure listeners and health checks.

5. **Security Configuration**  
   - Set up Security Groups to restrict access to EC2 and NFS.
   - Use least privilege principles for all components.

## 🖼️ Architecture Diagram

<img width="700" height="502" alt="image" src="https://github.com/user-attachments/assets/d46967e9-a4bd-44e7-aae3-faba958efee4" />

<img width="429" height="496" alt="image" src="https://github.com/user-attachments/assets/0cba9820-f5dc-4257-80a3-57825c49cf4e" />



