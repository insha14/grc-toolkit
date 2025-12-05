# Executive Summary

## Overview
This case study analyzes a cloud security incident caused by a misconfigured Amazon S3 bucket and overly permissive IAM role permissions, resulting in unauthorized access to sensitive customer data. The objective of this document is to demonstrate how governance, risk, and compliance (GRC) practices can be applied to investigate, document, and remediate cloud misconfigurations in a real-world environment.

## Incident Summary
An attacker exploited an overly permissive IAM role on an EC2 instance and used stolen credentials to access an S3 bucket containing customer application data. Due to misconfigured access policies, the bucket allowed broader access than intended, enabling the attacker to retrieve sensitive records including names, addresses, and portions of credit application information.

## Impact
Approximately 100,000 customer records were exposed. No financial loss occurred directly, but the incident posed significant risks to confidentiality, regulatory compliance, and organizational reputation.

## Root Cause
The primary causes identified were:
- Misconfigured S3 bucket access permissions  
- Overly broad IAM role policies attached to an EC2 instance  
- Lack of continuous cloud configuration monitoring  
- Absence of automated alerts for IAM or S3 policy drift  

## Response & Containment
The security team revoked compromised credentials, corrected S3 permissions, restricted IAM roles following least-privilege principles, and enabled additional logging and monitoring controls. A formal incident report, risk assessment, and corrective action plan were developed as part of the post-incident review.

## Key Lessons
- Cloud misconfigurations are one of the most common sources of security breaches  
- IAM roles must follow strict least-privilege standards  
- Continuous cloud security posture monitoring is essential  
- Periodic access reviews and configuration audits significantly reduce risk  

## Purpose of This Case Study
This case study demonstrates how to use GRC workflows, templates, checklists, and registers to document and remediate a real-world cloud security incident. It also serves as a practical portfolio artifact showcasing the ability to:  
- Investigate cloud misconfigurations  
- Conduct impact and risk assessments  
- Map findings to governance and compliance controls  
- Recommend remediation actions  
- Document the incident end-to-end using industry-standard practices  
