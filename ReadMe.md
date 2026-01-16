# AWS Web Application Firewall Project

This project shows how to deploy a basic web application on AWS using an EC2 instance, an Application Load Balancer, and AWS Web Application Firewall (WAF). It also demonstrates how to allow, block, and captcha incoming traffic based on IP addresses.

## What I Built

### 1. Network Setup
- Created a custom VPC
- Added 2 public subnets in different availability zones
- Attached an Internet Gateway and set up routing so traffic could reach the internet

### 2. Web Server Deployment
- Launched a t2.micro EC2 instance running Ubuntu
- Opened Port 22 for SSH and Port 80 for web traffic
- Used User Data to install Apache and set up a simple webpage

### 3. Application Load Balancer
- Created a target group and registered the EC2 instance
- Set up an internet-facing ALB that listens on Port 80
- Accessed the web app using the ALB DNS endpoint

### 4. AWS WAF Security Rules
- Created a Web ACL and attached it to the ALB
- Built an IP Set for testing
- Tested all traffic control actions:
  - Block (returned 403 Forbidden)
  - Allow (normal access)
  - Captcha challenge (user solves puzzle before entry)

## What This Project Demonstrates
- How to build an end-to-end secure cloud infrastructure on AWS
- How to route and protect traffic with an ALB and WAF
- How to control access and respond to real user requests in real time

<img width="1920" height="1080" alt="Screenshot 2025-12-30 164811" src="https://github.com/user-attachments/assets/38bb67a4-0881-4635-8739-4d0568693eac" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165116" src="https://github.com/user-attachments/assets/6f8a676f-cb59-40b9-a316-4e5a28eb780a" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165150" src="https://github.com/user-attachments/assets/201fc4f7-8f2c-4572-a534-1654e188984e" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165208" src="https://github.com/user-attachments/assets/65d58c93-e7d0-47b1-ba02-27535ff9e65c" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165329" src="https://github.com/user-attachments/assets/a829fe29-b7e3-4b4e-b866-04463a884128" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165533" src="https://github.com/user-attachments/assets/2b2fd1c0-0121-47bf-bee7-187eb38de917" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165624" src="https://github.com/user-attachments/assets/f5a6f43c-25fa-4c22-8456-c2ed4f6215cb" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165635" src="https://github.com/user-attachments/assets/ca6fc731-4dd3-4041-8f17-f9cdaec0d7a7" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165708" src="https://github.com/user-attachments/assets/99428609-a01f-4ba5-9abc-c6af9a28d298" />
<img width="1920" height="1080" alt="Screenshot 2025-12-30 165738" src="https://github.com/user-attachments/assets/4d39a89b-31c2-4f5b-a7c3-1ad8b7e7636e" />











