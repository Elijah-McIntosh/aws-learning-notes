# Cloud Basics + AWS Console

## Traditional IT

### How Websites Work

--


For the client and server to find each other, both must have **IP addresses**.

### What is a Server Composed Of?
- **Compute (CPU):** Performs calculations and processing  
- **Memory (RAM):** Stores information temporarily for fast access  
- **Storage:** Holds files and data long-term  
- **Database:** Stores data in a structured way for quick retrieval  
- **Network:** Routers, switches, DNS servers  

---

## IT Terminology

### Network
Cables, routers, switches, and servers connected to each other.

### Router
A networking device that forwards **data packets** between computer networks.  
Knows where to send packets across the internet.

### Switch
Receives a packet and sends it to the correct server/client within a network.

---

# Cloud Computing

Cloud computing is the **on-demand delivery** of:

- Compute power  
- Database storage  
- Applications  
- Other IT resources  

…through a cloud services platform with **pay-as-you-go pricing**.

You can:

- Provision exactly the right type & size of computing resources  
- Access as many resources as needed almost instantly  
- Get servers, storage, databases, and more through a web console  

**AWS owns and maintains** the hardware.  
**You provision and use** what you need.

---

# Deployment Models of the Cloud

## Private Cloud
- Cloud services used by **one organization**
- Not exposed to the public
- Full control
- Great for sensitive applications
- Meets specific business needs

## Public Cloud
- Cloud resources owned and operated by **third-party providers**
- Delivered over the internet

## Hybrid Cloud
- Some servers **on-premises**
- Some resources in the cloud  
- Best for:
  - Sensitive private infrastructure  
  - Flexibility + cost effectiveness  

---

# The Five Characteristics of Cloud Computing

### 1. On-Demand Self-Service
Provision resources without human interaction.

### 2. Broad Network Access
Resources available over a network for multiple platforms.

### 3. Multi-Tenancy & Resource Pooling
Multiple customers share infrastructure securely.

### 4. Rapid Elasticity & Scalability
Quickly scale resources in/out with demand.

### 5. Measured Service
Usage is metered; you pay only for what you use.

---

# Six Advantages of Cloud Computing

- Trade **CAPEX → OPEX**  
- Pay only for what you use  
- Reduced TCO & operational costs  
- Massive economies of scale  
- No more guessing capacity  
- Increase speed and agility  
- Stop running data centers  
- Go global in minutes  

---

# Problems Solved by the Cloud

- **Flexibility:** Change resource types as needed  
- **Cost-effectiveness:** Pay as you go  
- **Scalability:** Handle larger loads  
- **Elasticity:** Scale automatically  
- **High availability & fault tolerance:** Build across AZs  
- **Agility:** Launch applications faster  

---

# Types of Cloud Computing

## Infrastructure as a Service (IaaS)
- Building blocks of cloud IT  
- Networking, computers, storage  
- Most flexible  
- Similar to traditional IT

## Platform as a Service (PaaS)
- No need to manage servers  
- Focus on deployment & management  
- Great for developers

## Software as a Service (SaaS)
- Completed product run by a provider  
- Users simply consume the application  

---

# Pricing of the Cloud (Quick Overview)

- Compute → pay for compute time  
- Storage → pay for stored data  
- **Data transfer OUT** → usually charged  
- **Data transfer IN** → typically free  

Cloud solves the **expensive hardware** problem of traditional IT.

---

# AWS Global Infrastructure

AWS consists of:

- **Regions**
- **Availability Zones (AZs)**
- **Data Centers**
- **Edge Locations / Points of Presence**

---

## AWS Regions

A **region** = a cluster of data centers.  
AWS has many regions globally.

Most AWS services are **region-scoped**.

### How to choose a region:
- Compliance & legal requirements  
- Data sovereignty  
- Proximity to customers  
- Available services  
- Pricing differences  

---

## AWS Availability Zones (AZs)

- Each region has **3–6 AZs**
- Each AZ = one or more **discrete data centers**
- Redundant power, networking, connectivity  
- AZs are isolated from disasters  
- Connected with **high-bandwidth, low-latency** links  

---

## AWS Data Centers
Secure buildings within AZs that host AWS hardware.

They are the **physical home of the cloud**.

---

## AWS Edge Locations / Points of Presence
- 400+ global sites  
- In 90+ cities, 40+ countries  
- Used to deliver content closer to users  
- Reduce latency and improve speed  

---

# Tour of the AWS Console

### Global Services
- IAM  
- Route 53  
- CloudFront  
- WAF  

### Region-Scoped Services
- Amazon EC2 (IaaS)  
- Elastic Beanstalk (PaaS)  
- Lambda (FaaS)  
- Rekognition (SaaS)  

---

# Shared Responsibility Model

### YOU are responsible for **security IN the cloud**
- Data  
- User settings  
- Passwords  
- Encryption  
- Configurations  

### AWS is responsible for **security OF the cloud**
- Physical data centers  
- Hardware  
- Networking  
- Infrastructure  

---

# AWS Acceptable Use Policy
You must NOT use AWS for:

- Illegal or harmful content  
- Security violations  
- Network abuse  
- Email/messaging abuse  
