# Enterprise Secure by Design Assessment

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-[PROJECT_ID]-SECD-v[VERSION] |
| **Project** | [PROJECT_NAME] (Project [PROJECT_ID]) |
| **Document Type** | Secure by Design Assessment |
| **Classification** | [CONFIDENTIAL / INTERNAL] |
| **Version** | [VERSION] |
| **Status** | [DRAFT / IN_REVIEW / APPROVED] |
| **Date** | [YYYY-MM-DD] |
| **Owner** | [OWNER_NAME_AND_ROLE] |

## Executive Summary

### Assessment Overview
This document evaluates the security posture of [PROJECT_NAME] against enterprise security standards, including **SOC2 Trust Service Criteria** and **ISO 27001:2022**, aligned with **Solvency 2** operational risk requirements.

### Security Maturity Score
| Framework | Scope | Compliance Score | Status |
|-----------|-------|------------------|--------|
| **SOC2 Common Criteria** | Security, Availability, Confidentiality | [X]% | [R/A/G] |
| **ISO 27001:2022** | Organizational, People, Physical, Tech | [X]% | [R/A/G] |
| **Solvency 2** | Operational Risk (Art 258), Outsourcing | [X]% | [R/A/G] |

### Critical Risks & Gaps
1. **[Risk 1]**: [Description] - [Remediation Plan]
2. **[Risk 2]**: [Description] - [Remediation Plan]

---

## 1. SOC2 Trust Service Criteria Assessment

### 1.1 Security (Common Criteria)
*Focus: Protection against unauthorized access, disclosure, or damage.*

| Control Area | Key Controls | Status | Evidence/Gaps |
|--------------|--------------|--------|---------------|
| **CC1 Control Environment** | Ethics, Board Oversight, HR Security | [✅/⚠️/❌] | |
| **CC2 Communication** | Internal/External Info Sharing | [✅/⚠️/❌] | |
| **CC3 Risk Assessment** | Risk ID, Fraud Risk, Change Risk | [✅/⚠️/❌] | |
| **CC4 Monitoring** | Ongoing Evaluations, Deficiency Mgmt | [✅/⚠️/❌] | |
| **CC5 Control Activities** | Mitigation Logic, Policies | [✅/⚠️/❌] | |
| **CC6 Logical Access** | MFA, IAM, RBAC, Encryption | [✅/⚠️/❌] | |
| **CC7 System Ops** | Vuln Mgmt, Incident Response | [✅/⚠️/❌] | |
| **CC8 Change Mgmt** | Change Authorization, Testing | [✅/⚠️/❌] | |
| **CC9 Risk Mitigation** | Vendor Risk, Business Continuity | [✅/⚠️/❌] | |

### 1.2 Availability (Optional)
*Focus: System availability for operation and use.*
- **Controls**: Capacity management, Backup/Recovery testing, Environmental controls.
- **Status**: [Assessment]

### 1.3 Confidentiality (Optional)
*Focus: Information designated as confidential is protected.*
- **Controls**: Data classification, Disposal, Confidentiality agreements.
- **Status**: [Assessment]

### 1.4 Processing Integrity (Optional)
*Focus: System processing is complete, valid, accurate, timely, and authorized.*
- **Controls**: Input/Output validation, Error handling.
- **Status**: [Assessment]

### 1.5 Privacy (Optional)
*Focus: Personal information is collected, used, retained, and disclosed in conformity with commitments.*
- **Controls**: Notice, Choice/Consent, Access, Disclosure.
- **Status**: [Assessment] (See DPIA for details)

---

## 2. ISO 27001:2022 Controls Assessment

### 2.1 Organizational Controls (Clause 5)
*Policies, Cloud Services, ICT Supply Chain*

| Control | Requirement | Implementation | Status |
|---------|-------------|----------------|--------|
| **5.1** | Info Security Policies | Policies defined and approved | [Status] |
| **5.7** | Threat Intelligence | Threat feeds integrated | [Status] |
| **5.23** | Cloud Security | Cloud provider assessment | [Status] |
| **5.30** | ICT Continuity | DR plans aligned with RTO/RPO | [Status] |

### 2.2 People Controls (Clause 6)
*Screening, Awareness, Remote Working*

| Control | Requirement | Implementation | Status |
|---------|-------------|----------------|--------|
| **6.1** | Screening | Background checks | [Status] |
| **6.3** | Awareness Training | Annual security training | [Status] |
| **6.7** | Remote Working | VPN, Endpoint protection | [Status] |

### 2.3 Physical Controls (Clause 7)
*Perimeters, Equipment, Clear Desk*

| Control | Requirement | Implementation | Status |
|---------|-------------|----------------|--------|
| **7.1** | Physical Perimeters | Data center security (AWS/Azure) | [Status] |
| **7.10** | Storage Media | Encrypted disks, secure disposal | [Status] |

### 2.4 Technological Controls (Clause 8)
*Access, Encryption, Secure Coding, Logging*

| Control | Requirement | Implementation | Status |
|---------|-------------|----------------|--------|
| **8.3** | Info Access Restriction | Least privilege access | [Status] |
| **8.8** | Vuln Management | Automated scanning | [Status] |
| **8.24** | Cryptography | Encryption at rest/transit | [Status] |
| **8.28** | Secure Coding | SAST/DAST in CI/CD | [Status] |

---

## 3. Insurance & Solvency 2 Alignment

### 3.1 Operational Risk (Article 258)
**Requirement**: Insurance undertakings must have internal processes and procedures to manage operational risk (including IT security).

- **IT Security Controls**: [Describe alignment with ISO/SOC2 controls above]
- **Cyber Risk Quantification**: [Describe how cyber risk is quantified for capital purposes]

### 3.2 Outsourcing (Article 274)
**Requirement**: Written agreements with service providers must ensure compliance.

- **Cloud/Vendor Security**: [Confirm security clauses in contracts]
- **Audit Rights**: [Confirm right to audit is preserved]

### 3.3 Data Quality (Article 82)
**Requirement**: Data used for technical provisions must be accurate, complete, and appropriate.

- **Data Integrity Controls**: [Describe validation and reconciliation controls]

---

## 4. Remediation Plan

| ID | Finding | Action | Owner | Due Date | Priority |
|----|---------|--------|-------|----------|----------|
| SEC-01 | [e.g., No MFA] | [Implement MFA] | [CISO] | [Date] | Critical |
| SEC-02 | [e.g., Weak Logging] | [Enable CloudWatch] | [DevOps] | [Date] | High |

---

## 5. Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Solution Architect** | | | |
| **Security Architect** | | | |
| **CISO / DPO** | | | |

---
**Generated by**: ArcKit `/arckit.secure` command
**Model**: [AI_MODEL]
