# EC2 Instance Types Basics

This section covers EC2 instance types, how AWS names them, and when to use each type. Understanding instance types helps me choose the right balance of CPU, memory, and storage for different workloads.

---

## Why EC2 Instance Types Matter
Not all EC2 instances are the same.

Different workloads require different resources:
- Some need more CPU
- Some need more memory (RAM)
- Some need fast local storage

Choosing the correct instance type:
- Improves performance
- Reduces cost
- Prevents over-provisioning

---

## AWS EC2 Instance Naming Convention
AWS uses a standard naming format for EC2 instances.

Example:
m5.2xlarge

Breakdown:
- m → Instance class (general purpose)
- 5 → Generation (higher = newer hardware)
- 2xlarge → Size (amount of CPU and memory)

Size generally increases in this order:
small → medium → large → xlarge → 2xlarge → 4xlarge → larger sizes

Bigger size = more vCPUs and more memory.

---

## Main EC2 Instance Categories

---

## 1) General Purpose Instances
Balanced instances suitable for a wide variety of workloads.

Best for:
- Web servers
- Application servers
- Code repositories
- Development environments

Characteristics:
- Balanced CPU, memory, and networking
- Most commonly used instance type

Example:
- t3.micro (Free Tier eligible, used in this course)

Rule of thumb:
If I am unsure which instance to choose, start with General Purpose.

---

## 2) Compute Optimized Instances
Designed for CPU-intensive workloads.

Identified by:
- C series (C5, C6, etc.)

Best for:
- Batch data processing
- Media transcoding
- High-performance web servers
- High performance computing (HPC)
- Machine learning
- Dedicated gaming servers

Key trait:
- High CPU power relative to memory

Rule of thumb:
Lots of calculations = Compute Optimized.

---

## 3) Memory Optimized Instances
Designed for workloads that require large amounts of RAM.

Identified by:
- R series
- Other families include X1, High Memory, and Z1

Best for:
- Relational databases
- NoSQL databases
- In-memory caches (Redis, ElastiCache)
- Business intelligence applications
- Real-time big data processing

Key trait:
- Very large memory capacity

Rule of thumb:
Large datasets held in memory = Memory Optimized.

---

## 4) Storage Optimized Instances
Designed for fast access to large amounts of local storage.

Identified by:
- I series
- D series
- H1 series

Best for:
- High-frequency OLTP systems
- Data warehousing
- NoSQL databases
- Distributed file systems
- In-memory caches like Redis

Key trait:
- High IOPS and fast local disk access

Rule of thumb:
Heavy disk usage = Storage Optimized.

---

## Comparing Instance Types (Examples)

Instance: t3.micro  
- 1 vCPU  
- 1 GB memory  
- Focus: Free Tier and learning

Instance: r5.16xlarge  
- 16 vCPUs  
- 512 GB memory  
- Focus: Memory-heavy workloads

Instance: c5d.4xlarge  
- 16 vCPUs  
- 32 GB memory  
- Focus: CPU-heavy workloads

Key idea:
Instances with the same number of vCPUs can have very different memory and performance profiles.

---

## Useful Resource for Comparing Instances
ec2instances.info

This site allows me to:
- View all EC2 instance types
- Compare vCPUs, memory, pricing, and performance
- Sort and search by instance name

This is very useful when selecting an instance for real projects.

---

## Big Picture Takeaway
EC2 instance types allow me to:
- Match resources to workload needs
- Optimize performance
- Control costs effectively

---

## Key Takeaways
- EC2 instances are optimized for different workloads
- Instance names show class, generation, and size
- General purpose instances are balanced and flexible
- Compute optimized instances focus on CPU
- Memory optimized instances focus on RAM
- Storage optimized instances focus on disk performance
- ec2instances.info is a great tool for comparison
