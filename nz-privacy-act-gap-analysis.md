# NZ Privacy Act 2020 — Compliance Gap Analysis Report

**Analyst:** Julita Patel  
**Date:** 29 May 2026  
**Organisation Assessed:** HealthTrack NZ (Fictional NZ Healthcare Startup)  
**Framework:** New Zealand Privacy Act 2020 — 13 Information Privacy Principles  
**Tool:** NZ_Privacy_Act_2020_Compliance_Checklist.xlsx  

---

## Executive Summary

A compliance assessment was conducted against all 13 Information Privacy Principles 
of the NZ Privacy Act 2020 for a fictional NZ healthcare startup — HealthTrack NZ — 
that collects patient appointment data, medical history, and billing information.

The assessment identified significant compliance gaps across storage security, 
data retention, third-party disclosure, and transborder data flows. Immediate 
remediation is recommended for 4 Non-Compliant principles.

---

## Compliance Summary

| Status | Count | Percentage |
|--------|-------|------------|
| ✅ Compliant | 3 | 23% |
| ⚠️ Partially Compliant | 6 | 46% |
| ❌ Non-Compliant | 4 | 31% |
| **Total** | **13** | **100%** |

---

## Critical Findings — Non-Compliant (Immediate Action Required)

### Principle 5 — Storage and Security ❌
**Finding:** No encryption on the patient database and no access controls documented.  
**Risk:** High — unauthorised access to sensitive patient health data could result in 
a notifiable privacy breach under the Privacy Act 2020, requiring notification to 
the Privacy Commissioner and affected individuals.  
**Recommendation:** Implement database encryption at rest and in transit, role-based 
access controls (RBAC), and a documented data security policy immediately.

---

### Principle 9 — Retention of Personal Information ❌
**Finding:** No data retention policy exists — patient records are kept indefinitely.  
**Risk:** Medium — retaining data beyond its necessary period increases exposure in 
the event of a breach and breaches the Act.  
**Recommendation:** Implement a data retention policy specifying a minimum retention 
period of 7 years for health records in line with NZ health sector guidelines, 
followed by secure destruction.

---

### Principle 11 — Disclosure of Personal Information ❌
**Finding:** No data sharing agreement in place with the third-party billing provider 
who receives patient data.  
**Risk:** High — disclosing personal information to a third party without a formal 
agreement or lawful basis is a direct breach of the Act.  
**Recommendation:** Implement data sharing agreements with all third parties 
immediately, documenting what data is shared, why, and under what conditions.

---

### Principle 13 — Transborder Data Flows ❌
**Finding:** Cloud storage servers are located in the USA with no data transfer 
agreement confirming equivalent privacy protections.  
**Risk:** High — transferring personal health information outside NZ without 
equivalent protections is a breach of the Act.  
**Recommendation:** Either migrate to a NZ or Australia-based cloud region, or 
implement a formal data transfer agreement confirming the receiving country provides 
comparable privacy protections to the NZ Privacy Act 2020.

---

## Moderate Findings — Partially Compliant (Action Required)

### Principle 1 — Purpose of Collection ⚠️
No formal data collection policy is documented. While data collection appears 
lawful in practice, the absence of a written policy creates compliance risk. 
**Action:** Create a written data collection policy.

### Principle 3 — Collection of Information from Subject ⚠️
Patients are not formally informed of why their data is collected or who receives 
it. **Action:** Implement a patient consent form and privacy notice.

### Principle 6 — Access to Personal Information ⚠️
No formal Subject Access Request (SAR) process exists. Under the Act, individuals 
have the right to access their information within 20 working days. 
**Action:** Create a documented SAR process.

### Principle 7 — Correction of Personal Information ⚠️
No correction request procedure exists. 
**Action:** Implement a formal correction request process.

### Principle 8 — Accuracy of Personal Information ⚠️
No regular review process for verifying or updating patient records. 
**Action:** Implement quarterly data quality reviews.

### Principle 10 — Use of Personal Information ⚠️
Patient data is used for internal reporting without explicit consent for this 
secondary purpose. **Action:** Obtain explicit consent for any secondary data use.

---

## Compliant Principles — No Action Required

| Principle | Status | Notes |
|-----------|--------|-------|
| 2 — Source of collection | ✅ | Data collected directly from patients |
| 4 — Manner of collection | ✅ | Ethical collection practices in place |
| 12 — Unique identifiers | ✅ | Internally generated IDs, not shared with other agencies |

---

## Remediation Priority Matrix

| Priority | Principle | Action | Timeline |
|----------|-----------|--------|----------|
| 🔴 Immediate | 5 — Storage and Security | Implement encryption and access controls | Week 1 |
| 🔴 Immediate | 11 — Disclosure | Data sharing agreements with third parties | Week 1 |
| 🔴 Immediate | 13 — Transborder flows | Migrate to NZ/AU cloud region | Week 2 |
| 🔴 Immediate | 3 — Collection notice | Patient consent form and privacy notice | Week 2 |
| 🟡 Short-term | 9 — Retention | Data retention policy | Month 1 |
| 🟡 Short-term | 6 — Access | Subject Access Request process | Month 1 |
| 🟡 Short-term | 1 — Purpose | Written data collection policy | Month 1 |
| 🟡 Short-term | 7 — Correction | Correction request procedure | Month 2 |
| 🟡 Short-term | 8 — Accuracy | Quarterly data quality reviews | Month 2 |
| 🟡 Short-term | 10 — Secondary use | Consent for secondary data use | Month 2 |

---

## Key NZ Privacy Act 2020 Context

- The Privacy Act 2020 replaced the Privacy Act 1993 and came into force 1 December 2020
- Organisations must notify the Privacy Commissioner of serious privacy breaches
- The Privacy Commissioner can issue compliance notices and initiate proceedings
- Individuals can complain to the Privacy Commissioner if their privacy rights are breached
- Health information is classified as sensitive information requiring higher protection standards
- Source: privacy.org.nz

---

## Tools and Frameworks Used

| Tool | Purpose |
|------|---------|
| NZ Privacy Act 2020 | Primary compliance framework |
| privacy.org.nz | Official guidance and principle definitions |
| NZ_Privacy_Act_2020_Compliance_Checklist.xlsx | Assessment spreadsheet with colour-coded results |

---

## MITRE ATT&CK Relevance

Several non-compliant findings directly relate to cybersecurity threats:

| Privacy Gap | Related ATT&CK Technique | Risk |
|-------------|--------------------------|------|
| No database encryption (P5) | T1530 — Data from Cloud Storage | Unauthorised data access |
| No access controls (P5) | T1078 — Valid Accounts | Insider threat or credential abuse |
| Third-party disclosure (P11) | T1567 — Exfiltration to Cloud | Data exfiltration risk |
| Transborder flows (P13) | T1537 — Transfer to Cloud Account | Cross-border data exposure |

---

*This report was produced as part of a personal GRC analyst portfolio project.*  
*Analyst: Julita Patel | julitakpatel@gmail.com | Wellington, New Zealand*  
*GitHub: github.com/P1992J/soc-analyst-portfolio*
