# Data Classification Register

## Overview
The Data Classification Register documents different types of data handled by the organization, their classification levels, storage locations, and associated controls. It supports compliance, privacy requirements, and secure data handling throughout the organization.

## Purpose
This register ensures that sensitive data is properly identified and protected. It helps security, IT, and compliance teams apply appropriate controls based on the classification level and supports audits and risk assessments.

---

## Data Classification Table

| Data ID | Data Type | Classification (Public/Internal/Confidential/Highly Confidential) | Description | Storage Location | Owner | Controls in Place | Notes |
|--------|-----------|--------------------------------------------------------------------|-------------|------------------|--------|--------------------|--------|
| D-001 | Customer PII | Highly Confidential | Names, emails, phone numbers | Production DB (AWS RDS) | Engineering | Encryption at rest/in transit, RBAC, MFA | Critical asset |
| D-002 | Employee Records | Confidential | HR & payroll-related info | HR System (SaaS) | HR Manager | Access restricted, SOC 2 vendor, MFA | Annual review |
| D-003 | Marketing Analytics | Internal | Website traffic & campaign data | Analytics Platform | Marketing Lead | Limited access, anonymized | Moderate sensitivity |
| D-004 | Public Website Data | Public | Content visible to all users | Company Website | Marketing | No restrictions | Low-risk |

---

## Notes
- Classification must follow the Data Classification Policy.  
- Update this register when new systems or data types are added.  
- Sensitive data should have documented retention and destruction requirements.  
