# 🌐 Build a Virtual Private Cloud (Amazon VPC)

## 📖 Project Overview

This project demonstrates how to design and configure a secure virtual network using **Amazon Virtual Private Cloud (Amazon VPC)**, one of the core networking services in AWS. A VPC provides a logically isolated network where AWS resources such as Amazon EC2 instances, databases, and load balancers can be securely deployed and managed.

During this project, I created a custom Amazon VPC, configured a public subnet, enabled automatic public IPv4 address assignment, created and attached an Internet Gateway, and explored how these networking components work together to provide secure internet connectivity. Additionally, I completed the secret mission by provisioning VPC resources using **AWS CloudShell** and the **AWS Command Line Interface (AWS CLI)**, gaining practical experience with cloud infrastructure automation.

This project strengthened my understanding of AWS networking fundamentals and introduced concepts that are essential for Cloud Engineers, DevOps Engineers, and Cloud Security Engineers.

---

# 🎯 Project Objectives

The objectives of this project were to:

* Build a custom Amazon Virtual Private Cloud (VPC)
* Understand IPv4 CIDR block allocation
* Create and configure a public subnet
* Enable automatic public IPv4 address assignment
* Create and attach an Internet Gateway
* Learn how VPC networking components communicate
* Automate resource creation using AWS CloudShell and AWS CLI
* Understand AWS networking best practices

---

# ☁ AWS Services Used

## Amazon Virtual Private Cloud (Amazon VPC)

Amazon VPC is a networking service that enables users to create a logically isolated virtual network inside AWS. It provides complete control over networking components such as IP addressing, subnets, route tables, gateways, and security controls.

### Features

* Custom IP Address Ranges
* Public and Private Subnets
* Route Tables
* Internet Gateway
* Network Isolation
* Secure Communication

---

## AWS CloudShell

AWS CloudShell is a browser-based command-line environment that comes preconfigured with AWS CLI. It allows users to manage AWS resources directly from the AWS Console without installing software on their local machine.

---

## AWS Command Line Interface (AWS CLI)

AWS CLI is a command-line tool that enables users to create, configure, and manage AWS resources programmatically. It simplifies repetitive tasks and supports automation and Infrastructure as Code (IaC) practices.

---

# 🏗 Project Architecture

```
                 Internet
                     │
                     ▼
            Internet Gateway
                     │
                     ▼
        Amazon Virtual Private Cloud
                     │
                     ▼
              Public Subnet
                     │
                     ▼
          AWS Resources (EC2)
```

---

# 🚀 Implementation Steps

## Step 1 — Created a Custom Amazon VPC

* Opened the Amazon VPC Console
* Created a new VPC
* Configured the IPv4 CIDR Block
* Assigned a Name Tag

The VPC acts as the private virtual network where AWS resources are securely deployed.

---

## Step 2 — Created a Public Subnet

After creating the VPC, I created a subnet inside it.

The subnet:

* Uses a smaller CIDR block from the VPC
* Represents a logical network segment
* Can host AWS resources

I also enabled **Auto-Assign Public IPv4 Addresses** so that EC2 instances launched inside this subnet automatically receive a public IP address.

---

## Step 3 — Created an Internet Gateway

Created an Internet Gateway (IGW) and attached it to the VPC.

The Internet Gateway enables communication between resources inside the VPC and the public internet.

Without an Internet Gateway, resources inside the VPC cannot communicate directly with external networks.

---

## Step 4 — Used AWS CloudShell

Instead of creating resources only through the AWS Management Console, I also used AWS CloudShell to provision VPC resources using AWS CLI commands.

Commands executed included:

* Create VPC
* Tag VPC
* Create Subnet
* Create Internet Gateway
* Attach Internet Gateway

This provided practical experience with infrastructure automation.

---

# 🔐 Networking & Security Concepts Learned

## Amazon VPC

A Virtual Private Cloud (VPC) is a logically isolated virtual network that enables secure deployment of AWS resources.

---

## IPv4 CIDR Block

CIDR (Classless Inter-Domain Routing) defines the IP address range available within a VPC or subnet.

Example:

```
10.0.0.0/24
```

The CIDR block determines the number of available IP addresses.

---

## Subnet

A subnet is a smaller network created inside a VPC.

Subnets improve:

* Network organization
* Security
* Availability
* Scalability

---

## Public Subnet

A Public Subnet is associated with a route table that contains a route to an Internet Gateway.

Resources inside a public subnet can communicate with the internet if they have a public IP address.

---

## Internet Gateway

An Internet Gateway is a highly available AWS networking component that connects a VPC to the internet.

It enables:

* Outbound Internet Access
* Inbound Internet Connectivity
* Public Application Hosting

---

## AWS CloudShell

CloudShell is a browser-based Linux shell that includes AWS CLI and automatically uses the permissions of the logged-in AWS user.

---

## AWS CLI

AWS CLI allows administrators to automate AWS resource creation using commands instead of manually configuring resources through the AWS Console.

---

# 🔒 Security Best Practices Followed

During this project, I learned several networking security best practices:

* Used a custom VPC instead of relying on the default VPC.
* Configured a dedicated public subnet.
* Enabled public IPv4 assignment only where required.
* Attached an Internet Gateway only to provide controlled internet access.
* Used AWS CLI to automate infrastructure deployment.
* Followed modular network design principles for scalability and security.

---

# 💼 Skills Demonstrated

* Amazon VPC Administration
* AWS Networking
* CIDR Planning
* Subnet Design
* Internet Gateway Configuration
* AWS CloudShell
* AWS CLI
* Infrastructure Automation
* Network Architecture
* Cloud Infrastructure Management
* AWS Security Best Practices
* Cloud Networking Fundamentals

---

# 📄 Project Documentation

Complete project documentation can be found on NextWork:

👉 **[Build a Virtual Private Cloud (Amazon VPC)](https://learn.nextwork.org/confident_maroon_kind_tapir/docs/aws-networks-vpc)**

---

# 🎯 Project Outcome

Successfully designed and configured a custom Amazon Virtual Private Cloud, created a public subnet, attached an Internet Gateway, and understood how AWS networking components interact to enable secure communication. I also gained practical experience using AWS CloudShell and AWS CLI to automate the deployment of networking resources, strengthening my understanding of cloud networking and infrastructure management.

---

# 🧠 Key Takeaways

After completing this project, I gained hands-on experience with:

* Amazon VPC
* IPv4 CIDR Blocks
* Public Subnets
* Internet Gateways
* AWS Networking
* AWS CloudShell
* AWS CLI
* Infrastructure Automation
* Network Design
* Cloud Security Fundamentals
* AWS Best Practices

