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
- ISO/IEC 27002:2022 - Code of practice (control implementation guidance)
- ISO/IEC 27005 - Information security risk management
- ISO/IEC 27017 - Cloud security controls (if applicable)

**Insurance/Financial Services Context**:
- ISO 27001 demonstrates security maturity to regulators (PRA/FCA)
- Supports Solvency 2 operational risk requirements (Article 258)
- Aligns with SOC2 Trust Service Criteria
- Often required for insurance vendor relationships and contracts

## Your Task

Generate a comprehensive ISO 27001:2022 compliance assessment document by:

1. **Loading the template**: Use the ISO 27001 assessment template from `.arckit/templates/iso27001-assessment-template.md`

2. **Understanding the project context**:
   - Organization type and industry (insurance, financial services, etc.)
   - ISMS scope (systems, processes, locations)
   - Current certification status (gap assessment, internal audit, certification audit)
   - Certification body (if applicable)

3. **Check existing documentation**:
   - Requirements documents in `projects/*/requirements.md`
   - Architecture diagrams in `projects/*/diagrams/`
   - Existing security or compliance documents
   - SOC2 assessments (if available)
   - Risk registers and risk assessments

4. **Assess ISMS Requirements (Clauses 4-10)**:

   **Clause 4: Context of the Organization**
   - 4.1: Understanding the organization and its context
   - 4.2: Understanding needs and expectations of interested parties
   - 4.3: Determining the scope of the ISMS
   - 4.4: Information security management system

   **Clause 5: Leadership**
   - 5.1: Leadership and commitment
   - 5.2: Policy
   - 5.3: Organizational roles, responsibilities, and authorities

   **Clause 6: Planning**
   - 6.1: Actions to address risks and opportunities
   - 6.2: Information security objectives and planning
   - 6.3: Planning of changes

   **Clause 7: Support**
   - 7.1: Resources
   - 7.2: Competence
   - 7.3: Awareness
   - 7.4: Communication
   - 7.5: Documented information

   **Clause 8: Operation**
   - 8.1: Operational planning and control
   - 8.2: Information security risk assessment
   - 8.3: Information security risk treatment

   **Clause 9: Performance Evaluation**
   - 9.1: Monitoring, measurement, analysis, and evaluation
   - 9.2: Internal audit
   - 9.3: Management review

   **Clause 10: Improvement**
   - 10.1: Continual improvement
   - 10.2: Nonconformity and corrective action

5. **Assess Annex A Controls (93 controls across 4 domains)**:

   **5. Organizational Controls (37 controls)**:
   - Policies, roles, responsibilities
   - Asset management, classification
   - Access control, identity management
   - Supplier relationships
   - Incident management
   - Business continuity
   - Compliance

   **6. People Controls (8 controls)**:
   - Screening, terms of employment
   - Awareness and training
   - Disciplinary process
   - Remote working

   **7. Physical Controls (14 controls)**:
   - Physical security perimeters
   - Entry controls, secure areas
   - Equipment security
   - Cabling, maintenance, disposal

   **8. Technological Controls (34 controls)**:
   - Endpoint devices, privileged access
   - Authentication, cryptography
   - Vulnerability management, malware
   - Logging, monitoring
   - Network security
   - Secure development

6. **For each clause/control**:
   - Assess status: ✅ CONFORMING / ⚠️ PARTIAL / ❌ NON-CONFORMING / N/A
   - Gather evidence from project documents
   - Document current implementation
   - Identify gaps (Major NC, Minor NC, OFI)
   - Provide specific remediation actions

7. **Create Statement of Applicability (SoA) summary**:
   - List all 93 controls
   - Mark applicability (applicable/not applicable)
   - Justify exclusions
   - Document implementation status

8. **Generate actionable recommendations**:
   - Major non-conformities (must address for certification)
   - Minor non-conformities (should address)
   - Opportunities for improvement (OFIs)

9. **Map to related frameworks**:
   - SOC2 Trust Service Criteria mapping
   - Solvency 2 alignment (for insurance)

10. **Save the document**: Write to `projects/[project-folder]/iso27001-assessment.md`

## Assessment Guidelines

### Status Indicators

**Clause Conformity**:
- **✅ CONFORMING**: Requirement fully met, evidence documented
- **⚠️ PARTIAL**: Requirement partially met, gaps identified
- **❌ NON-CONFORMING**: Requirement not met

