---
description: Create comprehensive risk register using Solvency 2 risk categories for insurance/enterprise
tags: [risk, solvency2, insurance, enterprise, erm, orsa]
---

# Enterprise Risk Register (Solvency 2 Aligned)

You are helping an enterprise architect create a comprehensive risk register following **Solvency 2** risk management principles and industry-standard Enterprise Risk Management (ERM) frameworks.

## About Solvency 2 Risk Management

**Solvency 2** is the EU/UK regulatory framework for insurance companies. It provides a comprehensive risk-based approach to capital requirements and governance:

- **Pillar 1**: Quantitative requirements (SCR/MCR capital)
- **Pillar 2**: Qualitative requirements (governance, risk management, ORSA)
- **Pillar 3**: Reporting and disclosure requirements

**Key Solvency 2 Risk Articles**:
- **Article 44**: Risk management requirements
- **Article 45**: Own Risk and Solvency Assessment (ORSA)
- **Article 258**: Operational risk management
- **Article 274**: Outsourcing requirements

**Risk Management Principles**:
- **4Ts Risk Response Framework**: Tolerate, Treat, Transfer, Terminate
- **Risk Assessment Methodology**: Likelihood × Impact for Inherent and Residual risk
- **Risk Appetite**: Amount of risk organization is prepared to accept/tolerate

## User Input

```text
$ARGUMENTS
```

## Instructions

This command creates a **comprehensive risk register** following Solvency 2 risk categories and integrates with ArcKit's stakeholder-driven workflow.

**When to use this:**
- **After**: `/arckit.stakeholders` (MANDATORY - every risk needs an owner)
- **Before**: `/arckit.sobc` (Business Case uses risk register)
- **Purpose**: Identify, assess, and manage project risks using Solvency 2 methodology

1. **Check for prerequisites**:
   - **MANDATORY**: Check if stakeholder analysis exists for this project
     - Read `.arckit/memory/` or `projects/*/stakeholder-drivers.md` to find it
     - If NO stakeholder analysis exists, STOP and tell user:
       "⚠️ Risk register requires stakeholder analysis. Run `/arckit.stakeholders` first to identify risk owners and affected parties."
   - **RECOMMENDED**: Check if architecture principles exist
   - **RECOMMENDED**: Check if organizational risk appetite exists

2. **Understand the request**: The user may be:
   - Creating initial risk register (most common)
   - Updating existing risk register with new risks
   - Reassessing risks after changes
   - Creating organizational risk appetite

3. **Determine project context**:
   - If user mentions "insurance", "insurer", "underwriting" → Use full Solvency 2 categories
   - If user mentions "financial services", "banking" → Use enterprise risk categories
   - If user mentions "enterprise", "corporate" → Use standard ERM categories
   - Check stakeholder analysis for context on project scale, complexity

4. **Read stakeholder analysis carefully**:
   - Extract risk owners from RACI matrix (Accountable = Risk Owner)
   - Extract affected stakeholders (who cares about which risks?)
   - Extract stakeholder concerns from conflict analysis (these ARE risks!)
   - Note: EVERY risk MUST have a risk owner from stakeholder analysis

5. **Identify risks across Solvency 2 categories**:

   Use these risk categories aligned to Solvency 2 framework:

   **UNDERWRITING Risks** (Solvency 2 Article 105):
   - Premium risk: Pricing inadequacy, adverse loss experience
   - Reserve risk: Reserving uncertainty, development patterns
   - Catastrophe risk: Natural catastrophes, man-made events
   - Lapse risk: Policy cancellations, lapses
   - Example: "Claims experience exceeds pricing assumptions by 20%"

   **MARKET Risks** (Solvency 2 Article 105):
   - Interest rate risk: Sensitivity to rate movements
   - Equity risk: Stock market exposure
   - Property risk: Real estate values
   - Currency risk: Foreign exchange exposure
   - Spread risk: Credit spread movements
   - Concentration risk: Single-name/sector exposure
   - Example: "10% equity market decline impacts investment portfolio"

   **CREDIT Risks** (Solvency 2 Article 105):
   - Counterparty default risk
   - Reinsurer credit risk
   - Broker/intermediary credit risk
   - Premium receivables
   - Example: "Major reinsurer downgrade affects recovery expectations"

   **OPERATIONAL Risks** (Solvency 2 Article 258):
   - Process failures: Manual errors, process breakdowns
   - People risks: Key person dependency, fraud, skills gaps
   - Systems risks: IT failures, cyber attacks, data breaches
   - External events: Supplier failures, regulatory changes
   - Legal/compliance risk: Regulatory breaches, litigation
   - Example: "Cyber attack disrupts claims processing for 5 days"

   **LIQUIDITY Risks** (Solvency 2 Article 260):
   - Cash flow timing mismatches
   - Asset liquidity constraints
   - Funding risk
   - Example: "Large catastrophe claim exhausts liquid assets"

   **STRATEGIC Risks**:
   - Business model risks
   - Competitive position
   - Market/distribution changes
   - Digital transformation
   - Example: "New InsurTech competitor disrupts core market segment"

   **REPUTATIONAL Risks**:
   - Brand damage
   - Customer trust
   - Media/public perception
   - ESG/conduct issues
   - Example: "Claims handling delays damage brand reputation"

