# Audit Findings Report

## Overview
This document summarizes the audit findings identified during the investigation of the cloud misconfiguration incident. The findings highlight breakdowns in technical controls, governance processes, and compliance with established cloud security standards.

---

# 1. Finding 01 — Excessive IAM Permissions  
**Severity:** High  
**Finding Type:** Control Failure  
**Description:**  
An IAM role attached to an EC2 instance granted overly broad S3 permissions, including `ListBucket` and `GetObject` across multiple buckets.

### Evidence:
- IAM policy document containing wildcard (`*`) actions  
- CloudTrail logs showing unauthorized access using compromised credentials  

### Impact:
Allowed the attacker to retrieve sensitive customer data.

### Required Remediation:
- Enforce least-privilege IAM role standards  
- Implement permission boundaries  
- Require approval workflow for IAM role creation/modification  

---

# 2. Finding 02 — Misconfigured S3 Bucket Policies  
**Severity:** High  
**Finding Type:** Data Protection Failure  
**Description:**  
The S3 bucket storing customer application data allowed unintended access due to permissive bucket policies and lack of Block Public Access enforcement.

### Evidence:
- Bucket policy review showing broad access  
- Lack of classification tags or automated controls  

### Impact:
Enabled unauthorized access to Highly Confidential data.

### Required Remediation:
- Apply strict resource-based policies  
- Enable Block Public Access organization-wide  
- Enforce mandatory tagging + data classification  

---

# 3. Finding 03 — Inadequate Cloud Configuration Monitoring  
**Severity:** Medium–High  
**Finding Type:** Governance Failure  
**Description:**  
The organization lacked CSPM tooling or automated checks to detect cloud misconfigurations and policy drift.

### Evidence:
- No CSPM alerts  
- No configuration baseline reports  
- IAM and S3 misconfigurations persisted for months  

### Impact:
Misconfigurations went undetected, increasing exposure window.

### Required Remediation:
- Deploy CSPM solution  
- Establish automated configuration baseline comparisons  
- Integrate configuration checks in CI/CD  

---

# 4. Finding 04 — Incomplete Logging & Monitoring  
**Severity:** Medium  
**Finding Type:** Monitoring Control Gap  
**Description:**  
Although CloudTrail was enabled, alerting was reactive rather than proactive. S3 access logs were incomplete prior to the incident.

### Evidence:
- Missing server access logs for sensitive buckets  
- No anomaly detection tuned for bucket access patterns  

### Impact:
Delayed detection and limited forensic visibility.

### Required Remediation:
- Enable detailed S3 access logs for all sensitive buckets  
- Tune GuardDuty, CloudTrail Insights alerts  
- Implement centralized monitoring dashboards  

---

# 5. Finding 05 — Lack of Cloud Governance Enforcement  
**Severity:** Medium  
**Finding Type:** Process Non-Compliance  
**Description:**  
Key cloud configuration and IAM changes were not subject to formal review or approval. Governance policies existed but were not operationalized.

### Evidence:
- IAM role created without approval ticket  
- S3 bucket created without classification or review  
- Outdated documentation in governance handbook  

### Impact:
Gaps in process enforcement contributed to misconfiguration drift.

### Required Remediation:
- Implement mandatory approval workflow for cloud resource changes  
- Conduct quarterly cloud governance audits  
- Update internal cloud governance standards  

---

# Summary of Audit Findings

| Finding | Severity | Category |
|--------|----------|----------|
| Excessive IAM Permissions | High | Access Control Failure |
| Misconfigured S3 Bucket Policies | High | Data Protection Failure |
| Lack of Configuration Monitoring | Medium–High | Governance Failure |
| Incomplete Logging & Monitoring | Medium | Monitoring Gap |
| Weak Governance Enforcement | Medium | Process Compliance |

---

## Notes
These findings will be reviewed during the next internal audit cycle. Evidence collected has been stored in the audit evidence folder and mapped to the Corrective Action Plan (CAPA).

