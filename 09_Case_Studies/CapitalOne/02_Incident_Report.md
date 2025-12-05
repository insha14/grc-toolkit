# Incident Report

## Overview
This incident report documents a cloud security breach caused by a misconfigured Amazon S3 bucket and an overly permissive IAM role associated with an EC2 instance. The attacker exploited an exposed metadata service to obtain temporary credentials and access sensitive customer records stored in S3.

## 1. Incident Identification
- **Incident ID:** INC-2025-001  
- **Date & Time Detected:** March 12, 2025 – 14:35 UTC  
- **Detected By:** Security Monitoring Dashboard (AWS CloudTrail anomaly alert)  
- **Type of Incident:** Unauthorized access / Cloud misconfiguration  
- **System or Asset Affected:** AWS S3 bucket storing customer application data  

---

## 2. Incident Description
A security analyst observed unusual S3 access logs originating from an EC2 instance that typically did not access the S3 bucket containing customer application data. Investigation revealed that the EC2 instance had an IAM role with overly broad permissions (`s3:ListBucket` and `s3:GetObject` across multiple buckets).  
The attacker accessed the EC2 metadata service, extracted temporary IAM credentials, and used them to access sensitive files in the S3 bucket.


---

## 3. Impact Assessment
- **Data Impacted:** Customer PII — names, addresses, partial credit application details  
- **Users Affected:** ~100,000 customers  
- **Business Impact:** Moderate operational impact; potential regulatory exposure  
- **Regulatory Impact:** Potential reporting obligations under PCI DSS, GLBA  
- **Severity Level:** High  

---

## 4. Timeline of Events

Timeline:

14:35 — CloudTrail logs flag unusual S3 access patterns

14:42 — Security analyst validates anomalous behavior

14:50 — IAM role investigation begins

15:10 — Team identifies role with overly permissive policies

15:22 — Temporary credentials revoked

15:40 — S3 bucket access policies corrected

16:15 — Forensic review of access logs initiated

18:00 — Incident escalated to executive leadership
---

## 5. Containment Actions
Containment Actions:

Revoked exposed IAM credentials immediately

Restricted IAM role to least-privilege permissions

Removed public access configuration from the S3 bucket

Enabled S3 Block Public Access organization-wide

Activated real-time alerts for abnormal IAM activity

---

## 6. Eradication & Recovery
Eradication Steps:

IAM role reconfigured with specific resource-level permissions

S3 bucket access policies updated and verified

Disabled public access at account and bucket level

Reviewed and cleaned up unused IAM roles, policies, and keys

Recovery Steps:

Restored secure configuration baseline for all cloud assets

Conducted a complete audit of S3 permissions across all buckets

Revalidated access logs and confirmed no further unauthorized access

---

## 7. Root Cause Analysis

Root Cause:
The IAM role attached to an EC2 instance was configured with overly broad permissions.
A misconfigured S3 bucket allowed unauthorized listing and retrieval of objects.
Lack of continuous cloud posture monitoring allowed configuration drift.

---

## 8. Corrective Actions & Preventive Measures

Corrective Actions:

Implemented least-privilege IAM policies

Enforced organization-wide S3 Block Public Access

Added automated scanning for misconfigurations using CSPM tools

Preventive Controls:

Quarterly cloud configuration audits

Mandatory IAM policy reviews during deployments

Additional logging and alerting through GuardDuty, CloudTrail, and Config

Integration of cloud misconfiguration checks in CI/CD pipeline
---

## 9. Roles & Responsibilities
- **Incident Handler:** Cloud Security Lead  
- **System Owner:** Engineering Manager  
- **GRC Reviewer:** Compliance Officer  
- **Additional Stakeholders:** CTO, Legal, Customer Experience  

---

## 10. Final Approval

Incident Handler: _____________________ Date: ___________

GRC Reviewer: __________________________ Date: ___________

Executive Approver: ____________________ Date: ___________
---

## Notes
- A follow-up risk assessment has been initiated.  
- Regulatory reporting may be required depending on the final legal review.  
- Audit logs will be retained for 12 months as evidence.
