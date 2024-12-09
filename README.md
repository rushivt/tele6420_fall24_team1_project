# Highly Available Web Environment Automation with Terraform and Ansible

This project demonstrates the automation of a highly available and scalable web environment on AWS using **Terraform** and **Ansible**. By leveraging Infrastructure as Code (IaC) principles, we dynamically provision AWS resources, configure services, and ensure auto-scaling capabilities for optimized performance.

## Key Features

- **AWS Environment Setup**:
  - VPC with DNS support and hostnames enabled.
  - Creation of subnets, internet gateway, and route tables.
  - Security groups for controlled ingress traffic.
  
- **Instance Configuration**:
  - Ansible provisioning to bake custom AMIs with necessary packages like Python3, Flask, and Ansible.
  - Environment variable-based configuration for enhanced flexibility.

- **Auto-Scaling**:
  - Auto-Scaling groups to manage EC2 instances based on CPU usage.
  - CloudWatch alarms to monitor and trigger scaling policies.

- **Optional Enhancements**:
  - Elastic Load Balancer integration.
  - Containerization for immutability and better resource utilization.

## Prerequisites

- Terraform installed locally.
- Ansible installed locally.
- AWS CLI configured with appropriate permissions.
- An active AWS account with necessary IAM policies.

## Project Structure

```plaintext
├── terraform/
│   ├── main.tf               # Main Terraform configuration file
│   ├── variables.tf          # Variables for customization
│   └── outputs.tf            # Output configurations
├── ansible/
│   ├── playbook.yml          # Ansible playbook for instance setup
│   └── inventory             # Inventory file for Ansible
├── README.md                 # Project documentation
└── screenshots/              # Screenshots for IaC steps