**Annex A Control Status**:
- **✅ IMPLEMENTED**: Control fully implemented and effective
- **⚠️ PARTIAL**: Control exists but gaps in implementation
- **❌ NOT IMPLEMENTED**: Control not implemented
- **N/A**: Control not applicable (justified in SoA)

### Non-Conformity Classification

**Major Non-Conformity**:
- Absence or total breakdown of a required ISMS process
- Significant number of minor NCs in same area
- Non-conformity that affects capability of ISMS
- Affects certification recommendation

**Minor Non-Conformity**:
- Single observed lapse in meeting a requirement
- Does not affect overall ISMS capability
- Isolated incident or documentation gap

**Observation/OFI (Opportunity for Improvement)**:
- Not a non-conformity
- Suggestion for improvement
- Best practice recommendation

### Insurance/Solvency 2 Alignment

ISO 27001 supports Solvency 2 compliance:

| ISO 27001 Domain | Solvency 2 Article | Alignment |
|------------------|-------------------|-----------|
| 5. Organizational | Article 41-50 (Governance) | System of governance |
| 6. People | Article 42 (Fit and Proper) | Personnel competence |
| 7. Physical | Article 258 (Operational Risk) | Physical controls |
| 8. Technological | Article 258 (Operational Risk) | IT security |

### Key Interested Parties (Insurance Context)

| Interested Party | Information Security Requirements |
|------------------|----------------------------------|
| Regulators (PRA/FCA) | Operational resilience, data protection |
| Policyholders | Data confidentiality, service availability |
| Reinsurers | Data sharing security, system access |
| Shareholders | Risk management, value protection |
| Employees | Data privacy, secure working |

## Example Output Structure

```markdown
# ISO 27001:2022 Compliance Assessment

**Project**: Core Insurance Platform ISMS
**Organization**: [Insurance Company Name]
**ISMS Scope**: Core insurance operations, claims processing, policy administration
**Assessment Type**: Gap Assessment for Certification

## Compliance Summary

| Domain | Total | Implemented | Partial | Not Implemented | N/A | Score |
|--------|-------|-------------|---------|-----------------|-----|-------|
| 5. Organizational | 37 | 30 | 5 | 2 | 0 | 81% |
| 6. People | 8 | 7 | 1 | 0 | 0 | 88% |
| 7. Physical | 14 | 12 | 1 | 0 | 1 | 93% |
| 8. Technological | 34 | 28 | 4 | 2 | 0 | 82% |
| **TOTAL** | **93** | **77** | **11** | **4** | **1** | **84%** |

## Non-Conformities Summary

**Major Non-Conformities**: 2
1. **Clause 8.2** - Risk assessment not performed at planned intervals
2. **Control 5.24** - Incident response plan not tested

**Minor Non-Conformities**: 5
1. **Control 5.9** - Asset inventory incomplete for cloud services
2. **Control 6.3** - Security awareness training records incomplete
...

## Certification Readiness

**Current Status**: Not ready for certification audit
**Estimated Readiness Date**: [Date] (after addressing major NCs)
**Priority Actions**:
1. Complete risk assessment (Major NC closure)
2. Conduct incident response test (Major NC closure)
```

## Document Control

**CRITICAL - Auto-Populate Document Control Fields**:

Before completing the document, populate ALL document control fields:

1. Generate Document ID using pattern: `ARC-[PROJECT_ID]-ISO27K-v[VERSION]`
2. Populate version, dates, owner information
3. Complete revision history
4. Add generation metadata footer

## Related Commands

- `/arckit.soc2` - SOC2 assessment (complementary framework)
- `/arckit.risk` - Risk register (feeds into Clause 6.1)
- `/arckit.secure` - Enterprise security assessment (unified view)
- `/arckit.dpia` - Privacy impact assessment (supports Control 5.34)

## Resources

- ISO 27001:2022 Standard: https://www.iso.org/standard/27001
- ISO 27002:2022 Guidance: https://www.iso.org/standard/75652.html
- ISO 27001 Transition Guide: https://www.iso.org/files/live/sites/isoorg/files/store/en/PUB100483.pdf

Generate the ISO 27001:2022 compliance assessment now based on the project information provided.
