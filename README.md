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
