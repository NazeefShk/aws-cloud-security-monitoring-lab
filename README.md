# ☁️ AWS Cloud Security Monitoring Lab

<p align="center">

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazonaws)
![CloudTrail](https://img.shields.io/badge/AWS-CloudTrail-blue?style=for-the-badge)
![CloudWatch](https://img.shields.io/badge/AWS-CloudWatch-purple?style=for-the-badge)
![SNS](https://img.shields.io/badge/AWS-SNS-red?style=for-the-badge)
![IAM](https://img.shields.io/badge/AWS-IAM-green?style=for-the-badge)

</p>

---

## 📖 Project Overview

This project demonstrates the implementation of an end-to-end AWS cloud security monitoring solution using native AWS security and monitoring services.

The solution captures AWS Console Login events using AWS CloudTrail, forwards logs to Amazon CloudWatch Logs, detects login activity using Metric Filters, triggers CloudWatch Alarms, and sends real-time email notifications through Amazon SNS. Additionally, IAM Access Analyzer is configured to monitor resources for unintended external access.

This project simulates how organizations monitor AWS account activity and automate security alerting for critical management events.

---

## 🎯 Objectives

- Monitor AWS Console Login activity.
- Capture API events using AWS CloudTrail.
- Store logs in Amazon CloudWatch Logs.
- Detect login events using Metric Filters.
- Generate custom CloudWatch Metrics.
- Trigger CloudWatch Alarms automatically.
- Send real-time email alerts using Amazon SNS.
- Analyze external resource access using IAM Access Analyzer.
- Demonstrate an end-to-end cloud security monitoring workflow.

---

## 🏗️ Architecture

<p align="center">
<img src="architecture/architecture.png" width="1000">
</p>

---

## ⚙️ AWS Services Used

| Service | Purpose |
|----------|----------|
| AWS CloudTrail | Captures AWS API and Console Login events |
| Amazon CloudWatch Logs | Stores CloudTrail logs |
| CloudWatch Metric Filters | Detects ConsoleLogin events |
| CloudWatch Metrics | Generates custom security metrics |
| CloudWatch Alarms | Monitors security metrics |
| Amazon SNS | Sends email notifications |
| IAM Access Analyzer | Detects unintended external resource access |

---
