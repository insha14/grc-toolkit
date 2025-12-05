# Access Review Checklist

## Overview
Access reviews are a key control used to ensure that users have appropriate access to systems and data based on their job responsibilities. Regular reviews help identify excessive privileges, inactive accounts, and unauthorized access, all of which pose security and compliance risks. This checklist provides a structured way to assess whether access rights are being granted, reviewed, and removed in accordance with organizational policies.

## Purpose of Access Reviews
The purpose of an access review is to validate that access permissions are aligned with the principle of least privilege. This includes confirming that users only have the permissions necessary to perform their duties and that no unauthorized or outdated access rights remain in place. Access reviews support compliance requirements and help reduce the likelihood of data breaches caused by insider threats, account misuse, or configuration errors.

## Access Review Checklist Template

### User Access Review

| Review Step | Description | Evidence Examples | Status |
|-------------|-------------|-------------------|--------|
| Identify User Population | Obtain a complete list of active users for the system. | User export from IAM or system admin panel | |
| Validate Active Users | Verify that all users are still employed or still require access. | HR roster, employment status reports | |
| Review Role Appropriateness | Confirm user roles align with job responsibilities. | Org charts, job descriptions | |
| Identify Excessive Privileges | Look for admin or elevated access where not required. | Privilege reports, logs | |
| Remove Unnecessary Access | Disable or modify access for users who no longer require it. | Ticketing system records | |
| Review Service Accounts | Validate ownership and purpose of service or shared accounts. | Account documentation | |
| Check Dormant Accounts | Identify accounts with no recent activity. | Login activity logs | |
| Document Reviewer Approval | Capture reviewer sign-off and any required remediation actions. | Approval workflow, sign-off forms | |

### Privileged Access Review

| Review Step | Description | Evidence Examples | Status |
|-------------|-------------|-------------------|--------|
| Identify Privileged Accounts | List all accounts with administrative or elevated permissions. | Admin export from system | |
| Validate Need for Privilege | Confirm privileged access is required for job duties. | Manager approvals | |
| Check MFA Enforcement | Ensure multi-factor authentication is enforced for privileged accounts. | IAM policy, system logs | |
| Review Privileged Activity | Monitor logs for unusual or unauthorized admin actions. | SIEM alerts, activity reports | |
| Validate Password Security | Confirm privileged accounts follow strong password requirements. | Password policy screens, audit logs | |

## Role in This Toolkit
This checklist serves as a foundational tool for performing access-related audits and assessments. It prepares you to participate in internal audits, SOC 2 readiness projects, and access governance activities. Future additions to this toolkit may include sample access review procedures, workflows, and remediation examples to deepen practical understanding.
