# Cloud Security Configuration Checklist

## Overview
The Cloud Security Configuration Checklist provides a structured approach for validating that cloud environments are configured securely in alignment with industry best practices. Proper cloud configuration reduces the risk of unauthorized access, data exposure, and service misuse. This checklist applies to AWS, Azure, GCP, or similar cloud platforms.

## Objective
The objective of this checklist is to help security, compliance, and engineering teams evaluate critical cloud configurations, strengthen baseline security, and support audit and governance activities.

## Checklist Items

### Identity and Access Management (IAM)
- MFA is enabled for all user accounts, especially for administrators.
- IAM roles are used instead of long-term access keys.
- Access permissions follow the principle of least privilege.
- Unused IAM accounts and access keys are disabled or removed.
- Privileged accounts are monitored and reviewed regularly.
- Service accounts have documented ownership and restricted access.

### Network Security
- Security groups and firewall rules allow only necessary inbound/outbound traffic.
- Default VPC networks are not used for production workloads.
- Public access to cloud resources is disabled unless explicitly required.
- Subnets are segmented based on function (public, private, restricted).
- Network ACLs and routing tables are properly configured.
- Load balancers and gateways use secure protocols (TLS).

### Data Protection
- Encryption at rest is enabled for all storage services (e.g., S3, Azure Blob).
- Encryption in transit is enforced using TLS/HTTPS.
- Sensitive data is identified and classified.
- Backup mechanisms are configured and tested regularly.
- Data retention and deletion policies are implemented.

### Logging and Monitoring
- Cloud provider logging services are enabled (e.g., CloudTrail, Azure Monitor).
- Logs are stored centrally and protected from tampering.
- Alerts are configured for suspicious or unauthorized activity.
- Audit logs track IAM actions, network changes, and resource modifications.
- Monitoring tools provide visibility into system health and security events.

### Resource Configuration and Hardening
- Instances, containers, or services use approved and hardened images.
- Unused services, ports, or instances are disabled or terminated.
- Patching procedures are applied for OS and middleware components.
- Security baselines are applied consistently across environments.

### Storage and Access Controls
- Buckets, blobs, or storage objects are not publicly accessible unless required.
- Versioning and lifecycle policies are enabled where appropriate.
- Access to storage is restricted based on least privilege.
- Sensitive buckets use additional protection layers (bucket policies, KMS keys).

### Vulnerability and Compliance Management
- Regular scans are performed using cloud-native or third-party tools.
- Misconfiguration alerts are monitored and remediated promptly.
- Compliance dashboards (CIS,
