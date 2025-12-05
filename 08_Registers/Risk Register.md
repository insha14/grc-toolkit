# Risk Register

## Overview
The Risk Register is a centralized list of identified risks, their severity, existing controls, and current status. It provides visibility for leadership, security teams, and auditors, helping track how risks evolve and how they are being managed.

## Purpose
This register supports risk assessments, compliance reviews, audits, and decision-making. It aligns with your Risk Assessment Policy and Risk Acceptance workflow.

---

## Risk Register Table

| Risk ID | Risk Title | Description | Likelihood | Impact | Inherent Risk | Existing Controls | Residual Risk | Risk Owner | Status | Notes |
|--------|------------|-------------|------------|--------|----------------|-------------------|----------------|-------------|--------|-------|
| R-001 | Unauthorized Access | Users may gain access without MFA | Medium | High | High | MFA enabled, RBAC applied | Medium | IT Manager | Open | Review MFA logs quarterly |
| R-002 | Data Loss | Accidental deletion of critical files | Low | High | Medium | Daily backups | Low | Ops Lead | Open | Backup restoration test pending |
| R-003 | Vendor Breach | Third-party vendor compromises customer data | Medium | High | High | Vendor assessments, SOC 2 reports | Medium | GRC Lead | Open | Annual reassessment required |

---

## Notes
- Add new risks after audits, incidents, or major system changes.  
- Residual risk should be reassessed after applying controls.  
- Closed risks should remain documented for historical and audit evidence.
