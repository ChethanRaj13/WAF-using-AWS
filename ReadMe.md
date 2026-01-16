# AWS Web Application Firewall Project

This project shows how to deploy a basic web application on AWS using an EC2 instance, an Application Load Balancer and AWS Web Application Firewall (WAF). It also demonstrates how to allow, block and captcha incoming traffic based on IP addresses.

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
- How to build end to end secure cloud infrastructure on AWS
- How to route and protect traffic with an ALB and WAF
- How to control access and respond to real user requests in real time

## Next Steps
- Add VPC peering between networks
- Try integrating CloudFront and Shield
- Add logging and monitoring with CloudWatch
