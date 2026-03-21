# IAM Least Privilege Design for KijaniKiosk

## Overview

This document defines an Identity and Access Management (IAM) role for the KijaniKiosk application using the **principle of least privilege**.

The goal is to ensure that the application has only the minimum permissions required to perform its tasks, improving security and reducing risk.

---

##  Principle of Least Privilege

The **principle of least privilege** means:

> Grant only the permissions that are absolutely necessary for a user or application to perform its required function.

Any unnecessary permissions are removed to minimize potential security risks.

---

## IAM Role: KijaniKiosk Application Role

### Purpose

This IAM role is designed for the **backend application** to perform specific tasks such as:

- Reading configuration data  
- Writing application logs  
- Accessing required storage resources  

---

## Permissions Granted

The application is allowed to:

- Read objects from a specific storage location  
- Write logs to a designated storage bucket  

### Example Policy

```json id="iam02"
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowReadWriteToAppStorage",
      "Effect": "Allow",
      "Action": [
        "s3:GetObject", // -Read/download files from the bucket
        "s3:PutObject"  // -Upload/write files to the bucket
      ],
      "Resource": "arn:aws:s3:::kijaniosk-app-data/*"
    }
  ]
}
```

## Some Permisons that  are not allowed from above example 

 .Delete objects **(s3:DeleteObject)**

 .List bucket contents **(s3:ListBucket)**

 .Access other buckets