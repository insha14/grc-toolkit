# Sample Risk Register

## Overview
This sample risk register demonstrates how common cybersecurity risks can be documented, evaluated, and tracked using the methodology defined in this toolkit. The examples below illustrate how likelihood, impact, inherent risk, controls, and residual risk come together in a practical assessment. These entries are fictional but modeled after real-world scenarios that frequently appear in audits, vendor reviews, and internal risk assessments.

## Sample Risk Entries

| Risk ID | Asset / Process | Threat Description | Vulnerability | Likelihood | Impact | Inherent Risk Rating | Existing Controls | Proposed Mitigation | Residual Risk Rating | Risk Owner | Status |
|---------|------------------|--------------------|---------------|------------|--------|-----------------------|-------------------|----------------------|-----------------------|------------|--------|
| 1 | Employee Accounts | Unauthorized access through compromised credentials | Weak password practices and no MFA | High | High | High | Password policy in place | Implement MFA and conduct awareness training | Medium | IT Security | In Progress |
| 2 | Customer Database | Data breach from SQL injection attack | Improper input validation | Medium | High | High | Firewall and basic monitoring | Implement secure coding practices and regular code reviews | Medium | Development Team | Open |
| 3 | Production Servers | Service outage due to ransomware | Unpatched system vulnerabilities | High | High | Critical | Periodic patching | Enforce monthly patch cycles and deploy endpoint protection | High | Infrastructure | In Progress |
| 4 | Cloud Storage | Unauthorized data exposure | Misconfigured access permissions | Medium | Medium | Medium | Access logs and user reviews | Implement least privilege and automated configuration scanning | Low | Cloud Engineering | Open |
| 5 | Vendor-Supplied Tools | Third-party compromise affecting internal systems | No vendor risk assessment process | Low | High | Medium | Contractual security clauses only | Conduct formal vendor assessments and require SOC 2 reports | Low | Procurement | Planned |

## Notes
- These examples reflect common risks in modern IT environments.  
- Residual risk levels depend on the effectiveness of proposed actions.  
- Risk owners should revisit entries regularly to update status and progress.  
- Additional examples may be added as the toolkit expands to cover more scenarios.
