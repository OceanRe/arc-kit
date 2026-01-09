---
description: Create comprehensive risk register using Solvency 2 risk categories for insurance/enterprise
tags: [risk, solvency2, insurance, enterprise, erm, orsa]
---

# Enterprise Risk Register (Solvency 2 Aligned)

You are helping create a comprehensive risk register following **Solvency 2** risk management principles.

## About Solvency 2 Risk Management

**Solvency 2** is the regulatory framework for insurance companies providing risk-based capital and governance requirements:
- **Pillar 1**: Quantitative requirements (SCR/MCR)
- **Pillar 2**: Governance, risk management, ORSA
- **Pillar 3**: Reporting and disclosure

**Key Articles**: Article 44 (Risk Management), Article 45 (ORSA), Article 258 (Operational Risk)

## User Input

```text
$ARGUMENTS
```

## Instructions

1. **Check prerequisites**:
   - MANDATORY: Stakeholder analysis exists (`projects/*/stakeholder-drivers.md`)
   - If not, tell user to run `/prompts:arckit.stakeholders` first

2. **Identify risks across Solvency 2 categories**:

   **UNDERWRITING** (Article 105): Premium, reserve, catastrophe, lapse risk
   **MARKET** (Article 105): Interest rate, equity, property, currency, spread
   **CREDIT** (Article 105): Counterparty default, reinsurer credit
   **OPERATIONAL** (Article 258): Process, people, systems, external events
   **LIQUIDITY** (Article 260): Cash flow, asset liquidity, funding
   **STRATEGIC**: Business model, competition, transformation
   **REPUTATIONAL**: Brand, customer trust, conduct

3. **For each risk**:
   - Risk ID, Category, Title, Description
   - Inherent assessment (Likelihood 1-5 × Impact 1-5)
   - Controls and residual assessment
   - 4Ts response (Tolerate/Treat/Transfer/Terminate)
   - SCR impact estimate
   - Risk owner (from stakeholder RACI)
   - KRIs and monitoring

4. **Load template**: `.arckit/templates/insurance-risk-register-template.md`

5. **Output**: `projects/[project]/risk-register.md`

## Impact Scale (Insurance)

- **1 - Negligible**: < £1M, < 5pp SCR
- **2 - Minor**: £1-5M, 5-10pp SCR
- **3 - Moderate**: £5-20M, 10-20pp SCR
- **4 - Major**: £20-50M, 20-40pp SCR
- **5 - Catastrophic**: > £50M, > 40pp SCR

## Related Commands

- `/prompts:arckit.stakeholders` - Identify risk owners
- `/prompts:arckit.sobc` - Business case uses risk register
- `/prompts:arckit.secure` - Security assessment

Generate the Solvency 2 aligned risk register now.
