# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Thuleer R
* **Register Number**: 212225230285
* **Date of Submission**: 17/08/2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

1.I logged in to the AWS Management Console and created a new VPC with the CIDR block 10.0.0.0/16 to provide an isolated network environment for my resources.

2.Inside the VPC, I created a public subnet with the CIDR block 10.0.1.0/24 and enabled Auto-assign Public IPv4 Address so that instances launched in the subnet 

could receive public IP addresses.

3.I created an Internet Gateway (IGW) and attached it to the VPC. Then, I created a route table, added a default route (0.0.0.0/0) pointing to the IGW, and 

associated the route table with the public subnet to enable internet connectivity.

4.Next, I created a security group and configured inbound rules to allow SSH (Port 22) for remote access and HTTP (Port 80) for web traffic. After that, I 

launched an Amazon EC2 instance using the Amazon Linux 2 AMI in the public subnet and attached the security group and key pair.

5.Finally, I connected to the EC2 instance, installed and started the Apache HTTP Server (httpd), created a simple HTML web page, and verified that the website 

was accessible through a web browser using the instance's public IP address.

## Output Screenshots (Attach 3)
<img width="1917" height="936" alt="Screenshot 2026-08-17 141752" src="https://github.com/user-attachments/assets/24b33507-c1d0-439c-932a-ff68f2815cff" />


<img width="1909" height="928" alt="Screenshot 2026-08-17 142039" src="https://github.com/user-attachments/assets/2e61b51c-b8c7-4a94-b91b-796c5fe672e8" />

<img width="1911" height="986" alt="Screenshot 2026-08-17 144652" src="https://github.com/user-attachments/assets/04525aa9-5736-4c30-b66a-2582b6e10537" />

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
