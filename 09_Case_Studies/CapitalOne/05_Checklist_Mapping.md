# Cloud Misconfiguration Checklist Mapping

## Overview
This document maps the cloud incident to specific failures and gaps identified in the Cloud Security Configuration Checklist. This demonstrates how governance controls, if properly implemented and monitored, could have prevented or reduced the severity of the incident.

---

## 1. Identity and Access Management (IAM)

| Checklist Control | Expected State | Actual State | Gap Identified |
|-------------------|----------------|--------------|----------------|
| IAM roles follow least-privilege | Roles should grant only required actions | EC2 role allowed broad S3 actions (`ListBucket`, `GetObject` for multiple buckets) | Excessive permissions; violation of least-privilege |
| MFA for privileged access | Enabled for all privileged identities | Temporary IAM credentials were obtained via metadata service | Lack of additional guardrails on metadata access |
| Regular review of IAM roles | Quarterly or monthly reviews | IAM role had not been reviewed for months | Configuration drift unnoticed |

---

## 2. Network Security

| Checklist Control | Expected State | Actual State | Gap Identified |
|-------------------|----------------|--------------|----------------|
| Access to sensitive resources restricted through network boundaries | S3 buckets restricted by VPC endpoints | Bucket accessible more broadly than intended | No network-based restriction for S3 access |
| Ingress/egress controls validated | Only approved traffic allowed | No restrictions on EC2 metadata service path | Allowed token retrieval |

---

## 3. Data Protection

| Checklist Control | Expected State | Actual State | Gap Identified |
|-------------------|----------------|--------------|----------------|
| S3 buckets containing sensitive data must **not** allow public access | Public access blocked | Bucket had permissive policy and lacked Block Public Access enforcement | Direct misconfiguration |
| Encryption at rest and in transit | Required | Encryption existed, but access misconfigurations overshadowed protection | Control existed but was insufficient for threat model |
| Data classified and tagged | Highly Confidential data must be tagged and tightly controlled | Data was stored without proper tagging or automated controls | Classification not enforced |

---

## 4. Logging and Monitoring

| Checklist Control | Expected State | Actual State | Gap Identified |
|-------------------|----------------|--------------|----------------|
| CloudTrail enabled and monitored | Enabled and actively reviewed | Alert was triggered only after unusual access | Reactive monitoring |
| S3 access logging | Required for sensitive buckets | Limited visibility; logs incomplete before event | No proactive anomaly detection |
| IAM policy drift detection | Should detect over-permissive policies | No automated alerts for policy drift | Posture monitoring missing |

---

## 5. Resource
