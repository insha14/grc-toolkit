# Impact Assessment

## Overview
This document provides a structured assessment of the business, technical, regulatory, operational, and reputational impacts resulting from the cloud misconfiguration incident involving unauthorized access to an S3 bucket containing sensitive customer data.

---

## 1. Data Impact
- **Data Exposed:** Customer PII, including names, addresses, and partial credit application information  
- **Data Volume:** Approximately 100,000 customer records  
- **Classification Level:** Highly Confidential  
- **Affected Systems:** AWS S3 bucket storing application data; EC2 IAM role with excessive permissions  

**Impact Summary:**  
The exposure of Highly Confidential data increases the risk of identity theft, fraud, and privacy violations.

---

## 2. Business Impact
- Temporary disruption to internal operations  
- Immediate resource allocation required for incident investigation  
- Increased support inquiries from customers  
- Additional engineering and security workload to correct misconfigurations  

**Impact Summary:**  
Overall business operations continued, but the incident redirected technical and security resources for 48–72 hours and caused reputational concern among leadership.

---

## 3. Regulatory & Compliance Impact
Potential implications under:
- **GLBA (Gramm–Leach–Bliley Act)**  
- **PCI DSS** (partial credit application fields)  
- **State privacy laws** depending on customer location  

Possible outcomes:
- Mandatory breach notifications  
- Fines if negligence is proven  
- Increased audit scrutiny  

**Impact Summary:**  
The organization may have regulatory reporting obligations within defined timeframes and could face compliance penalties if gaps are not remediated.

---

## 4. Financial Impact
- No direct fraudulent transactions observed  
- Costs incurred for:  
  - Forensic analysis  
  - Cloud configuration audit  
  - Additional monitoring tools  
  - External legal review (if required)  

Estimated cost: **Moderate**, depending on regulator involvement.

---

## 5. Reputational Impact
- Loss of customer trust due to exposure of personal data  
- Increased risk of negative media coverage if incident becomes public  
- Executives concerned about long-term brand implications  

**Impact Summary:**  
Reputational impact is moderate to high depending on external disclosure requirements.

---

## 6. Operational Impact
- Engineering teams halted deployments during investigation  
- Cloud configurations across all environments required review  
- Increased load on support and security operations teams  

**Impact Summary:**  
Operations slowed but did not stop; long-term improvements required to prevent recurrence.

---

## 7. Overall Severity Rating
| Factor | Rating |
|--------|--------|
| Data Sensitivity | High |
| Volume of Data | High |
| Regulatory Exposure | Medium–High |
| Business Disruption | Medium |
| Likelihood of Recurrence | Medium |

### ⭐ **Overall Incident Severity: HIGH**

---

## Notes
- This impact assessment informs the corrective action plan and risk register updates.  
- All findings will be referenced in the final audit report and executive summary.  
