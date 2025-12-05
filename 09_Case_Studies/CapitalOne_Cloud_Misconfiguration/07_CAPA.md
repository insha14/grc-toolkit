# Corrective Action Plan (CAPA)

## Overview
This Corrective Action Plan outlines the actions required to prevent recurrence of the cloud misconfiguration incident. It includes immediate remediation steps, long-term preventive measures, control enhancements, and assigned responsibilities.

---

# 1. Immediate Corrective Actions (Completed)

| Action | Description | Owner | Status |
|--------|-------------|--------|--------|
| Revoke compromised IAM credentials | Disabled all temporary credentials associated with the EC2 instance | Cloud Security | Completed |
| Restrict IAM role permissions | Updated IAM role to least-privilege and removed wildcard permissions | Engineering | Completed |
| Correct S3 bucket access policies | Disabled broad access, applied least-privilege bucket policies | Cloud Engineering | Completed |
| Block public access org-wide | Enabled S3 Block Public Access across all AWS accounts | Cloud Security | Completed |
| Enable detailed S3 access logs | Activated server access logs for sensitive buckets | CloudOps | Completed |

---

# 2. Short-Term Preventive Actions (0–30 Days)

| Action | Description | Owner | Due Date | Status |
|--------|-------------|--------|----------|--------|
| Deploy CSPM tool | Implement CSPM solution (e.g., Prisma, Wiz, or AWS Config rules) for continuous monitoring | Security | 30 Days | Planned |
| Review IAM roles across all environments | Audit all roles for least-privilege alignment | Cloud Security | 21 Days | In Progress |
| Enforce metadata protection | Migrate all EC2 instances to IMDSv2 | Engineering | 14 Days | In Progress |
| Establish change approval workflow | Require formal approval for creation/modification of IAM roles and S3 bucket policies | GRC + DevOps | 30 Days | Planned |
| Implement tagging standards | Enforce mandatory data classification tags on all S3 buckets | Cloud Governance | 30 Days | Planned |

---

# 3. Long-Term Preventive Controls (30–90 Days)

| Control Enhancement | Description | Owner | Target |
|---------------------|-------------|--------|----------------|
| Implement IAM permission boundaries | Prevent use of overly broad policies at the account level | Security Architecture | 90 Days |
| Integrate cloud validation into CI/CD | Add automated static checks for IAM/S3 misconfigurations in pipelines | DevSecOps | 75 Days |
| Quarterly cloud configuration audits | Institutionalize periodic audits of IAM, S3, EC2 metadata, logging | GRC | Ongoing |
| Deploy anomaly detection alerts | Enable GuardDuty and CloudTrail Insights org-wide | Security Operations | 60 Days |
| Implement centralized security baseline templates | Standardize IAM/S3/EC2 configurations | Cloud Architecture | 90 Days |

---

# 4. Accountability & Ownership

Primary Drive: Cloud Security Lead
Supporting Teams: Engineering, DevOps, GRC, Legal, Operations
Executive Oversight: CTO / CISO
Review Cadence: Weekly updates during remediation, monthly thereafter
---

# 5. Success Criteria

A successful corrective action plan is defined by:

- No IAM roles containing wildcard permissions  
- No S3 buckets with public or overly permissive access  
- CSPM tool actively monitoring all cloud resources  
- Automated alerts enabled for IAM, S3, metadata anomalies  
- Quarterly cloud reviews conducted and documented  
- Evidence of updated governance workflows and approval processes  

---

# 6. Verification and Closure Plan

| Verification Step | Description | Owner | Status |
|-------------------|-------------|--------|---------|
| Validate least privilege for all IAM roles | Confirm through audit and CSPM | GRC | Pending |
| Verify S3 access policies | Ensure all sensitive buckets meet confidentiality requirements | Cloud Engineering | Pending |
| Review CSPM alerts and baseline | Establish new baseline and alert tuning | Security | Pending |
| Document updated workflows | Updated cloud governance and IAM change processes | GRC | Pending |

---

## Notes
The CAPA will be reviewed during internal audit and by executive leadership during the post-incident governance review.
