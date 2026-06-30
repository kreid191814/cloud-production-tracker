# Cloud Production Tracking Platform

## Project Overview

This project demonstrates the design and implementation of a scalable AWS cloud application for tracking daily production metrics. The solution is inspired by an enterprise workflow I previously developed using SharePoint and Excel and has been redesigned using AWS cloud services to improve scalability, automation, security, and reporting.

---

## Business Problem

The current process relies on manual spreadsheets to track daily production and generate weekly reports. As the number of users grows, the process becomes difficult to manage, scale, and maintain.

---

## Business Goals

The solution will:

- Replace manual spreadsheets with a cloud-based application.
- Centralize production data in a secure database.
- Allow users to securely submit daily production metrics.
- Provide dashboards for managers to monitor productivity.
- Automatically archive weekly production data.
- Generate AI-powered weekly production summaries.
- Support a scalable architecture capable of handling increasing numbers of users.

---

## Planned AWS Architecture

The solution will be designed using AWS services including:

- Amazon VPC
- Public and Private Subnets
- Internet Gateway
- Route Tables
- Security Groups
- EC2
- Application Load Balancer
- Auto Scaling
- Amazon DynamoDB
- AWS Lambda
- Amazon S3
- Amazon CloudWatch
- AWS IAM

---

## Current Status

🚧 Sprint 1 – Project Planning

Current Tasks:
- Define business requirements
- Design AWS architecture
- Build networking foundation (VPC)

## Sprint 1 - Networking Foundation ✅

### Completed

- Designed a custom Amazon VPC
- Configured a scalable IPv4 CIDR block (10.0.0.0/16)
- Created two public subnets across two Availability Zones
- Created two private subnets across two Availability Zones
- Configured an Internet Gateway
- Configured route tables
- Added an Amazon S3 Gateway Endpoint
- Enabled DNS resolution and DNS hostnames

### Key Design Decisions

- Used two Availability Zones to improve high availability.
- Separated internet-facing resources from backend resources using public and private subnets.
- Implemented a scalable network foundation for future Auto Scaling and Load Balancing.

## Sprint 2 - Compute 🚧

### Completed

- Launched an Amazon EC2 instance using Amazon Linux 2023.
- Configured SSH access using an RSA key pair.
- Deployed the instance into a custom Amazon VPC.
- Placed the instance in a public subnet.
- Created and configured a Security Group allowing SSH (22) and HTTP (80).
- Connected securely to the EC2 instance from macOS using SSH.
- Installed and configured Apache HTTP Server (httpd).
- Enabled Apache to start automatically after system reboots.
- Deployed a static web application accessible from the internet using the EC2 public IP address.

### Lessons Learned

- EC2 instances inherit networking from the VPC and subnet they are deployed into.
- A subnet is considered public when its route table contains a route to an Internet Gateway.
- Security Groups control which network traffic is allowed to reach an EC2 instance.
- Apache must be installed and started before a web server can serve content.
- Verifying the VPC and subnet before launching an EC2 instance is critical to ensure the infrastructure
  matches the intended architecture.
- SSH key pairs provide secure administrative access without using passwords.

### Deployment Verification

## Deployment Verification

The Cloud Production Tracker application was successfully deployed to an Amazon EC2 instance running Amazon Linux 2023 within a custom Amazon VPC.

The application is hosted using Apache HTTP Server and is accessible through the EC2 public IPv4 address.

![Cloud Production Tracker Homepage](cloud-production-tracker-homepage/screenshots.png)
