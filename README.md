# KijaniKiosk DevOps Foundation

## Overview

This repository contains the DevOps Starter Kit for the KijaniKiosk platform.  
It demonstrates key DevOps practices including Git workflow, cloud architecture design, security, and network segmentation.

The project was built using a **feature-based workflow** and follows best practices for collaboration and infrastructure design.

---

## DevOps Workflow

The development process followed this flow:

### Steps followed:
1. Created a feature branch for isolated development `feature/starter-kit-files`
2. Added all required documentation and architecture designs  
3. Committed and pushed changes to GitHub  
4. Created a Pull Request into `develop`  
5. Reviewed and merged changes  
6. Promoted `develop` into `main`  

This demonstrates:
- **Flow** – smooth progression of work  
- **Feedback** – via Pull Requests  
- **Learning** – through iterative development  


## Submission Checklist

✔ Repository contains `starter-kit/` folder  
✔ Feature branch used: `feature/starter-kit-files`  
✔ Develop branch created and used for integration  
✔ Main branch updated after testing  
✔ At least one Pull Request created and merged  
✔ All required documentation files completed  
✔ Network diagram shows public and private subnet architecture  
✔ IAM policy demonstrates least privilege  
✔ Region and availability zone design explained  

---
## Pull Request

This project was developed using a feature branch workflow.

All changes were first implemented in a feature branch, then reviewed and merged through a Pull Request.

Pull Request:

`https://github.com/sololemons/kijaniosk-devops-foundation/pull/1`


## ☁️ Cloud Architecture

- The system is designed using a **PaaS model**  
- Deployment is planned in the **South Africa region** (closest to Kenya)  
- Multi-Availability Zone (AZ) architecture ensures:
  - High availability  
  - Fault tolerance  
  - Disaster recovery  

---

## 🔐 Security Design

- IAM follows the **principle of least privilege**
- Users and applications are granted only the minimum permissions required
- This reduces risk and improves system security

---

## 🌐 Network Design

- The system is deployed inside a **Virtual Private Cloud (VPC)**
- Architecture includes:
  - **Public Subnet** (internet-facing)
  - **Private Subnet** (secure resources)
- Traffic flow: 
Internet → Internet Gateway → Public Subnet → Private Subnet

---

## Key Learnings

- How to use Git branches and Pull Requests effectively  
- How to design a basic cloud architecture  
- Understanding IAM and security principles  
- Designing network segmentation  
- Applying DevOps principles in a real workflow  

---

## Conclusion

This project demonstrates foundational DevOps skills required to build, secure, and deploy scalable systems.

It reflects best practices in:
- Collaboration  
- Security  
- Infrastructure design  
- Continuous improvement  

---
##  Notes on Repository Workflow

While the main development work followed the proper DevOps workflow:
feature/starter-kit-files → develop → main

The README file was initially created directly in the `main` branch during repository setup.

Future updates to the README were made through the feature branch workflow to align with DevOps best practices.


## 👨‍💻 Author

**Solomon Ndimu Ngandu**

---