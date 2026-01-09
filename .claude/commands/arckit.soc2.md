---
description: Generate a SOC2 Type II compliance assessment for enterprise systems
tags: [security, compliance, soc2, trust-services, audit, insurance]
---

# SOC2 Type II Compliance Assessment

You are helping to conduct a **SOC2 Type II compliance assessment** for an enterprise technology project.

## Context

SOC2 (Service Organization Control 2) is a framework developed by the AICPA (American Institute of Certified Public Accountants) for managing customer data based on five Trust Service Criteria. This assessment evaluates security controls required for enterprise systems, particularly those handling sensitive customer data.

**Key SOC2 References**:
- AICPA Trust Service Criteria (TSC)
- SOC2 Type II examination requirements
- Common Criteria (Security) - Required for all SOC2 reports
- Optional categories: Availability, Processing Integrity, Confidentiality, Privacy

**Insurance/Financial Services Context**:
- SOC2 aligns with Solvency 2 operational risk requirements (Article 258)
- Supports ISO 27001 compliance (many overlapping controls)
- Demonstrates security maturity to regulators and customers
- Required for many vendor relationships and insurance contracts

## Your Task

Generate a comprehensive SOC2 Type II compliance assessment document by:

1. **Loading the template**: Use the SOC2 assessment template from `.arckit/templates/soc2-assessment-template.md`

2. **Understanding the project context**:
   - Organization type and industry (insurance, financial services, etc.)
   - Systems and services in scope
   - Trust Service Categories to include (Security is always required)
   - Current compliance status (new assessment, renewal, remediation)
   - Reporting period for Type II (typically 6-12 months)

3. **Check existing documentation**:
   - Requirements documents in `projects/*/requirements.md`
   - Architecture diagrams in `projects/*/diagrams/`
   - Existing security or compliance documents
   - ISO 27001 assessments (if available)
   - Risk registers

4. **Assess compliance across Trust Service Categories**:

   **Security (Common Criteria - CC) - REQUIRED** (33 controls):
   - CC1: Control Environment (5 controls)
   - CC2: Communication and Information (3 controls)
   - CC3: Risk Assessment (4 controls)
   - CC4: Monitoring Activities (2 controls)
   - CC5: Control Activities (3 controls)
   - CC6: Logical and Physical Access (8 controls)
   - CC7: System Operations (5 controls)
   - CC8: Change Management (1 control)
   - CC9: Risk Mitigation (2 controls)

   **Availability (A) - OPTIONAL** (3 controls):
   - A1.1: Capacity management
   - A1.2: Environmental controls and recovery
   - A1.3: Recovery testing

   **Processing Integrity (PI) - OPTIONAL** (5 controls):
   - PI1.1-PI1.5: Processing accuracy, completeness, authorization

   **Confidentiality (C) - OPTIONAL** (2 controls):
   - C1.1: Confidential information identification
   - C1.2: Confidential information disposal

   **Privacy (P) - OPTIONAL** (18 controls):
   - P1-P8: Notice, choice, collection, use, access, disclosure, quality, monitoring

5. **For each control**:
   - Assess status: ✅ COMPLIANT / ⚠️ PARTIAL / ❌ NON-COMPLIANT / N/A
   - Gather evidence from project documents
   - Document current implementation
   - Identify gaps and risks
   - Provide specific remediation actions with owners and timelines

6. **Calculate overall compliance score**: X/61 controls compliant (if all categories in scope)

7. **Identify critical compliance gaps**:
   - Controls that block SOC2 certification
   - High-risk deficiencies
   - Controls affecting multiple criteria

8. **Generate actionable recommendations**:
   - Critical priority (0-30 days) - certification blockers
   - High priority (1-3 months) - significant gaps
   - Medium priority (3-6 months) - continuous improvement

9. **Map to related frameworks**:
   - ISO 27001:2022 control mapping
   - Solvency 2 operational risk alignment (for insurance)

10. **Save the document**: Write to `projects/[project-folder]/soc2-assessment.md`

## Trust Service Categories Selection Guide

**Always Include**:
- ✅ **Security (CC)** - Required for all SOC2 reports

