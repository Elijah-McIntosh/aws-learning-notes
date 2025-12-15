# IAM Basics – Users, Groups, Policies & Permissions

## IAM Overview
**IAM = Identity and Access Management**  
It is a **GLOBAL service**, not tied to any AWS region.

IAM controls:
- Who can access your AWS account  
- What actions they can perform  

---

## Root Account
The **root account** is created by default when the AWS account is created.

### Root should NOT:
- Be used for daily tasks  
- Be shared with anyone  

### Why?  
Root has **full, unrestricted access** — like the owner of a dealership:

- Can fire everyone  
- Shut the place down  
- Change prices  
- Revoke access  

This is why we create **users**, **groups**, and **roles** instead of giving root access.

---

## IAM Users
Users are **people** in your organization who need access to AWS.

Properties:
- Each user has their own credentials  
- Users can be assigned permissions  
- Users **do not** have to belong to a group  
- Users **can** belong to multiple groups  

---

## IAM Groups
Groups are **collections of users** that share the same permissions.

Rules:
- Groups contain **only users**, not other groups  
- You cannot nest a group inside another group  
- Applying permissions to a group applies them to all users in it  

---

# IAM Permissions & Policies

Users or groups are assigned **JSON documents** called **policies**.  
Policies define the **permissions** of the user or group.

### Least Privilege Principle
Always give the **minimum permissions** necessary for a user to do their job.

> Don’t give users more access than they need.

---

# IAM Policy Structure

A policy consists of:

### **Top-Level Fields**
- **Version** – policy language version (always `"2012-10-17"`)
- **Id** – optional identifier for the policy
- **Statement** – one or more statements (REQUIRED)

---

## Statement Structure
Each statement can include:

- **Sid** – optional identifier  
- **Effect** – `"Allow"` or `"Deny"`  
- **Principal** – the user/account/role this policy applies to  
- **Action** – list of actions allowed or denied  
- **Resource** – which resources the actions apply to  
- **Condition** – optional conditions for when the policy applies  

Example actions:
- `s3:GetObject`
- `ec2:StartInstances`
- `iam:CreateUser`

---

## Example Minimal Policy Structure

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": {
        "AWS": "elijah"
      },
      "Action": [
        "s3:GetObject"
      ],
      "Resource": "arn:aws:s3:::elijahs-demo-udemy-s3-lecture/images/beach.jpg"
    }
  ]
}
