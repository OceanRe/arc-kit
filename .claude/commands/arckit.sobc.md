---
description: Create Strategic Outline Business Case (SOBC) using Insurance Investment Appraisal model
tags: [business-case, sobc, insurance, investment, finance, solvency2]
---

# Insurance Strategic Outline Business Case (SOBC)

You are helping an enterprise architect create a Strategic Outline Business Case (SOBC) to justify investment in a technology project for an insurance company.

## About SOBC

A **Strategic Outline Business Case (SOBC)** is the first stage in the investment lifecycle:
- **SOBC**: Strategic Outline (this command) - High-level case for change, done BEFORE detailed requirements
- **OBC**: Outline Business Case - After some design work, with refined costs
- **FBC**: Full Business Case - Detailed case with accurate costs, ready for final approval

This command creates the **SOBC** - the strategic case to secure approval to proceed with requirements and design.

## User Input

```text
$ARGUMENTS
```

## Instructions

This command creates a **Strategic Outline Business Case (SOBC)** following standard Insurance Investment Appraisal methodology. This is a high-level justification done BEFORE detailed requirements to secure approval and funding.

**When to use this:**
- **After**: `/arckit.stakeholders` (MANDATORY - SOBC must link to stakeholder goals)
- **Before**: `/arckit.requirements` (SOBC justifies whether to proceed with detailed requirements)
- **Purpose**: Secure executive approval and funding to proceed to next stage

**Note**: Later stages will create OBC (Outline Business Case) and FBC (Full Business Case) with more accurate costs. This SOBC uses strategic estimates and options analysis.

1. **Check for prerequisites**:
   - **MANDATORY**: Check if stakeholder analysis exists for this project
     - Read `.arckit/memory/` or `projects/*/stakeholder-drivers.md` to find it
     - If NO stakeholder analysis exists, STOP and tell user:
       "⚠️ SOBC requires stakeholder analysis. Run `/arckit.stakeholders` first to identify who benefits and why."
   - **RECOMMENDED**: Check if architecture principles exist
     - Read `.arckit/memory/architecture-principles.md`
     - If exists, use for strategic alignment
   - **OPTIONAL**: Check if requirements exist
     - If exists, use for more accurate estimates
     - If not, use high-level cost estimates

2. **Understand the request**: The user may be:
   - Creating initial SOBC (most common)
   - Updating existing SOBC with new information
   - Evaluating multiple strategic options

3. **Determine project context**:
   - Focus on **Insurance** context (underwriting, claims, solvency, regulation)
   - Check stakeholder analysis for insurance-specific stakeholders (Chief Actuary, Chief Underwriting Officer, CRO)

4. **Read stakeholder analysis carefully**:
   - Extract ALL stakeholder goals (these become benefits!)
   - Extract stakeholder drivers (these explain WHY project needed)
   - Extract conflicts (these become risks/mitigations)
   - Extract outcomes (these become success criteria)
   - Note: EVERY benefit in SOBC MUST trace to a stakeholder goal

5. **Generate comprehensive SOBC** following the template at `.arckit/templates/sobc-template.md`:

   **Structure (Insurance Investment Appraisal)**:

   **1. Executive Summary**:
   - Purpose, Recommendation, Financial Summary (NPV, ROI, Payback), Solvency II Impact.

   **2. Strategic Context**:
   - Alignment with Business Plan (Growth, Efficiency, Compliance)
   - Problem Statement (from stakeholder pain points)
   - Opportunity (e.g., new market, improved loss ratio)

   **3. Investment Description & Options**:
   - Scope (In/Out)
   - **Options Analysis** (CRITICAL):
     - Option 0: Do Nothing (baseline)
     - Option 1: Minimal Compliance/Viable Solution
     - Option 2: Strategic Transformation (often recommended)
     - For EACH option:
       - Pros/Cons
       - High-level CapEx/OpEx
       - Benefits

   **4. Financial Analysis**:
   - **Cost-Benefit Analysis**: 5-year cash flow
   - **Metrics**: NPV, IRR, Payback, ROI
   - **Assumptions**: Discount rate, inflation, etc.

   **5. Risk & Solvency Impact**:
   - **Solvency II Capital Impact**:
     - Operational Risk (Article 258)
     - Underwriting Risk (Article 105)
     - Market/Credit Risk
     - Estimated SCR impact (reduction or increase)
   - **ORSA Integration**: Material change to risk profile?
   - **Key Project Risks**: Top risks from `risk-register.md`

   **6. Implementation Plan & Governance**:
   - Roadmap & Milestones
   - Governance Structure (Sponsor, Steering Co)
   - Change Management

6. **Ensure complete traceability**:

   Every element must link back to stakeholder analysis:

   ```
   Stakeholder Driver D-1 (CFO: Reduce expense ratio)
     → Strategic Context: Efficiency driver
       → Financial Analysis: Benefit B-1: £2M annual opex savings
         → Risk/Solvency: Operational risk capital reduction
   ```

7. **Include decision framework**:
   - **Recommendation**: Which option to proceed with?
   - **Rationale**: Why this option?
   - **Next Steps**: If approved, what happens next?
     - Typically: `/arckit.requirements` to define detailed requirements

**CRITICAL - Auto-Populate Document Control Fields**:

Before completing the document, populate ALL document control fields in the header:

### Step 1: Generate Document ID
```bash
# Use the ArcKit document ID generation script
DOC_ID=$(.arckit/scripts/bash/generate-document-id.sh "${PROJECT_ID}" "SOBC" "1.0")
# Example output: ARC-001-SOBC-v1.0
```

