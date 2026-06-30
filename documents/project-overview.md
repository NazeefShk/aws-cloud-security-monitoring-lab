# Project Overview

## Introduction

The AWS Cloud Security Monitoring Lab is a hands-on cloud security project designed to demonstrate how AWS native services can be integrated to monitor, detect, and alert on security-related events.

The project focuses on building an event-driven monitoring pipeline capable of capturing AWS API activity, detecting management console logins, generating security metrics, triggering alarms, and notifying administrators through email.

In addition to security monitoring, IAM Access Analyzer was configured to evaluate AWS resources for unintended external access.

---

## Project Objectives

The primary objectives of this project were to:

- Capture AWS API activity using AWS CloudTrail.
- Centralize CloudTrail logs in Amazon CloudWatch Logs.
- Detect AWS Console Login events using CloudWatch Metric Filters.
- Generate custom CloudWatch Metrics.
- Trigger CloudWatch Alarms automatically.
- Send real-time security alerts using Amazon SNS.
- Analyze external resource access with IAM Access Analyzer.
- Understand AWS-native security monitoring workflows.

---

## AWS Services Used

| Service | Purpose |
|----------|----------|
| AWS CloudTrail | Captures AWS API events |
| Amazon S3 | Stores CloudTrail log files |
| Amazon CloudWatch Logs | Stores CloudTrail logs |
| CloudWatch Metric Filters | Detects security events |
| CloudWatch Metrics | Creates custom security metrics |
| CloudWatch Alarms | Monitors security metrics |
| Amazon SNS | Sends email alerts |
| IAM Access Analyzer | Identifies external access risks |

---

## Monitoring Workflow

```
AWS Console Login
        │
        ▼
AWS CloudTrail
        │
        ▼
CloudWatch Logs
        │
        ▼
Metric Filter
        │
        ▼
CloudWatch Metric
        │
        ▼
CloudWatch Alarm
        │
        ▼
Amazon SNS
        │
        ▼
Email Notification
```

---

## Skills Demonstrated

- AWS Security
- Cloud Monitoring
- Security Event Detection
- CloudTrail
- CloudWatch Logs
- CloudWatch Metrics
- CloudWatch Alarms
- Amazon SNS
- IAM Access Analyzer
- Log Analysis
- Security Operations
- Incident Monitoring

---

## Conclusion

This project demonstrates practical implementation of AWS-native cloud security monitoring and event-driven alerting. It provides hands-on experience with cloud logging, automated detection, and security operations concepts commonly used in production AWS environments.
