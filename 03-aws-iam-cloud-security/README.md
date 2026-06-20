# 🔐 Cloud Security with AWS IAM

## 📌 Project Overview

This project demonstrates how to secure AWS resources using **AWS Identity and Access Management (IAM)**. I learned how to control access to Amazon EC2 instances by creating IAM users, user groups, and custom IAM policies. The project follows the **Principle of Least Privilege**, ensuring users receive only the permissions required to perform their tasks.

To simulate a real-world enterprise environment, I launched separate **Production** and **Development** EC2 instances, created an IAM policy that grants access only to the development instance, and verified permissions using the AWS IAM Policy Simulator.

---

# 🎯 Objectives

The primary objectives of this project were to:

- Launch Amazon EC2 instances
- Understand AWS Identity and Access Management (IAM)
- Create IAM Policies using JSON
- Create IAM Users
- Create IAM User Groups
- Apply Least Privilege access
- Use Resource Tags for access control
- Create an AWS Account Alias
- Test user permissions
- Validate policies using the IAM Policy Simulator

---

# ☁ AWS Services Used

## AWS Identity and Access Management (IAM)

AWS IAM is a security service that enables administrators to securely manage authentication and authorization for AWS resources.

IAM allows administrators to:

- Create users
- Create groups
- Create roles
- Define permissions
- Control access to AWS services

IAM is one of the most important AWS security services.

---

## Amazon EC2 (Elastic Compute Cloud)

Amazon EC2 is a cloud computing service that provides scalable virtual machines called **Instances**.

EC2 instances are commonly used to:

- Host web applications
- Run databases
- Execute software
- Deploy enterprise applications

In this project, two EC2 instances were created:

- Production
- Development

---

# 🏗 Project Architecture

```

AWS Account
│
├── IAM
│ ├── IAM User
│ ├── IAM Group
│ └── IAM Policy
│
└── Amazon EC2
├── Production Instance
└── Development Instance

```

The IAM Policy grants access only to the Development EC2 instance while restricting access to the Production instance.

---

# 🚀 Implementation Steps

## Step 1 — Launched Amazon EC2 Instances

Created two EC2 instances:

- Production Instance
- Development Instance

These instances simulate two different application environments.

---

## Step 2 — Tagged EC2 Instances

Assigned the following tags:

| Key | Value |
|------|--------|
| Env | Production |
| Env | Development |

Resource tags help organize AWS resources and enable **Tag-Based Access Control**.

---

## Step 3 — Created a Custom IAM Policy

Created an IAM Policy using JSON.

The policy:

- Allowed EC2 actions only on instances tagged as **Development**
- Allowed EC2 Describe actions
- Denied CreateTags
- Denied DeleteTags

This ensured users could manage only Development resources.

---

## Step 4 — Created an AWS Account Alias

Configured a custom AWS Account Alias.

Benefits include:

- Easier login URL
- Improved user experience
- Easier account identification
- Professional sign-in experience

---

## Step 5 — Created an IAM User Group

Created a dedicated user group for interns.

Instead of assigning permissions individually, permissions were attached to the group.

This simplifies user management.

---

## Step 6 — Created an IAM User

Created a new IAM user for the intern.

The user received:

- Username
- Temporary password
- AWS Sign-in URL

The user was added to the Intern Group.

---

## Step 7 — Tested User Permissions

Logged into AWS using the IAM user.

Permission testing results:

### Production Instance

Attempted to stop the Production EC2 instance.

Result:

Access Denied

The IAM Policy correctly blocked access.

---

### Development Instance

Attempted to stop the Development EC2 instance.

Result:

Success

The policy correctly allowed access.

---

## Step 8 — Used IAM Policy Simulator

Validated permissions using the AWS IAM Policy Simulator.

Simulation Results:

- StopInstances → Allowed
- DeleteTags → Denied

The simulator confirmed that the policy was working correctly without modifying actual AWS resources.

---

# 🔐 Security Best Practices Implemented

During this project, I followed several AWS security best practices:

- Principle of Least Privilege
- IAM User instead of Root User
- Group-Based Permission Management
- JSON IAM Policies
- Tag-Based Access Control
- Explicit Deny Rules
- Permission Validation using IAM Policy Simulator

---

# 📚 Key Concepts Learned

## IAM User

An IAM User represents an individual person or application that requires access to AWS resources.

Each user has unique credentials and permissions.

---

## IAM Group

An IAM Group is a collection of IAM Users.

Permissions assigned to the group are automatically inherited by all users within the group.

---

## IAM Policy

An IAM Policy is a JSON document that defines permissions.

Policies specify:

- Who can perform actions
- What actions are allowed
- Which AWS resources are affected

---

## Authentication

Authentication verifies the identity of a user before granting access.

Examples:

- Username
- Password
- MFA

---

## Authorization

Authorization determines what actions an authenticated user is allowed to perform.

Authorization is controlled using IAM Policies.

---

## Principle of Least Privilege

Users should receive only the permissions necessary to perform their assigned tasks.

This reduces security risks.

---

## Resource Tags

Tags are key-value pairs attached to AWS resources.

They help with:

- Organization
- Cost Allocation
- Automation
- Security
- Access Control

---

## Tag-Based Access Control

Permissions can be granted based on resource tags instead of individual resource IDs.

Example:

```

Env = Development

```

Only Development resources receive access.

---

## AWS Account Alias

A custom account alias replaces the numeric AWS Account ID in the login URL.

Benefits:

- Easier sign-in
- Easier sharing
- Professional account identification

---

## IAM Policy Simulator

The IAM Policy Simulator allows administrators to test permissions without affecting live AWS resources.

It is commonly used to:

- Troubleshoot permission issues
- Validate policies
- Improve security

---

# 💼 Skills Demonstrated

- AWS IAM Administration
- Amazon EC2 Management
- IAM User Management
- IAM Group Management
- JSON Policy Creation
- IAM Policy Simulator
- AWS Security
- Authentication
- Authorization
- Principle of Least Privilege
- Tag-Based Access Control
- Cloud Identity Management
- Access Management

---

# 📄 Project Documentation

Complete project documentation is available on NextWork.

https://learn.nextwork.org/confident_maroon_kind_tapir/docs/aws-security-iam

---

# 🎯 Project Outcome

Successfully implemented secure access control using AWS IAM by creating IAM users, groups, and JSON policies. Restricted access to production resources while allowing authorized access to development resources through tag-based permissions. Validated the implementation using the IAM Policy Simulator and reinforced cloud security best practices such as least privilege and identity-based access control.

---

# 🧠 What I Learned

After completing this project, I gained practical experience in:

- AWS Identity and Access Management (IAM)
- Amazon EC2 Security
- JSON Policy Writing
- IAM Users and Groups
- IAM Policies
- AWS Authentication
- AWS Authorization
- Tag-Based Access Control
- AWS Account Alias
- IAM Policy Simulator
- Least Privilege Security Model
- Enterprise Access Management
- Cloud Security Best Practices
