# AWS CLI, CloudShell, and SDK – Notes (Beginner)

## 🧭 How users can access AWS
There are **three main ways** to access AWS services:

1) **AWS Management Console**
- Web-based GUI (browser)
- Protected by **password + MFA**

2) **AWS Command Line Interface (CLI)**
- Run AWS commands from a terminal (Command Prompt / PowerShell / Terminal)
- Protected by **access keys**

3) **AWS Software Development Kit (SDK)**
- Used inside application code (Python, JavaScript, etc.)
- Protected by **access keys** (or IAM roles in real-world setups)

---

## 🔑 Access Keys (Important)
Access keys are generated through the AWS Console.  
Users can manage their own access keys.

**Access keys are SECRET (like a password). Don’t share them.**

- **Access Key ID** ≈ username  
- **Secret Access Key** ≈ password  

✅ Best practice: never post keys in GitHub, screenshots, or notes.

---

## ⌨️ AWS CLI (Command Line Interface)
The **AWS CLI** is a tool that lets you interact with AWS services using commands in your command-line shell.

Simple definition:
- **CLI = typing commands instead of clicking buttons**

Car dealership analogy 🚘
- **Console** = walking around the dealership and talking to people  
- **CLI** = calling the inventory manager and saying:  
  “List all the cars in inventory.”

### “Direct access to the public APIs of AWS services” (what that means)
When you run CLI commands, you are sending requests **directly to AWS service APIs** (instead of clicking in the console).

### Why CLI matters
- You can develop scripts to manage resources
- Faster and more repeatable than clicking around
- Alternative to using the AWS Management Console
- AWS CLI is open-source: https://github.com/aws/aws-cli

---

## 🧩 AWS SDK (Software Development Kit)
The **AWS SDK** is a set of language-specific libraries that lets your application access AWS programmatically.

- Embedded within your application
- Supports many environments:

**SDKs:** JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++  
**Mobile SDKs:** Android, iOS  
**IoT SDKs:** Embedded C, Arduino

---

## ⚖️ CLI vs SDK (simple)
- **CLI** = you typing commands to AWS  
- **SDK** = your application typing commands to AWS automatically  

---

## ☁️ AWS CloudShell
**AWS CloudShell** is a browser-based terminal inside the AWS Console.

It includes:
- Command-line environment
- Pre-installed AWS CLI
- Automatic authentication
- No setup required

CloudShell is great for learning because it works immediately.

---

## 🧪 Hands-On Examples I Ran

### AWS CLI (Local – Command Prompt)

Command used:
```bash
aws iam list-users
