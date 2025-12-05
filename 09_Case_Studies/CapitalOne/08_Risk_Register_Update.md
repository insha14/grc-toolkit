# Updated Risk Register Entry

## Overview
This document captures the new and modified risks added to the organization's Risk Register following the cloud misconfiguration incident. It reflects updated risk scoring, ownership assignments, and planned treatments.

---

# 1. New Risk Entry: Cloud Misconfiguration Leading to Data Exposure

**Risk ID:** RSK-2025-004  
**Category:** Cloud Security / Access Control  
**Description:**  
Unauthorized access to sensitive data may occur due to misconfigured IAM roles, S3 bucket policies, or insufficient monitoring of cloud resources.

### **Risk Factors**
- Excessive IAM permissions  
- Public or overly permissive S3 policies  
- Misconfigured EC2 metadata service  
- Lack of continuous configuration monitoring  

---

# 2. Risk Scoring

| Factor | Rating | Notes |
|--------|---------|--------|
| **Likelihood** | Medium–High | Misconfigurations can occur frequently without CSPM and strict governance |
| **Impact** | High | Exposure of Highly Confidential customer data |
| **Inherent Risk Score** | High | Due to cloud scale, sensitive data, and ease of misconfigurations |
| **Residual Risk Score** | Medium | After applying CAPA controls |

---

# 3. Risk Treatment

**Treatment Strategy:**  
Mitigate through technical controls, continuous monitoring, and governance enhancements.

### **Mitigation Actions**
- Implement CSPM tool for continuous scanning  
- Migrate all EC2 instances to IMDSv2  
- Enforce least-privilege IAM permissions  
- Apply S3 Block Public Access organization-wide  
- Require mandatory approval workflow for IAM/S3 changes  
- Conduct quarterly cloud configuration audits  

---

# 4. Risk Owner & Stakeholders

- **Primary Owner:** Cloud Security Lead  
- **Supporting Stakeholders:**  
  - Engineering Manager  
  - DevSecOps Team  
  - GRC Officer  
  - CTO (executive oversight)  

---

# 5. Control Mapping

| Control Area | Relevant Controls |
|--------------|------------------|
| **IAM Governance** | Least privilege, permissions boundaries, role review workflow |
| **Data Protection** | S3 Block Public Access, encryption policies, classification tagging |
| **Monitoring** | CloudTrail, GuardDuty, CSPM alerts |
| **Configuration Management** | Baseline templates, automated CI/CD misconfig checks |

---

# 6. Evidence Collected

- Updated IAM role policies  
- Revised S3 bucket access configurations  
- Audit logs confirming credential revocation  
- CSPM baseline report (post-deployment)  
- Updated cloud governance workflow  

---

# 7. Next Review Date

**Scheduled Review:** 90 days from incident closure  
**Reviewer:** GRC Officer  
**Purpose:** Validate the effectiveness of remediation and ensure no drift has reoccurred.

---

## Notes
This risk entry will be included in quarterly risk committee meetings and referenced in internal audit findings.
