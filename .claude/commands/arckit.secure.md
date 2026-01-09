---
description: Generate an Enterprise Secure by Design assessment using SOC2 and ISO 27001 frameworks
tags: [security, soc2, iso27001, enterprise, insurance, solvency2, compliance]
---

# Enterprise Secure by Design Assessment

You are helping to conduct an **Enterprise Secure by Design assessment** for an enterprise technology project, using industry-standard security frameworks.

## Context

Enterprise organizations must demonstrate security maturity through recognized frameworks. This assessment evaluates security controls using SOC2 Trust Service Criteria and ISO 27001:2022 controls, aligned with Solvency 2 operational risk requirements for insurance/financial services.

## User Input

```text
$ARGUMENTS
```

## Instructions

1. **Check for prerequisites**:
   - Requirements (`projects/*/requirements.md`)
   - Architecture diagrams
   - Risk register (`projects/*/risk-register.md`)

2. **Generate the Assessment**:
   - Use the template at `.arckit/templates/secure-by-design-template.md`.
   - Populate the **SOC2 Assessment** section using knowledge of the 5 Trust Service Criteria.
   - Populate the **ISO 27001 Assessment** section using the 93 controls from the 2022 standard.
   - Address **Solvency 2** specific requirements (Article 258 Operational Risk, Article 274 Outsourcing).

3. **Output**:
   - Create `projects/[PROJECT_NAME]/secure-by-design-assessment.md`.
   - Ensure the document provides a clear "Go/No-Go" view on security maturity.

**CRITICAL - Auto-Populate Document Control Fields**:
- `[PROJECT_ID]`
- `[VERSION]`
- `[DATE]`
- `ARC-[PROJECT_ID]-SECD-v[VERSION]`

## Output Format

Provide:
1. **Location**: `projects/[PROJECT_NAME]/secure-by-design-assessment.md`
2. **Summary**:
   - "Created Secure by Design assessment"
   - "Compliance Score: SOC2 [X]%, ISO 27001 [Y]%"
   - "Critical Risks: [N] identified"
   - "Solvency 2 Alignment: [Addressed/Gap]"

## Template Reference

Use `.arckit/templates/secure-by-design-template.md`.
