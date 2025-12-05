# Sample Audit Report

## Overview
This sample audit report illustrates how audit observations, control evaluations, and recommendations are documented during an internal or external audit. The format below reflects a simplified but realistic structure commonly used in ITGC, SOC 2 readiness, and ISO 27001 internal audits. The purpose of this example is to demonstrate how findings are communicated clearly and professionally to management and stakeholders.

## Executive Summary
The audit focused on evaluating the effectiveness of key information technology general controls (ITGCs) related to access management, change management, and IT operations. Overall, the organization has implemented foundational controls; however, several areas require improvement to strengthen security and reduce operational risk. The issues identified relate primarily to delayed access removal, inconsistent change documentation, and insufficient log review practices. Recommendations have been provided to address these gaps.

## Scope and Objectives
The scope of this audit included systems supporting the organization’s core operations, with a focus on user access provisioning and deprovisioning, change management processes, backup operations, and log review activities. The objectives were to assess whether controls are designed appropriately, operating effectively, and aligned with internal policies and industry best practices.

## Methodology
The audit was conducted through a combination of document review, interviews with control owners, system walkthroughs, and testing of selected samples. Evidence was evaluated to determine whether key controls were functioning as intended. Findings were classified based on severity, considering both likelihood and potential business impact.

## Detailed Findings

### Finding 1: Delayed Removal of Terminated Users  
**Severity:** High  
The audit identified multiple user accounts belonging to terminated employees that remained active for more than seven days. This increases the risk of unauthorized access and violates the organization's access management policy.  
**Recommendation:** Implement automated HR-to-IT notifications and perform weekly reconciliation of active accounts to ensure timely removal.

### Finding 2: Incomplete Change Documentation  
**Severity:** Medium  
A sample of change requests revealed missing approval records and insufficient testing evidence. Inconsistent documentation increases the likelihood of introducing system errors or security vulnerabilities.  
**Recommendation:** Enforce mandatory fields in the change management system and conduct periodic reviews to verify compliance with the change control process.

### Finding 3: Limited Log Review Activities  
**Severity:** Medium  
System and security logs are not being reviewed on a documented schedule. This limits the organization’s ability to detect suspicious activity or unauthorized changes.  
**Recommendation:** Establish a formal log review schedule, assign ownership, and retain evidence of log review activities for audit purposes.

### Finding 4: Backup Restoration Not Tested Regularly  
**Severity:** Low  
Backups are performed daily; however, restoration testing has not been conducted in the past six months. Without periodic testing, there is no assurance that backups can be successfully restored during an incident.  
**Recommendation:** Conduct quarterly restoration tests and document results.

## Conclusion
The audit identified several control gaps that, if addressed promptly, will significantly improve the organization’s security posture. Management should prioritize the remediation of high-severity issues and establish monitoring mechanisms to ensure the sustained effectiveness of critical controls. The audit team will follow up on remediation efforts as part of the next quarterly review.

