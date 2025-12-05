
# Asset Inventory Register

## Overview
The Asset Inventory Register provides a centralized record of all critical information assets, including hardware, software, cloud systems, and data repositories. It supports risk assessments, access management, compliance audits, and incident response.

## Purpose
This register helps the organization track asset ownership, classify data, and ensure that appropriate controls are applied based on asset sensitivity and business importance.

---

## Asset Inventory Table

| Asset ID | Asset Name | Type (Hardware/Software/Data/Cloud) | Description | Owner | Data Classification | Location | Dependencies | Notes |
|----------|------------|---------------------------------------|-------------|--------|----------------------|----------|--------------|--------|
| A-001 | Employee Laptops | Hardware | Corporate-issued laptops for staff | IT Manager | Internal | Office/Remote | MDM, Endpoint Protection | Encrypted & monitored |
| A-002 | CRM System | Software | Customer relationship management platform | Sales Lead | Confidential | Cloud (SaaS) | SSO, MFA | SOC 2 vendor |
| A-003 | Production Database | Data | Stores customer and transaction data | Engineering | Highly Confidential | Cloud (AWS RDS) | Backend Services | Backups daily |
| A-004 | Email Platform | Software | Company-wide communication system | IT Lead | Internal | Cloud (Microsoft 365) | IAM, MFA | Logs retained 90 days |

---

## Notes
- Each asset must have a clearly assigned owner.  
- Data classification should match the Data Classification Policy.  
- Update the register when new assets are added, removed, or change ownership.  
- This register supports audits, incident response, and risk assessment activities.