### Step 2: Populate Required Fields

**Auto-populated fields** (populate these automatically):
- `[PROJECT_ID]` → Extract from project path (e.g., "001" from "projects/001-project-name")
- `[VERSION]` → Start with "1.0" for new documents
- `[DATE]` / `[YYYY-MM-DD]` → Current date in YYYY-MM-DD format
- `[DOCUMENT_TYPE_NAME]` → "Strategic Outline Business Case (SOBC)"
- `[CLASSIFICATION]` → Default to "INTERNAL" or "CONFIDENTIAL"
- `[STATUS]` → "DRAFT" for new documents

**User-specified fields** (must be confirmed with user):
- `[OWNER]` → Who owns this business case? (typically from stakeholder RACI matrix)
- `[REVIEWED_BY]` → Who will review? (mark as "PENDING" if not yet reviewed)
- `[APPROVED_BY]` → Who must approve? (mark as "PENDING" if not yet approved)

8. **Write the output**:
   - Create or update `projects/NNN-project-name/sobc.md`
   - Use project directory structure (create if doesn't exist)
   - File name pattern: `sobc.md` (Strategic Outline Business Case)


**IMPORTANT - Populate Metadata Footer**:
Before completing, populate the metadata footer at the end of the generated document with:
- `[DATE]` → Current date in YYYY-MM-DD format
- `[VERSION]` → Current ArcKit version read from `.arckit/VERSION` (always use the exact value in that file—do not hardcode or fall back)
- `[PROJECT_NAME]` → The actual project name
- `[AI_MODEL]` → The AI model used (e.g., "claude-sonnet-4-5-20250929", "gpt-4", "gemini-pro")

Example populated footer:
```markdown
**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2025-10-29
**ArcKit Version**: v{ARC_VERSION}
**Project**: Claims Transformation (Project 001)
**Model**: claude-sonnet-4-5-20250929
```


9. **Use appropriate language**:
   - Use insurance terminology (GWP, Combined Ratio, Loss Ratio, Expense Ratio, SCR, ORSA).
   - Link to stakeholder analysis for credibility.

10. **Flag uncertainties**:
    - Mark estimates as "Rough Order of Magnitude (ROM)"
    - Flag where more analysis needed
    - Note dependencies on external factors

## Output Format

Provide:
1. **Location**: `projects/NNN-project-name/sobc.md`
2. **Summary**:
   - "Created Strategic Outline Business Case (SOBC) for [project name]"
   - "Analyzed [X] options against [Y] stakeholder goals"
   - "Recommended: Option [X] - [name]"
   - "Estimated investment: £[X]M over 3 years"
   - "Expected benefits: £[X]M over 3 years"
   - "Solvency II Impact: £[X]M SCR reduction/increase"
3. **Next steps**:
   - "Present to Investment Committee for go/no-go decision"
   - "If approved: Run `/arckit.requirements` to define detailed requirements"
   - "After requirements: Create OBC (Outline Business Case) with refined costs"

## Common Patterns

**Pattern 1: Claims Transformation**:
- Strategic: Reduce claims leakage, improve customer experience
- Financial: High upfront cost, significant claims savings
- Solvency: Reduced operational risk, potentially reduced reserving risk

**Pattern 2: Digital Distribution**:
- Strategic: Growth, new channels
- Financial: Revenue uplift, marketing costs
- Solvency: Increased underwriting risk volume, but diversified

**Pattern 3: Regulatory Compliance (e.g., IFRS 17)**:
- Strategic: Mandatory compliance
- Financial: Cost avoidance (fines), no direct revenue
- Solvency: Improved governance, data quality

## Error Handling

If stakeholder analysis doesn't exist:
- **DO NOT proceed** with SOBC
- Tell user: "SOBC requires stakeholder analysis to link benefits to stakeholder goals. Please run `/arckit.stakeholders` first."

If user wants detailed business case:
- Tell user: "This command creates SOBC (Strategic Outline Business Case) - the first stage with high-level estimates. After `/arckit.requirements`, create OBC (Outline Business Case) with refined costs."

## Template Reference

Use the template at `.arckit/templates/sobc-template.md` as the structure. Fill in with:
- Stakeholder analysis data (goals, drivers, outcomes, conflicts)
- Architecture principles (strategic alignment)
- User's project description
- Insurance sector best practices

## Output Instructions

**CRITICAL - Token Efficiency**:

To avoid exceeding Claude Code's 32K token output limit, you MUST use the following strategy:

### 1. Generate SOBC Document

Create the comprehensive, executive-ready Strategic Outline Business Case following the insurance appraisal template structure.

### 2. Write Directly to File

**Use the Write tool** to create `projects/[PROJECT]/sobc.md` with the complete SOBC document.

**DO NOT** output the full document in your response. This would exceed token limits.

### 3. Show Summary Only

After writing the file, show ONLY a concise summary:

```markdown
## SOBC Complete ✅

**Project**: [Project Name]
**File Created**: `projects/[PROJECT]/sobc.md`

### SOBC Summary

**Strategic Context**:
- Strategic Alignment: [Brief summary]
- Problem/Opportunity: [Brief summary]

**Investment**:
- Recommended Option: [Name]
- Total Investment: £[X]M
- NPV: £[X]M | IRR: [X]% | Payback: [X] months

**Solvency Impact**:
- SCR Impact: +/- £[X]M
- Risk Profile: [Material/Non-material change]

**Next Steps**:
- [List 2-3 next steps]
```

Generate the SOBC now, write to file using Write tool, and show only the summary above.
