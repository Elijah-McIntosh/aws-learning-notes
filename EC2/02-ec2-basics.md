EC2 Basics (Introduction)

In this EC2 module, we begin by creating our first website on AWS. This section introduces the core concepts of Amazon EC2 and explains why it is foundational to cloud computing.

---

## What Is Amazon EC2?
Amazon EC2 stands for Elastic Compute Cloud.

- One of the most widely used AWS services
- Provides Infrastructure as a Service (IaaS)
- Allows you to rent virtual servers (compute) on demand

Instead of buying physical hardware, you launch and pay for virtual machines only when you need them.

---

## Why EC2 Matters
EC2 is fundamental to understanding AWS because the cloud is about:
- Renting compute resources on demand
- Scaling resources up or down easily
- Paying only for what you use

If you understand EC2, you understand the core idea of cloud infrastructure.

---

## EC2 Components
EC2 is not just a single service. It is made up of multiple components that work together.

- EC2 Instances – Virtual machines (servers)
- EBS Volumes – Virtual storage disks
- Elastic Load Balancer (ELB) – Distributes traffic across instances
- Auto Scaling Group (ASG) – Automatically scales instances based on demand

High-Level Architecture (Conceptual):

                Elastic Load Balancer (ELB)
                           |
           ---------------------------------------
           |                 |                 |
      EC2 Instance       EC2 Instance       EC2 Instance
           |                 |                 |
         EBS               EBS               EBS

---

## Instance Options — What You Can Choose
When launching an EC2 instance, you choose how the virtual server is configured.

Key configuration choices include:

Operating System
- Linux (most common)
- Windows
- macOS

Compute
- CPU
- Number of cores

Memory
- RAM size

Storage
- Network-attached storage (EBS or EFS)
- Hardware-attached storage (Instance Store)

Networking
- Network performance
- Public or private IP options

Security
- Firewall rules managed by Security Groups

Bootstrapping
- Automated setup using EC2 User Data

Configuration Overview:

EC2 Configuration
|
|-- Operating System
|-- CPU and Cores
|-- RAM
|-- Storage (EBS / EFS / Instance Store)
|-- Networking
|-- Security Groups
|-- User Data

---

## Security Groups (Firewall Concept)
Security Groups control what traffic is allowed in and out of an EC2 instance.

Conceptual Flow:

Internet
   |
[ Security Group ]
   |
EC2 Instance

- Acts as a virtual firewall
- Controls inbound and outbound rules
- Common ports: SSH (22), HTTP (80), HTTPS (443)

---

## Bootstrapping with EC2 User Data
EC2 User Data is a script that runs only once when the instance launches for the first time.

Bootstrapping means automatically running setup commands at startup.

Common User Data tasks:
- Installing updates and software
- Downloading files
- Running application setup commands

Important notes:
- Runs one time at first boot
- Executes as the root user
- Has full sudo permissions
- Larger scripts increase startup time

Bootstrapping Flow:

Launch EC2
   |
User Data runs (one time)
   |
Instance ready for use

---

## Key Takeaways
- EC2 stands for Elastic Compute Cloud
- EC2 provides Infrastructure as a Service (IaaS)
- EC2 consists of instances, storage, load balancing, and auto scaling
- You control OS, compute, memory, storage, networking, and security
- EC2 User Data automates first-boot setup and runs as root