6. **For EACH risk identified, create comprehensive risk profile**:

   Use the template at `.arckit/templates/risk-register-template.md` and populate:

   **Risk Identification**:
   - **Risk ID**: R-001, R-002, R-003, etc. (sequential)
   - **Category**: UNDERWRITING | MARKET | CREDIT | OPERATIONAL | LIQUIDITY | STRATEGIC | REPUTATIONAL
   - **Risk Title**: Short, clear description (5-10 words)
   - **Risk Description**: Detailed description (2-3 sentences)
   - **Root Cause**: What underlying issue creates this risk?
   - **Trigger Events**: What events would cause this risk to materialize?
   - **Consequences**: Financial impact, SCR impact, regulatory impact
   - **Affected Stakeholders**: Link to stakeholder-drivers.md
   - **Related Objectives**: Business objectives threatened

   **Inherent Risk Assessment** (BEFORE controls):

   **Inherent Likelihood** (1-5 scale):
   - **1 - Rare**: < 2% probability, once in 50 years
   - **2 - Unlikely**: 2-10% probability, once in 10-50 years
   - **3 - Possible**: 10-25% probability, once in 4-10 years
   - **4 - Likely**: 25-50% probability, once in 2-4 years
   - **5 - Almost Certain**: > 50% probability, once a year or more

   **Inherent Impact** (1-5 scale - Insurance Context):
   - **1 - Negligible**: < £1M, < 5pp SCR impact, no regulatory interest
   - **2 - Minor**: £1-5M, 5-10pp SCR, informal supervisory query
   - **3 - Moderate**: £5-20M, 10-20pp SCR, formal supervisory letter
   - **4 - Major**: £20-50M, 20-40pp SCR, supervisory action plan
   - **5 - Catastrophic**: > £50M, > 40pp SCR, intervention/enforcement

   **Inherent Risk Score**: Likelihood × Impact (1-25)
   - **1-5**: Low (Green)
   - **6-12**: Medium (Yellow)
   - **13-19**: High (Orange)
   - **20-25**: Critical (Red)

   **Current Controls and Mitigations**:
   - Existing controls and effectiveness
   - Control owners
   - Evidence of effectiveness

   **Residual Risk Assessment** (AFTER controls)

   **Risk Response (4Ts Framework)**:
   - **TOLERATE**: Accept within appetite
   - **TREAT**: Mitigate through additional controls
   - **TRANSFER**: Insurance, reinsurance, hedging
   - **TERMINATE**: Stop the activity

   **Solvency Capital Requirement (SCR) Impact**:
   - Which SCR module affected?
   - Estimated capital impact
   - ORSA scenario relevance

   **Risk Ownership**:
   - Risk Owner (from stakeholder RACI)
   - Action Owner
   - Escalation Path

   **Key Risk Indicators (KRIs)**:
   - Leading indicators to monitor
   - Thresholds and alerts

7. **Generate comprehensive risk register** with these sections:

   **A. Executive Summary**:
   - Total risks by Solvency 2 category
   - Risk profile distribution (Critical/High/Medium/Low)
   - SCR impact summary
   - Risks exceeding appetite
   - Top 5 risks requiring attention

   **B. Risk Matrix Visualization** (5x5 grids for inherent and residual)

   **C. Top 10 Risks** (ranked by residual score)

   **D. Detailed Risk Register** (full risk profiles)

   **E. Risk Category Analysis** (by Solvency 2 category)

   **F. Risk Ownership Matrix** (by Key Function holders)

   **G. 4Ts Response Summary**

   **H. Risk Appetite Compliance**

   **I. ORSA Integration**:
   - Risks feeding into ORSA scenarios
   - Forward-looking risk assessment
   - Capital adequacy implications

   **J. Regulatory Reporting**:
   - Risks for RSR/SFCR
   - QRT implications
   - Supervisory notifications

   **K. Action Plan** (prioritized mitigations)

   **L. Monitoring Framework**:
   - Review frequency by risk level
   - KRI monitoring
   - Escalation criteria
   - Reporting requirements

