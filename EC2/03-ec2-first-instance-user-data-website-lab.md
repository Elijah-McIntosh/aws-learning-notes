# EC2 Hands-On: Launch Instance with User Data Website

In this hands-on lab, I launched my first EC2 instance running Amazon Linux and used EC2 User Data to automatically deploy a simple website. I also learned how to manage the EC2 instance lifecycle (start, stop, terminate).

---

## Purpose of This Lab
- Launch an EC2 instance using the AWS Console
- Understand key EC2 launch settings
- Use EC2 User Data to bootstrap a web server
- Access a website hosted on EC2
- Learn how instance states affect access and cost

---

## High-Level Overview
What I did in this lab:
- Created an EC2 instance using Amazon Linux 2
- Used a Free Tier eligible instance type (t2.micro)
- Configured networking and security groups
- Used User Data to install and start a web server
- Accessed the site using the public IPv4 address
- Practiced stopping, starting, and terminating the instance

---

## Step 1: Launching the EC2 Instance
- Opened the EC2 Console
- Clicked Instances
- Clicked Launch instances

---

## Step 2: Name and Tags
- Name tag: My First Instance
- The Name tag is sufficient for identification
- Additional tags are optional

---

## Step 3: Choose an AMI (Operating System)
- Selected Amazon Linux 2023 kernel-6.1 AMI
- Chosen from Quick Start options
- Architecture: 64-bit x86
- AWS-provided and Free Tier eligible

---

## Step 4: Choose Instance Type
- Selected t3.micro
- Free Tier eligible
- Controls CPU, memory, and cost

Note: If t2.micro is unavailable, AWS may use t3.micro.

---

## Step 5: Create a Key Pair
A key pair is required to log into the instance using SSH.

- Created a new key pair named EC2 Tutorial
- Key pair type: RSA

Key pair formats:
- .pem for Mac, Linux, and Windows 10+
- .ppk for older Windows versions using PuTTY

Important notes:
- The key pair downloads only once
- Losing it means SSH access is lost

---

## Step 6: Network Settings and Security Groups
- Default network settings used
- Instance receives a public IPv4 address

Security group created: launch-wizard-1

Inbound rules:
- SSH (port 22) from anywhere
- HTTP (port 80) from anywhere

Purpose:
- SSH allows remote access
- HTTP allows web traffic to the server

HTTPS was not enabled in this lab.

---

## Step 7: Configure Storage
- Root volume: 8 GB gp3
- One volume is sufficient

Important setting:
- Delete on Termination is enabled
- Storage is deleted when the instance is terminated

---

## Step 8: EC2 User Data (Bootstrapping)
User Data is a script that runs automatically on the first launch only.

What the User Data script does:
- Updates the instance
- Installs the HTTPD web server
- Creates an HTML file
- Displays a Hello World webpage

Important notes:
- Runs only once
- Executes on first boot
- Used to automate setup
- Script was provided for learning purposes

---

## Step 9: Launch the Instance
- Reviewed all settings
- Clicked Launch instance
- Instance entered pending state for 10–15 seconds

This demonstrates how quickly cloud infrastructure can be created.

---

## Step 10: Instance Details (Running State)
Once running, the instance shows:
- Name: My First Instance
- Instance ID (unique identifier)
- Public IPv4 address (used to access the website)
- Private IPv4 address (used internally by AWS)
- Instance type: t3.micro
- AMI: Amazon Linux 2023 kernel-6.1
- Key pair: EC2 Tutorial
- Security group: launch-wizard-1
- Storage: 8 GB EBS volume

---

## Step 11: Accessing the Web Server
To access the website:
- Open a web browser
- Navigate to http://<public-ip-address>

Important notes:
- Use HTTP, not HTTPS
- HTTPS may cause infinite loading
- The page displays Hello World and the private IPv4 address

If the page does not load immediately:
- Wait a few minutes
- Refresh the page

---

## Step 12: Managing EC2 Instance States

### Stop
- Stops compute billing
- Storage remains attached
- Web server is inaccessible
- Instance can be started again

### Start
- Instance restarts
- Public IPv4 address may change
- Private IPv4 address remains the same

### Terminate
- Permanently deletes the instance
- Deletes attached storage by default
- Cannot be recovered

Always use the current public IPv4 address after restarting.

---

## Big Picture Takeaway
This lab demonstrated:
- The speed and power of cloud infrastructure
- How EC2, networking, security groups, and storage work together
- How User Data automates server setup
- How instance lifecycle actions affect cost and access

---

## Key Takeaways
- Launched an EC2 instance using Amazon Linux 2023 kernel-6.1
- Used a Free Tier eligible instance type
- Created and used a key pair for SSH access
- Configured security groups for SSH and HTTP
- Used EC2 User Data to automatically deploy a website
- Learned how start, stop, and terminate affect billing and IP addresses
