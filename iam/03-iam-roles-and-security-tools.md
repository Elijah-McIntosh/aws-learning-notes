## 🎭 IAM Roles for AWS Services

Some AWS services need permission to perform actions **on your behalf**.  
Instead of using long-term access keys, AWS uses **IAM Roles**.

### 🔑 Key Characteristics
- Not associated with a physical person
- No passwords or access keys
- Provide temporary credentials
- Designed to be assumed by AWS services

### 🧩 Common IAM Service Roles
- EC2 Instance Roles
- Lambda Execution Roles
- CloudFormation Roles

---

## 🧪 Hands-On: EC2 IAM Role

### ✅ What Was Completed
- Created an IAM Role for EC2
- Attached a permission policy to the role
- Assigned the role to an EC2 instance

### 🧠 Key Takeaways
- EC2 can securely access AWS services
- No access keys stored on the instance
- Follows AWS security best practices

> **Note:** EC2 configuration details will be covered in the next study section.

---

## 🔍 IAM Security & Audit Tools

AWS provides built-in tools to help review permissions and enforce the  
**least privilege principle**.

---

## 📄 IAM Credentials Report (Account-Level)

### 📌 What It Is
A downloadable report that lists all IAM users and the status of their credentials.

### 📊 Information Included
- Password enabled or disabled
- Access keys active or inactive
- MFA enabled or not
- Credential usage status

### 🧪 Hands-On Summary
- Generated an IAM Credentials Report
- Reviewed user security posture
- Identified unused or potentially risky credentials

---

## 🧭 IAM Access Advisor (User-Level)

### 👀 What It Shows
- AWS services a user has permissions for
- When each service was last accessed

### 🎯 Why It Matters
- Helps identify unused permissions
- Supports enforcing least privilege
- Assists with policy cleanup and security reviews

### 🧪 Hands-On Summary
- Reviewed Access Advisor for an IAM user
- Checked service access history
- Evaluated which permissions were necessary

---

## 🔐 Shared Responsibility Model (IAM)

### ☁️ AWS Responsibilities
- Global infrastructure security
- Configuration and vulnerability analysis
- Compliance validation

### 👤 Customer Responsibilities
- Manage users, groups, roles, and policies
- Enable MFA on all accounts
- Rotate access keys regularly
- Audit permissions using IAM tools
- Analyze access patterns

---

## ✅ IAM Best Practices

- Do not use the root account for daily work
- Use roles for AWS services instead of access keys
- Enforce MFA for all users
- Follow the least privilege principle
- Regularly audit permissions
- Never share IAM users or access keys

---

## 🧾 IAM Section Summary

- Roles provide temporary permissions to AWS services
- EC2 roles allow instances to access AWS securely
- Credentials Report audits account-level security
- Access Advisor identifies unused permissions
- IAM security is a shared responsibility
