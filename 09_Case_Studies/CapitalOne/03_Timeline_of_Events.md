# Timeline of Events

## Overview
This document provides a clear, chronological sequence of events for the cloud misconfiguration incident. It is designed for audit review, executive reporting, and incident response analysis.

---

## Incident Timeline

| Time (UTC) | Event Description |
|------------|------------------|
| **14:35** | CloudTrail flags unusual S3 access activity originating from an EC2 instance. |
| **14:42** | Security analyst validates the anomaly and compares logs with baseline behavior. |
| **14:50** | IAM investigation begins; analysts identify an EC2 instance role with overly broad permissions. |
| **15:10** | Role policy reviewed and confirmed to include `s3:ListBucket` and `s3:GetObject` for multiple buckets. |
| **15:22** | Temporary IAM credentials associated with the EC2 instance retrieved by attacker are revoked. |
| **15:40** | S3 bucket permissions corrected; public access blocked at bucket level. |
| **16:15** | Forensic review initiated across S3 access logs, IAM logs, and instance metadata service records. |
| **17:00** | Engineering notified and asked to validate secure configuration of all related cloud services. |
| **18:00** | Incident escalated to executive leadership; preliminary impact analysis completed. |
| **20:30** | Full containment confirmed; no further unauthorized access observed. |
| **Next Day, 09:00** | Cross-functional team meeting held for root cause analysis and action planning. |

---

## Notes
- Times reflect coordinated internal logs and analyst observations.  
- All timestamps stored for audit and regulatory evidence retention.  
- This timeline is referenced in the Incident Report and Corrective Action Plan.
