# AWS-cloud-first-steps
AWS Cloud Computing Essentials – EC2, Availability Zones &amp; High Availability
# ☁️ AWS Cloud First Steps

## Deploying EC2 Across Multiple Availability Zones

This repository contains study notes and assignment documentation for **AWS Cloud Computing Essentials**, focusing on deploying Amazon EC2 instances across multiple Availability Zones for high availability.

---

## 🎯 Learning Objective
Launch two Amazon EC2 instances in **two different Availability Zones (AZs)** within the same AWS Region.

---

## 🌍 Problem & Solution Overview

### ❌ Problem
- On-premises infrastructure introduces:
  - Single point of failure
  - Limited scalability
  - Hardware dependency

### ✅ Solution
- Migrate the stabilisation system’s computational module to the **AWS Global Infrastructure**
- Deploy EC2 instances across **multiple Availability Zones** within one AWS Region

---

## 🏗️ AWS Global Infrastructure

### AWS Region
- A **geographical cluster of data centres**
- Example: **US East (us-east-1)**
- Contains **three or more Availability Zones**
- Provides **99.99% service level agreement (SLA)**

### Availability Zones (AZs)
- Physically isolated data centres
- Independent:
  - Power
  - Networking
  - Connectivity
- Identified using region codes (e.g. `us-east-1a`, `us-east-1b`)

---

## 🖥️ Amazon EC2 (Compute Layer)

- Amazon EC2 provides **resizable compute capacity**
- Used to host the stabilisation system’s computational module
- Two EC2 instances are deployed:
  - Same Region
  - Different Availability Zones

### Benefit
- Improved **fault tolerance**
- Higher **availability**

---

## 💾 Amazon EBS (Storage Layer)

- Amazon Elastic Block Store (EBS) provides:
  - Persistent block storage
  - High performance
  - Optimised for EC2

- Each EC2 instance has an **EBS volume attached**
- EBS volumes are **Availability Zone–specific**

---

## 🌐 Accessing the Module

Each EC2 instance is accessible via:
- **Public IP address** (e.g. `192.168.2.1`)
- **Public DNS name** (e.g. `example.com`)

---

## 📈 High Availability Architecture

Running EC2 instances in separate Availability Zones ensures:
- No single point of failure
- Continuous operation if one AZ becomes unavailable

### Architecture Overview

AWS Region (us-east-1)
│
├── AZ us-east-1a
│ └── EC2 Instance + EBS
│
└── AZ us-east-1b
└── EC2 Instance + EBS


---

## 🧠 Key Takeaways
- Regions contain multiple AZs
- AZs are isolated and fault-tolerant
- EC2 provides scalable compute power
- EBS provides persistent storage
- Multi-AZ deployment improves reliability and availability

---

## 📘 Course
AWS Cloud Computing Essentials
