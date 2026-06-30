# Setup Guide

## Prerequisites

Before starting the lab, ensure you have:

- AWS Account
- IAM User with Administrator Access
- Verified Email Address
- Amazon S3 Bucket
- CloudTrail Enabled

---

# Step 1 — Create an S3 Bucket

Create an S3 bucket to store CloudTrail logs.

Example:

```
cloudtrail-security-logs
```

---

# Step 2 — Configure AWS CloudTrail

1. Navigate to CloudTrail.
2. Create a new Trail.
3. Enable Multi-Region Logging.
4. Enable Management Events.
5. Select the S3 bucket created earlier.
6. Enable CloudWatch Logs integration.

---

# Step 3 — Configure CloudWatch Logs

Create a log group named:

```
CloudTrailLogs
```

Assign the required IAM role for CloudTrail to publish logs.

---

# Step 4 — Create Metric Filter

Navigate to:

CloudWatch Logs → CloudTrailLogs → Metric Filters

Create the following filter:

```json
{ $.eventName = "ConsoleLogin" }
```

Configuration:

- Filter Name: ConsoleLoginFilter
- Namespace: Security
- Metric Name: ConsoleLogin

---

# Step 5 — Create CloudWatch Alarm

Create an alarm using:

Metric:

```
ConsoleLogin
```

Threshold:

```
Greater than 0
```

Period:

```
5 Minutes
```

---

# Step 6 — Configure Amazon SNS

Create a topic:

```
SecurityAlerts
```

Subscribe an email endpoint.

Confirm the email subscription.

Associate the SNS Topic with the CloudWatch Alarm.

---

# Step 7 — Configure IAM Access Analyzer

Navigate to:

IAM → Access Analyzer

Create an analyzer.

Configuration:

- Analyzer Type: Account
- Zone of Trust: Current Account

---

# Step 8 — Validate Monitoring

Generate a Console Login event.

Verify:

- CloudTrail Event
- CloudWatch Log
- Metric Filter
- CloudWatch Alarm
- Email Notification

---

# Cleanup

To avoid unwanted AWS charges:

- Delete CloudWatch Alarm
- Delete Metric Filter
- Delete SNS Topic
- Delete CloudTrail
- Delete S3 Bucket
- Delete IAM Access Analyzer
