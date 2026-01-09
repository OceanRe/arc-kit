---
description: Generate an ISO 27001:2022 compliance assessment for information security management
tags: [security, compliance, iso27001, isms, audit, insurance]
---

# ISO 27001:2022 Compliance Assessment

You are helping to conduct an **ISO 27001:2022 compliance assessment** for an enterprise Information Security Management System (ISMS).

## Context

ISO 27001:2022 is the international standard for Information Security Management Systems (ISMS). The 2022 version includes 93 controls across 4 domains (Organizational, People, Physical, Technological). This assessment evaluates both the ISMS management system requirements (Clauses 4-10) and the Annex A controls.

**Key ISO 27001 References**:
- ISO/IEC 27001:2022 - Requirements
- ISO/IEC 27002:2022 - Code of practice
- ISO/IEC 27005 - Information security risk management

**Insurance/Financial Services Context**:
- ISO 27001 demonstrates security maturity to regulators
- Supports Solvency 2 operational risk requirements (Article 258)
- Aligns with SOC2 Trust Service Criteria
- Often required for insurance vendor relationships

## Your Task

Generate a comprehensive ISO 27001:2022 compliance assessment document by:

1. **Loading the template**: Use the ISO 27001 assessment template from `.arckit/templates/iso27001-assessment-template.md`

2. **Understanding the project context**:
   - Organization type and industry
   - ISMS scope (systems, processes, locations)
   - Current certification status
   - Certification body (if applicable)

3. **Assess ISMS Requirements (Clauses 4-10)**:
   - Clause 4: Context of the Organization
   - Clause 5: Leadership
   - Clause 6: Planning
   - Clause 7: Support
   - Clause 8: Operation
   - Clause 9: Performance Evaluation
   - Clause 10: Improvement

4. **Assess Annex A Controls (93 controls)**:
   - 5. Organizational Controls (37 controls)
   - 6. People Controls (8 controls)
   - 7. Physical Controls (14 controls)
   - 8. Technological Controls (34 controls)

5. **For each clause/control**:
   - Assess status: ✅ CONFORMING / ⚠️ PARTIAL / ❌ NON-CONFORMING / N/A
   - Document current implementation
   - Identify gaps (Major NC, Minor NC, OFI)
   - Provide remediation actions

6. **Create Statement of Applicability (SoA) summary**

7. **Map to related frameworks**:
   - SOC2 Trust Service Criteria mapping
   - Solvency 2 alignment (for insurance)

8. **Save the document**: Write to `projects/[project-folder]/iso27001-assessment.md`

## Non-Conformity Classification

**Major Non-Conformity**: Absence or total breakdown of a required ISMS process
**Minor Non-Conformity**: Single observed lapse in meeting a requirement
**OFI**: Opportunity for improvement (not a non-conformity)

## Related Commands

- `/prompts:arckit.soc2` - SOC2 assessment (complementary framework)
- `/prompts:arckit.risk` - Risk register (feeds into Clause 6.1)
- `/prompts:arckit.secure` - Enterprise security assessment

Generate the ISO 27001:2022 compliance assessment now based on the project information provided.
