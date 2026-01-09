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

   **Availability (A) - OPTIONAL** (3 controls)
   **Processing Integrity (PI) - OPTIONAL** (5 controls)
   **Confidentiality (C) - OPTIONAL** (2 controls)
   **Privacy (P) - OPTIONAL** (18 controls)

5. **For each control**:
   - Assess status: ✅ COMPLIANT / ⚠️ PARTIAL / ❌ NON-COMPLIANT / N/A
   - Gather evidence from project documents
   - Document current implementation
   - Identify gaps and remediation actions

6. **Calculate overall compliance score**: X/61 controls compliant

7. **Map to related frameworks**:
   - ISO 27001:2022 control mapping
   - Solvency 2 operational risk alignment (for insurance)

8. **Save the document**: Write to `projects/[project-folder]/soc2-assessment.md`

## Trust Service Categories Selection Guide

**Always Include**:
- ✅ **Security (CC)** - Required for all SOC2 reports

**Include If Applicable**:
- **Availability (A)** - If system uptime/availability is committed to customers
- **Processing Integrity (PI)** - If accurate data processing is critical
- **Confidentiality (C)** - If handling confidential business information
- **Privacy (P)** - If processing personal information

## Related Commands

- `/prompts:arckit.iso27001` - ISO 27001:2022 assessment
- `/prompts:arckit.risk` - Risk register (operational risks feed into CC3)
- `/prompts:arckit.secure` - Enterprise security assessment

Generate the SOC2 Type II compliance assessment now based on the project information provided.