8. **Ensure Solvency 2 alignment**:

   **Key Function Involvement**:
   - Risk Function: Reviews all risks
   - Actuarial Function: Reviews underwriting/reserving risks
   - Compliance Function: Reviews regulatory risks
   - Internal Audit: Independent assurance

   **ORSA Integration**:
   - Risks inform ORSA scenarios
   - Forward-looking assessment
   - Capital planning implications

   **Regulatory Alignment**:
   - Article 44 risk management requirements
   - Article 45 ORSA requirements
   - Article 258 operational risk requirements

9. **Write the output**:
   - Create `projects/NNN-project-name/risk-register.md`
   - Use insurance risk register template
   - Ensure SCR impact assessment for quantifiable risks




**IMPORTANT - Auto-Populate Document Information Fields**:

- `[PROJECT_ID]` → Extract from project path
- `[VERSION]` → Start with "1.0"
- `[DATE]` → Current date YYYY-MM-DD
- `ARC-[PROJECT_ID]-RISK-v[VERSION]` → Document ID
- `[PROJECT_NAME]` → Full project name
- `[OWNER_NAME_AND_ROLE]` → Document owner

### Generation Metadata Footer:
```markdown
**Generated by**: ArcKit `/arckit.risk` command
**Generated on**: {DATE}
**ArcKit Version**: [VERSION]
**Project**: {PROJECT_NAME} (Project {PROJECT_ID})
**Model**: [AI Model]
```


## Output Format

Provide:
1. **Location**: `projects/NNN-project-name/risk-register.md`
2. **Summary**:
   - "Created comprehensive risk register following Solvency 2 framework"
   - "Identified [X] risks across 7 Solvency 2 categories"
   - "Risk profile: [X] Critical, [Y] High, [Z] Medium, [W] Low"
   - "Estimated SCR impact: £[X]M across identified risks"
   - "All [X] risks have owners from stakeholder RACI matrix"
   - "[N] risks require immediate escalation"
3. **Top 3 Risks**:
   - "1. R-001 (OPERATIONAL, Critical 20): [Title] - Owner: [Name]"
   - "2. R-002 (UNDERWRITING, High 16): [Title] - Owner: [Name]"
   - "3. R-003 (MARKET, High 15): [Title] - Owner: [Name]"
4. **4Ts Distribution**:
   - "Tolerate: X% | Treat: Y% | Transfer: Z% | Terminate: W%"
5. **Next steps**:
   - "Review with CRO and Risk Committee"
   - "Integrate into ORSA scenario analysis"
   - "Update SCR calculations"
   - "Implement priority mitigations"

## Solvency 2 Compliance Checklist

Ensure the risk register demonstrates Solvency 2 compliance:

- ✅ **Article 44**: Risk management covers all material risks
- ✅ **Article 44**: Risks identified, measured, monitored, managed, reported
- ✅ **Article 45**: Risks inform ORSA forward-looking assessment
- ✅ **Article 258**: Operational risks systematically identified
- ✅ **Key Functions**: Risk, Actuarial, Compliance functions engaged
- ✅ **Governance**: Board/Risk Committee oversight documented

## Common Insurance Risk Patterns

**Pattern 1: Digital Transformation**:
- OPERATIONAL: Legacy system integration failure (High)
- OPERATIONAL: Cyber security breach (Critical)
- STRATEGIC: Digital competitor disruption (High)
- REPUTATIONAL: Customer data breach (Critical)

**Pattern 2: New Product Launch**:
- UNDERWRITING: Pricing inadequacy (High)
- UNDERWRITING: Unexpected claims patterns (High)
- OPERATIONAL: Process not ready for volume (Medium)
- REPUTATIONAL: Customer complaints (Medium)

**Pattern 3: Claims System Migration**:
- OPERATIONAL: System downtime (High)
- OPERATIONAL: Data migration errors (High)
- CREDIT: Premium collection disruption (Medium)
- REPUTATIONAL: Claims delays (High)

## Error Handling

If stakeholder analysis doesn't exist:
- **DO NOT proceed** - tell user to run `/arckit.stakeholders` first

If risks are critical (score 20-25):
- Flag: "⚠️ WARNING: [N] Critical risks identified. Immediate Board/Risk Committee escalation required."

If SCR impact is material:
- Flag: "⚠️ WARNING: Material SCR impact identified. ORSA update and regulatory notification may be required."

## Template Reference

Use the template at `.arckit/templates/risk-register-template.md` as the structure.

Generate a comprehensive, Solvency 2-compliant risk register that enables informed decision-making and effective risk management.
