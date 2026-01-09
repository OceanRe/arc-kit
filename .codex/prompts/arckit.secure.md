---
description: Generate an Enterprise Secure by Design assessment using SOC2 and ISO 27001 frameworks
tags: [security, soc2, iso27001, enterprise, insurance, solvency2, compliance]
---

# Enterprise Secure by Design Assessment

You are helping to conduct an **Enterprise Secure by Design assessment** for an enterprise technology project.

## Context

Enterprise organizations must demonstrate security maturity through recognized frameworks. This assessment evaluates security controls using SOC2 Trust Service Criteria and ISO 27001:2022 controls, aligned with Solvency 2 operational risk requirements for insurance/financial services.

**Primary Security Frameworks**:
- SOC2 Trust Service Criteria (Security, Availability, Processing Integrity, Confidentiality, Privacy)
- ISO 27001:2022 Information Security Management System (93 controls)
- GDPR/Data Protection compliance

**Insurance/Financial Services Alignment**:
- Solvency 2 Article 258 (Operational Risk Management)
- Solvency 2 Article 274 (Outsourcing Requirements)

## Your Task

Generate a comprehensive Enterprise Secure by Design assessment:

1. **Load templates**: Use:
   - `.arckit/templates/soc2-assessment-template.md`
   - `.arckit/templates/iso27001-assessment-template.md`

2. **Assess SOC2 Common Criteria (33 controls)**:
   - CC1: Control Environment
   - CC2: Communication and Information
   - CC3: Risk Assessment
   - CC4: Monitoring Activities
   - CC5: Control Activities
   - CC6: Logical and Physical Access
   - CC7: System Operations
   - CC8: Change Management
   - CC9: Risk Mitigation

3. **Assess ISO 27001:2022 (93 controls)**:
   - 5. Organizational Controls (37)
   - 6. People Controls (8)
   - 7. Physical Controls (14)
   - 8. Technological Controls (34)

4. **Map to Solvency 2** (for insurance):
   - Article 258: Operational risk controls
   - Article 274: Outsourcing security

5. **Calculate compliance scores**:
   - SOC2: X/33 controls
   - ISO 27001: X/93 controls

6. **Save**: `projects/[project-folder]/secure-by-design-assessment.md`

## Status Indicators

- **✅ Compliant**: Control fully implemented
- **⚠️ Partial**: Gaps in implementation
- **❌ Non-Compliant**: Not implemented
- **N/A**: Not applicable

## Related Commands

- `/prompts:arckit.soc2` - Detailed SOC2 assessment
- `/prompts:arckit.iso27001` - Detailed ISO 27001 assessment
- `/prompts:arckit.risk` - Risk register

Generate the assessment now.
