# Root Cause Analysis (RCA)

## Overview
This Root Cause Analysis examines the underlying technical, procedural, and governance-related failures that enabled unauthorized access to Highly Confidential customer data stored in an AWS S3 bucket. The analysis uses structured RCA methods, including the 5 Whys technique, to trace the incident back to systemic weaknesses.

---

# 1. Technical Root Cause
- An IAM role attached to an EC2 instance had overly broad permissions, including the ability to list and retrieve objects from multiple S3 buckets.
- The S3 bucket storing customer application data was configured with permissive access policies that allowed unintended access paths.
- The EC2 metadata service (IMDSv1) allowed token retrieval without additional hardening, enabling credential theft.
- Misconfigurations were not detected due to the absence of continuous cloud posture monitoring.

**Technical Root Cause Summary:**  
A combination of misconfigured IAM permissions and insecure S3 bucket policies created an unauthorized access pathway.

---

# 2. Governance Root Cause
- Cloud configuration baselines were not enforced consistently across environments.
- IAM policies were not included in periodic access reviews.
- No CSPM (Cloud Security Posture Management) tooling was implemented to detect configuration drift.
- Security policies existed but were not operationalized through automated controls.
- Lack of standardized approval workflow for creating or modifying IAM roles.

**Governance Root Cause Summary:**  
Weak enforcement of cloud governance practices allowed configuration drift, excessive permissions, and a lack of visibility into misconfigurations.

---

# 3. Procedural Root Cause
- The engineering team used an inline IAM policy instead of an approved, least-privilege template.
- S3 bucket creation did not require a formal review or approval step.
- No checklist was followed to validate access restrictions for Highly Confidential data.
- Logs were being collected but not actively monitored for early detection.

**Procedural Root Cause Summary:**  
Key operational processes—cloud provisioning, IAM change management, and monitoring—were not followed or were insufficiently documented.

---

# 4. 5 Whys Analysis

### **1. Why did the attacker access the S3 bucket?**  
Because the IAM role had permissions that allowed S3 access.

### **2. Why did the IAM role have excessive permissions?**  
Because the engineering team used a broad wildcard policy (`s3:*`) instead of a least-privilege policy.

### **3. Why was a wildcard policy allowed?**  
Because there was no enforced policy or technical control preventing overly permissive IAM configurations.

### **4. Why were governance controls not enforced?**  
Because the cloud environment lacked CSPM tools, automated checks, and periodic configuration audits.

### **5. Why were audits and monitoring insufficient?**  
Because cloud security responsibilities were distributed across teams without centralized oversight or ownership.

---

# 5. Contributing Factors
- Lack of S3 Block Public Access enforcement at the organizational level  
- No IAM permission boundaries  
- Metadata service not restricted (IMDSv1 enabled)  
- Missing tagging/classification on sensitive buckets  
- No approval workflow for role or bucket policy changes  
- Incomplete S3 access logs prior to incident  

---

# 6. Root Cause Conclusion
The incident occurred due to a combination of technical misconfigurations, weak cloud governance controls, and procedural gaps. Excessive IAM permissions and misconfigured S3 access policies created a vulnerability that was exploited through credential retrieval from an EC2 metadata service. Proper gove
