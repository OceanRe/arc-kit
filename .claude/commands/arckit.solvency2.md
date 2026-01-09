---
description: Perform a Solvency II Pillar 2 governance assessment
globs: .arckit/templates/solvency2-governance-template.md
---
# arckit.solvency2

This command performs a Solvency II Pillar 2 governance assessment for the insurance enterprise.

## Usage

```bash
/arckit.solvency2
```

## Description

The command generates a `solvency2-governance.md` file in the project directory, assessing compliance with Pillar 2 requirements including:
- General Governance Requirements (Fit & Proper, Outsourcing, Remuneration)
- Key Functions (Risk, Compliance, Internal Audit, Actuarial)
- Risk Management System (Underwriting, Market, Credit, Operational Risks)
- ORSA Governance

## Parameters

None. The command uses the template `.arckit/templates/solvency2-governance-template.md`.

## Example Output

```markdown
# Solvency II Pillar 2 Governance Assessment

## Executive Summary
**Assessment Outcome**: COMPLIANT

## 1. Governance System
...
```