**Include If Applicable**:
- **Availability (A)** - If system uptime/availability is committed to customers
- **Processing Integrity (PI)** - If accurate data processing is critical (insurance claims, financial transactions)
- **Confidentiality (C)** - If handling confidential business information beyond PII
- **Privacy (P)** - If processing personal information (customer data, policyholder information)

**Insurance/Financial Services Typical Scope**:
- Security (CC) + Availability (A) + Processing Integrity (PI) + Confidentiality (C) + Privacy (P)
- Full scope recommended due to policyholder data and regulatory expectations

## Assessment Guidelines

### Status Indicators

- **✅ COMPLIANT**: Control fully implemented, evidence documented, operating effectively
- **⚠️ PARTIAL**: Control exists but gaps in implementation or evidence
- **❌ NON-COMPLIANT**: Control not implemented or ineffective
- **N/A**: Control genuinely not applicable (must justify)

### Control Testing Evidence

**Design Effectiveness** (Does the control address the risk?):
- Control documentation exists
- Control is appropriately designed
- Control ownership assigned

**Operating Effectiveness** (Is the control working over time?):
- Evidence of consistent execution
- Testing or monitoring results
- Exception handling documented

### Insurance/Solvency 2 Alignment

SOC2 controls support Solvency 2 compliance:

| SOC2 Category | Solvency 2 Article | Alignment |
|---------------|-------------------|-----------|
| Security (CC) | Article 258 (Operational Risk) | IT security controls |
| Availability (A) | Article 258 (Business Continuity) | System availability |
| Processing Integrity (PI) | Article 82 (Data Quality) | Accurate processing |
| Confidentiality (C) | Article 274 (Outsourcing) | Data protection |
| Privacy (P) | GDPR Integration | Personal data |

## Example Output Structure

```markdown
# SOC2 Type II Compliance Assessment

**Project**: Claims Processing System
**Organization**: [Insurance Company Name]
**Trust Service Categories**: Security, Availability, Processing Integrity, Confidentiality, Privacy

## Compliance Summary

| Category | Controls | Compliant | Partial | Non-Compliant | Score |
|----------|----------|-----------|---------|---------------|-------|
| Security (CC) | 33 | 28 | 4 | 1 | 85% |
| Availability (A) | 3 | 3 | 0 | 0 | 100% |
| Processing Integrity (PI) | 5 | 4 | 1 | 0 | 80% |
| Confidentiality (C) | 2 | 2 | 0 | 0 | 100% |
| Privacy (P) | 18 | 15 | 2 | 1 | 83% |
| **TOTAL** | **61** | **52** | **7** | **2** | **85%** |

## Critical Gaps

1. **CC7.1 - Vulnerability Management** - ❌ Non-compliant
   - Gap: No formal vulnerability scanning program
   - Risk: High - Cannot demonstrate vulnerability management to auditor
   - Remediation: Implement weekly vulnerability scanning - Due: 30 days

2. **P3 - Data Collection** - ❌ Non-compliant
   - Gap: Privacy notice does not cover all data collection points
   - Risk: Medium - Privacy principle violation
   - Remediation: Update privacy notice - Due: 14 days
```

## Document Control

**CRITICAL - Auto-Populate Document Control Fields**:

Before completing the document, populate ALL document control fields:

1. Generate Document ID using pattern: `ARC-[PROJECT_ID]-SOC2-v[VERSION]`
2. Populate version, dates, owner information
3. Complete revision history
4. Add generation metadata footer

## Related Commands

- `/arckit.iso27001` - ISO 27001:2022 assessment (complementary framework)
- `/arckit.risk` - Risk register (operational risks feed into CC3)
- `/arckit.secure` - Enterprise security assessment (unified view)
- `/arckit.dpia` - Privacy impact assessment (supports Privacy category)

## Resources

- AICPA Trust Service Criteria: https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/trustservices
- SOC2 Guide: https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations
- SOC2 Academy: https://www.aicpa.org/cpe-learning/course/soc-2-academy

Generate the SOC2 Type II compliance assessment now based on the project information provided.
