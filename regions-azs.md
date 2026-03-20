# Region and Availability Zones for KijaniKiosk

## Overview

This document explains the region selection and multi-Availability Zone (AZ) strategy for the KijaniKiosk platform.

The goal is to ensure **high availability, reliability, and low latency** for users while designing for failure and resilience.

---

##  Region Selection

A **region** is a geographical location where cloud resources are deployed.

Since the target users and development context are based in **Kenya**, the closest available region would be selected to minimize latency and improve performance.

### Cloud Provider Region Choice

If using major cloud providers:

- **AWS (Amazon Web Services)**  
  - Preferred region: **South Africa**  

- **Google Cloud Platform (GCP)**  
  - Preferred region: **Johannesburg, South Africa**

- **Microsoft Azure**  
  - Preferred region: **South Africa West (Johannesburg)**  

### Why This Region?

- Geographically closest major cloud region to Kenya  
- Reduced network latency  
- Faster response times for users  
- Improved user experience  
- Better performance compared to distant regions (e.g. Europe or US)

---

##  Availability Zones (AZs)

Availability Zones are **physically separate data centers within a region**.

Each AZ has:
- Independent power supply  
- Independent networking  
- Independent cooling systems  

---

##  Multi-AZ Architecture

KijaniKiosk is designed to run across **multiple Availability Zones** within the selected region.

### How it works:

- Application is deployed in at least **two AZs**
- A load balancer distributes traffic across AZs
- If one AZ fails, traffic is automatically routed to another

---

##  Benefits of Multi-AZ Design

### 1. High Availability
- Ensures the system remains accessible even if one AZ fails

### 2. Fault Tolerance
- Isolates failures to a single AZ without affecting the entire system

### 3. Disaster Recovery
- Provides automatic failover in case of infrastructure issues

### 4. Improved Reliability
- Reduces downtime and improves user trust

---

##  Failure Scenario Example

If **Availability Zone 1 (AZ1)** goes down:

- Traffic is automatically redirected to **Availability Zone 2 (AZ2)**
- Users experience minimal or no disruption
- System continues operating normally

---

##  Design Summary

| Component            | Design Choice                                         |
|---------------------|------------------------------------------------------|
| Region              | Closest region to Kenya (South Africa)               |
| Availability Zones   | Multiple AZs within the region                       |
| Deployment          | Distributed across AZs                               |
| Failover Strategy   | Automatic failover via load balancer                |

---

##  Conclusion

The combination of a well-chosen region and multi-AZ architecture ensures:

- High availability  
- Fault tolerance  
- Low latency  
- Improved reliability  

By selecting a region close to Kenya (such as South Africa), the system achieves better performance and user experience.

---

##  DevOps Alignment

- **Flow**: Continuous deployment across zones  
- **Feedback**: Monitoring and failover mechanisms  
- **Learning**: Understanding distributed system resilience  