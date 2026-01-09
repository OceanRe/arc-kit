# Insurance Risk Register (Solvency 2 Aligned)

## Document Information

| Field | Value |
|-------|-------|
| **Document ID** | ARC-[PROJECT_ID]-RISK-v[VERSION] |
| **Project** | [PROJECT_NAME] (Project [PROJECT_ID]) |
| **Document Type** | Risk Register (Solvency 2 Aligned) |
| **Classification** | [CONFIDENTIAL / INTERNAL / PUBLIC] |
| **Version** | [VERSION] |
| **Status** | [DRAFT / FINAL / ARCHIVED] |
| **Date** | [YYYY-MM-DD] |
| **Owner** | [OWNER_NAME_AND_ROLE] |

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| [VERSION] | [DATE] | ArcKit AI | Initial creation from `/arckit.risk` command |

---

## Executive Summary

### Risk Profile Overview

**Total Risks Identified:** [X] risks across 7 Solvency 2 risk categories

| Risk Level | Inherent | Residual | Change |
|------------|----------|----------|--------|
| **Critical** (20-25) | X | Y | ↓ Z% |
| **High** (13-19) | X | Y | ↓ Z% |
| **Medium** (6-12) | X | Y | ↓ Z% |
| **Low** (1-5) | X | Y | ↓ Z% |
| **TOTAL** | XXX | YYY | ↓ ZZ% |

### Solvency 2 Risk Category Distribution

| Category | Count | Avg Inherent | Avg Residual | Control Effectiveness | Capital Impact |
|----------|-------|--------------|--------------|----------------------|----------------|
| **UNDERWRITING** | X | 12.5 | 8.2 | 34% reduction | [SCR Impact] |
| **MARKET** | X | 10.3 | 6.5 | 37% reduction | [SCR Impact] |
| **CREDIT** | X | 11.8 | 7.1 | 40% reduction | [SCR Impact] |
| **OPERATIONAL** | X | 15.2 | 9.8 | 36% reduction | [SCR Impact] |
| **LIQUIDITY** | X | 14.5 | 10.2 | 30% reduction | [SCR Impact] |
| **STRATEGIC** | X | 13.1 | 8.5 | 35% reduction | N/A |
| **REPUTATIONAL** | X | 11.0 | 7.0 | 36% reduction | N/A |

### Overall Risk Assessment

**Overall Residual Risk Score:** [YYY]/500
**Risk Reduction from Controls:** [ZZ]% reduction from inherent risk
**Risk Profile Status:** ✅ Within Risk Appetite | ⚠️ Approaching Limits | ❌ Exceeds Risk Appetite

### Solvency Capital Requirement (SCR) Impact

**Estimated SCR Impact from Identified Risks:**

| Risk Module | Base SCR | Project Impact | Revised SCR |
|-------------|----------|----------------|-------------|
| Underwriting Risk | £[X]M | +/- £[Y]M | £[Z]M |
| Market Risk | £[X]M | +/- £[Y]M | £[Z]M |
| Credit Risk | £[X]M | +/- £[Y]M | £[Z]M |
| Operational Risk | £[X]M | +/- £[Y]M | £[Z]M |
| **Total SCR** | **£[X]M** | **+/- £[Y]M** | **£[Z]M** |

### Risks Exceeding Appetite

**Number of risks exceeding organizational appetite:** [N] risks

| Risk ID | Title | Category | Score | Appetite | Excess | Escalation |
|---------|-------|----------|-------|----------|--------|------------|
| R-001 | ... | OPERATIONAL | 20 | 12 | +8 | Board/Risk Committee approval required |

### Top 5 Critical Risks Requiring Immediate Attention

1. **R-001** (OPERATIONAL, Critical 20): [Title] - Owner: [Name] - Status: [Status]
2. **R-002** (UNDERWRITING, Critical 25): [Title] - Owner: [Name] - Status: [Status]
3. **R-003** (MARKET, High 16): [Title] - Owner: [Name] - Status: [Status]
4. **R-004** (CREDIT, High 15): [Title] - Owner: [Name] - Status: [Status]
5. **R-005** (LIQUIDITY, High 15): [Title] - Owner: [Name] - Status: [Status]

---

## A. Risk Appetite Framework

### Enterprise Risk Appetite Statement

**Risk Appetite Statement:**
[Organization name] accepts a [conservative/moderate/aggressive] level of risk in pursuit of its strategic objectives. We seek to optimize the risk-return profile while maintaining:
- Solvency ratio above [X]% of SCR
- Strong credit ratings (minimum [A-])
- Stable earnings with volatility below [X]%
- Protection of policyholder interests

### Risk Appetite by Category

| Risk Category | Appetite Level | Quantitative Limit | Qualitative Statement |
|---------------|---------------|-------------------|----------------------|
| **UNDERWRITING** | Medium | Combined ratio < 98% | Accept risks within core expertise |
| **MARKET** | Low | VaR < £[X]M (99.5%) | Conservative investment strategy |
| **CREDIT** | Low | Max single exposure < [X]% | High quality counterparties only |
| **OPERATIONAL** | Very Low | Op risk losses < £[X]M/year | Zero tolerance for control failures |
| **LIQUIDITY** | Very Low | Liquidity coverage > 150% | Always meet obligations |
| **STRATEGIC** | Medium | ROE volatility < [X]% | Pursue growth within strategy |
| **REPUTATIONAL** | Very Low | NPS > [X] | Protect brand and trust |

### Risk Tolerance Thresholds

| Threshold | Definition | Action Required |
|-----------|------------|-----------------|
| **Green Zone** | Within appetite | Normal monitoring |
| **Amber Zone** | 80-100% of appetite | Enhanced monitoring, management action |
| **Red Zone** | Exceeds appetite | Escalation to Board, immediate action |

---

## B. Risk Matrix Visualization

### Inherent Risk Matrix (Before Controls)

**Likelihood × Impact Matrix - Inherent Risk Positions**

```
LIKELIHOOD ↑
     5 | Almost Certain |       | R-003 | R-007 |       | R-001 |
       |                |-------|-------|-------|-------|-------|
     4 | Likely         |       |       | R-005 | R-009 |       |
       |                |-------|-------|-------|-------|-------|
     3 | Possible       | R-006 |       | R-002 |       | R-004 |
       |                |-------|-------|-------|-------|-------|
     2 | Unlikely       |       | R-008 |       |       |       |
       |                |-------|-------|-------|-------|-------|
     1 | Rare           |       |       | R-010 |       |       |
       |________________|_______|_______|_______|_______|_______|
                            1       2       3       4       5
                        Negligible Minor  Moderate Major Catastrophic
                                      IMPACT →
```

**Risk Zones:**
- 🟥 **Critical (20-25)**: R-001, R-003 - Immediate escalation required
- 🟧 **High (13-19)**: R-002, R-004, R-005, R-007, R-009 - Senior management attention
- 🟨 **Medium (6-12)**: R-006, R-008 - Management monitoring
- 🟩 **Low (1-5)**: R-010 - Routine monitoring

### Residual Risk Matrix (After Controls)

**Likelihood × Impact Matrix - Residual Risk Positions**

```
LIKELIHOOD ↑
     5 | Almost Certain |       |       |       |       |       |
       |                |-------|-------|-------|-------|-------|
     4 | Likely         |       |       | R-003 |       |       |
       |                |-------|-------|-------|-------|-------|
     3 | Possible       | R-006 | R-001 | R-002 | R-005 |       |
       |                |-------|-------|-------|-------|-------|
     2 | Unlikely       |       | R-008 | R-007 | R-009 |       |
       |                |-------|-------|-------|-------|-------|
     1 | Rare           |       | R-010 |       | R-004 |       |
       |________________|_______|_______|_______|_______|_______|
                            1       2       3       4       5
                        Negligible Minor  Moderate Major Catastrophic
                                      IMPACT →
```

---

## C. Top 10 Risks (Ranked by Residual Score)

| Rank | ID | Title | Category | Inherent | Residual | Owner | Status | Response | SCR Impact |
|------|----|-------|----------|----------|----------|-------|--------|----------|------------|
| 1 | R-001 | [Risk title] | OPERATIONAL | 25 | 16 | CRO | In Progress | Treat | £[X]M |
| 2 | R-002 | [Risk title] | UNDERWRITING | 20 | 12 | Chief Underwriting Officer | In Progress | Treat | £[X]M |
| 3 | R-003 | [Risk title] | MARKET | 20 | 16 | CIO | Open | Treat | £[X]M |
| 4 | R-004 | [Risk title] | CREDIT | 16 | 9 | CFO | Monitoring | Transfer | £[X]M |
| 5 | R-005 | [Risk title] | LIQUIDITY | 15 | 12 | CFO | In Progress | Treat | £[X]M |
| 6 | R-006 | [Risk title] | OPERATIONAL | 12 | 6 | COO | Monitoring | Tolerate | £[X]M |
| 7 | R-007 | [Risk title] | STRATEGIC | 15 | 8 | CEO | In Progress | Treat | N/A |
| 8 | R-008 | [Risk title] | REPUTATIONAL | 9 | 4 | CCO | Closed | Tolerate | N/A |
| 9 | R-009 | [Risk title] | MARKET | 12 | 8 | CIO | In Progress | Treat | £[X]M |
| 10 | R-010 | [Risk title] | OPERATIONAL | 6 | 3 | CRO | Monitoring | Tolerate | £[X]M |

---

## D. Detailed Risk Register

### Risk R-001: [Risk Title]

**Category:** OPERATIONAL (Solvency 2 Article 258)
**Status:** In Progress
**Risk Owner:** [Name, Role] (from Stakeholder RACI: Accountable)
**Action Owner:** [Name, Role]

#### Risk Identification

**Risk Description:**
[Detailed description of the risk - 2-3 sentences explaining what the risk is]

**Root Cause:**
[What underlying issue creates this risk?]

**Risk Drivers:**
- [Driver 1 - e.g., System complexity]
- [Driver 2 - e.g., Process immaturity]
- [Driver 3 - e.g., Resource constraints]

**Trigger Events:**
- [Event 1 that would cause this risk to materialize]
- [Event 2 that would cause this risk to materialize]
- [Event 3 that would cause this risk to materialize]

**Consequences if Realized:**
- **Financial Impact:** £[X]M potential loss
- **SCR Impact:** Increase in operational risk capital by £[X]M
- **Regulatory Impact:** [Potential supervisory action]
- **Operational Impact:** [Business disruption description]
- **Reputational Impact:** [Brand/trust damage]

**Affected Stakeholders:**
- **[Stakeholder 1]** (from stakeholder-drivers.md): [How they are affected]
- **[Stakeholder 2]**: [How they are affected]
- **Policyholders**: [Impact on customer service/claims]

**Related Business Objectives:**
- [Stakeholder Goal G-001]: [How this risk threatens the goal]
- [Strategic objective]: [How this risk threatens the objective]

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 5 - Almost Certain | [Why this is almost certain to happen without controls] |
| **Impact** | 5 - Catastrophic | [Why the impact would be catastrophic] |
| **Inherent Risk Score** | **25** (Critical) | 5 × 5 = 25 |

**Risk Zone:** 🟥 Critical (20-25)

#### Current Controls and Mitigations

**Preventive Controls:**
1. **[Control 1]**: [Description of control]
   - Owner: [Name]
   - Effectiveness: Weak | Adequate | **Strong**
   - Testing: [Last tested date, result]

2. **[Control 2]**: [Description of control]
   - Owner: [Name]
   - Effectiveness: Weak | **Adequate** | Strong
   - Testing: [Last tested date, result]

**Detective Controls:**
1. **[Control 3]**: [Description - e.g., monitoring, reporting]
   - Owner: [Name]
   - Effectiveness: [Rating]
   - Frequency: [How often monitored]

**Overall Control Effectiveness:** Adequate (reduces risk from 25 to 16)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | [Why still likely even with controls] |
| **Impact** | 4 - Major | [Why impact is still major] |
| **Residual Risk Score** | **16** (High) | 4 × 4 = 16 |

**Risk Zone:** 🟧 High (13-19)
**Risk Reduction:** 36% reduction from inherent (25 → 16)

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:**
[Why this response was chosen - e.g., "Risk exceeds appetite but can be mitigated through additional controls at reasonable cost"]

**Alternative Responses Considered:**
- **Tolerate**: Rejected - Risk score too high, exceeds appetite
- **Transfer**: Considered - Cyber insurance obtained as secondary response
- **Terminate**: Not viable - Activity essential to insurance operations

#### Solvency 2 Capital Impact

**SCR Module:** Operational Risk
**SCR Impact Assessment:**

| Scenario | Probability | Loss Amount | Expected Loss | Capital Required |
|----------|-------------|-------------|---------------|------------------|
| Base case | 50% | £[X]M | £[Y]M | £[Z]M |
| Stress case | 10% | £[X]M | £[Y]M | £[Z]M |
| Extreme case | 1% | £[X]M | £[Y]M | £[Z]M |

**Alignment with ORSA:**
- This risk is included in ORSA scenario analysis
- Forward-looking assessment conducted
- Capital buffer adequate: [Yes/No]

#### Risk Appetite Assessment

**Organizational Risk Appetite for OPERATIONAL risks:** Low (Score ≤ 8)
**Current Residual Risk Score:** 16 (High)
**Assessment:** ❌ **Exceeds Appetite** by 8 points (100% over threshold)

**Justification:**
[Why proceeding despite exceeding appetite - e.g., "Strategic imperative, Board approval obtained, additional mitigations planned"]

**Escalation Required:** Yes - Board Risk Committee approval required

#### Action Plan

**Additional Mitigations Needed:**

1. **[Mitigation Action 1]**
   - Description: [Detailed action]
   - Owner: [Name, Role]
   - Due Date: [Date]
   - Cost: £[X]
   - Expected Impact: Reduce likelihood from 4 to 2

2. **[Mitigation Action 2]**
   - Description: [Detailed action]
   - Owner: [Name, Role]
   - Due Date: [Date]
   - Cost: £[X]
   - Expected Impact: Reduce impact from 4 to 3

**Target Residual Risk After Mitigations:**
- Target Likelihood: 2 (Unlikely)
- Target Impact: 3 (Moderate)
- Target Score: 6 (Medium) ✅ Within appetite (≤ 8)

**Key Risk Indicators (KRIs):**
| KRI | Threshold | Current | Status |
|-----|-----------|---------|--------|
| [KRI 1] | [Limit] | [Value] | [🟢/🟡/🔴] |
| [KRI 2] | [Limit] | [Value] | [🟢/🟡/🔴] |

**Monitoring Plan:**
- **Frequency:** Monthly review in Risk Committee
- **Escalation Triggers:**
  - Score increases by 3+ points
  - KRI breaches threshold
  - Mitigation actions delayed > 2 weeks

---

### Risk R-002: [Underwriting Risk Title]

**Category:** UNDERWRITING (Solvency 2 Article 105)
**Status:** Open
**Risk Owner:** Chief Underwriting Officer
**Action Owner:** [Name, Role]

#### Risk Description
[Description of underwriting risk - e.g., adverse claims experience, pricing inadequacy]

#### Solvency 2 Underwriting Risk Sub-Categories

| Sub-Category | Applicable | Assessment |
|--------------|------------|------------|
| Premium Risk | [Yes/No] | [Assessment] |
| Reserve Risk | [Yes/No] | [Assessment] |
| Catastrophe Risk | [Yes/No] | [Assessment] |
| Lapse Risk | [Yes/No] | [Assessment] |

[Continue with full risk template structure as above]

---

## E. Risk Category Analysis

### UNDERWRITING Risks (Solvency 2 Article 105)

**Definition:** Risk of loss arising from inadequate pricing, underwriting decisions, or adverse claims experience.

**Total UNDERWRITING Risks:** [X]
**Average Inherent Score:** 14.2 (High)
**Average Residual Score:** 9.8 (Medium)
**Control Effectiveness:** 31% reduction

**SCR Module Impact:** £[X]M

**Sub-Categories:**
- **Premium Risk:** Risk from fluctuation in timing, frequency, and severity of insured events
- **Reserve Risk:** Risk from fluctuation in timing and amount of claims settlements
- **Catastrophe Risk:** Risk of extreme or exceptional events (nat cat, man-made)
- **Lapse Risk:** Risk from changes in lapse rates

**Risk List:**
- R-002: [Title] - Residual: 12 (Medium)
- R-011: [Title] - Residual: 8 (Medium)

**Key Controls:**
- Underwriting guidelines and authority limits
- Pricing adequacy reviews
- Reserving methodology and actuarial sign-off
- Reinsurance program
- Claims management process

**Category Risk Profile:** ⚠️ Concerning - Monitor claims development closely

---

### MARKET Risks (Solvency 2 Article 105)

**Definition:** Risk of loss from movements in market prices of assets, liabilities, and financial instruments.

**Total MARKET Risks:** [X]
**Average Inherent Score:** 12.5 (High)
**Average Residual Score:** 8.0 (Medium)
**Control Effectiveness:** 36% reduction

**SCR Module Impact:** £[X]M

**Sub-Categories:**
- **Interest Rate Risk:** Sensitivity to changes in interest rates
- **Equity Risk:** Sensitivity to equity market movements
- **Property Risk:** Sensitivity to property values
- **Currency Risk:** Sensitivity to exchange rate movements
- **Spread Risk:** Sensitivity to credit spreads
- **Concentration Risk:** Exposure concentrations

**Risk List:**
- R-003: [Title] - Residual: 10 (Medium)
- R-009: [Title] - Residual: 8 (Medium)

**Key Controls:**
- Investment policy and limits
- Asset-liability matching
- Duration management
- Currency hedging
- Diversification requirements
- Stress testing program

**Category Risk Profile:** ✅ Acceptable - Within investment policy limits

---

### CREDIT Risks (Solvency 2 Article 105)

**Definition:** Risk of loss from counterparty default or deterioration in credit quality.

**Total CREDIT Risks:** [X]
**Average Inherent Score:** 11.0 (Medium)
**Average Residual Score:** 7.5 (Medium)
**Control Effectiveness:** 32% reduction

**SCR Module Impact:** £[X]M

**Counterparty Categories:**
- Reinsurers
- Banks and financial institutions
- Brokers and intermediaries
- Policyholders (premium receivables)
- Investment counterparties

**Risk List:**
- R-004: [Title] - Residual: 9 (Medium)
- R-012: [Title] - Residual: 6 (Medium)

**Key Controls:**
- Credit limits by counterparty
- Credit rating requirements
- Collateral arrangements
- Concentration limits
- Credit monitoring and watchlist
- Reinsurer security policy

**Category Risk Profile:** ✅ Acceptable - Strong counterparty quality

---

### OPERATIONAL Risks (Solvency 2 Article 258)

**Definition:** Risk of loss from inadequate or failed internal processes, people, systems, or external events.

**Total OPERATIONAL Risks:** [X]
**Average Inherent Score:** 15.0 (High)
**Average Residual Score:** 10.0 (Medium)
**Control Effectiveness:** 33% reduction

**SCR Module Impact:** £[X]M

**Sub-Categories:**
- **Process Risk:** Internal process failures
- **People Risk:** Human error, fraud, key person dependency
- **Systems Risk:** IT failures, cyber attacks, data breaches
- **External Events:** Natural disasters, supplier failures, regulatory changes
- **Legal Risk:** Litigation, contract disputes
- **Compliance Risk:** Regulatory breaches, sanctions

**Risk List:**
- R-001: [Title] - Residual: 16 (High) ⚠️ Exceeds appetite
- R-006: [Title] - Residual: 6 (Medium)
- R-010: [Title] - Residual: 3 (Low)

**Key Controls:**
- Business continuity planning
- IT disaster recovery
- Cyber security program (SOC2/ISO 27001)
- Internal controls framework
- Compliance monitoring
- Fraud prevention
- Vendor management

**Category Risk Profile:** ⚠️ Concerning - R-001 exceeds appetite, mitigation underway

---

### LIQUIDITY Risks (Solvency 2 Article 260)

**Definition:** Risk that the insurer cannot meet its obligations as they fall due without incurring unacceptable losses.

**Total LIQUIDITY Risks:** [X]
**Average Inherent Score:** 12.0 (Medium)
**Average Residual Score:** 8.0 (Medium)
**Control Effectiveness:** 33% reduction

**Not included in SCR but monitored separately**

**Liquidity Metrics:**
| Metric | Limit | Current | Status |
|--------|-------|---------|--------|
| Liquidity Coverage Ratio | >150% | [X]% | [🟢/🟡/🔴] |
| Cash and equivalents | >£[X]M | £[Y]M | [🟢/🟡/🔴] |
| Liquid assets / liabilities | >[X]% | [Y]% | [🟢/🟡/🔴] |

**Risk List:**
- R-005: [Title] - Residual: 12 (Medium)

**Key Controls:**
- Liquidity policy and limits
- Cash flow forecasting
- Liquidity buffer requirements
- Asset liability management
- Contingency funding plan
- Stress testing (liquidity)

**Category Risk Profile:** ✅ Acceptable - Strong liquidity position

---

### STRATEGIC Risks

**Definition:** Risk from business decisions, changes in business environment, or failure to adapt to industry changes.

**Total STRATEGIC Risks:** [X]
**Average Inherent Score:** 13.5 (High)
**Average Residual Score:** 9.0 (Medium)
**Control Effectiveness:** 33% reduction

**Not included in SCR (Pillar 1) but considered in ORSA (Pillar 2)**

**Strategic Risk Themes:**
- Market and competitive position
- Business model sustainability
- Digital transformation
- Regulatory change
- Climate change and ESG
- Talent and capability

**Risk List:**
- R-007: [Title] - Residual: 8 (Medium)

**Key Controls:**
- Strategic planning process
- Market and competitor analysis
- Scenario planning
- Board strategy reviews
- Performance monitoring

**Category Risk Profile:** ✅ Acceptable - Aligned with strategic plan

---

### REPUTATIONAL Risks

**Definition:** Risk of damage to brand, trust, or stakeholder relationships affecting business value.

**Total REPUTATIONAL Risks:** [X]
**Average Inherent Score:** 11.0 (Medium)
**Average Residual Score:** 6.5 (Medium)
**Control Effectiveness:** 41% reduction

**Not included in SCR but significant business impact**

**Reputation Risk Sources:**
- Customer complaints and service failures
- Product mis-selling or conduct issues
- Data breaches and privacy failures
- Social media and press coverage
- Environmental, Social, Governance (ESG) issues
- Executive misconduct

**Risk List:**
- R-008: [Title] - Residual: 4 (Low)

**Key Controls:**
- Conduct risk framework
- Customer complaints handling
- Media monitoring and response
- Crisis management plan
- ESG policy and reporting
- Brand protection

**Category Risk Profile:** ✅ Acceptable - Strong brand management

---

## F. Risk Ownership Matrix

**Risk Ownership Distribution by Solvency 2 Key Function:**

| Role | Solvency 2 Function | Owned Risks | Critical | High | Medium | Low | Total Score |
|------|---------------------|-------------|----------|------|--------|-----|-------------|
| CRO | Risk Management | R-001, R-006, R-010 | 0 | 1 | 2 | 0 | 25 |
| Chief Underwriting Officer | N/A | R-002, R-011 | 0 | 1 | 1 | 0 | 20 |
| CFO | N/A | R-004, R-005 | 0 | 1 | 1 | 0 | 21 |
| CIO | N/A | R-003, R-009 | 0 | 1 | 1 | 0 | 18 |
| Chief Actuary | Actuarial Function | [Risks] | 0 | 0 | 0 | 0 | 0 |
| Compliance Officer | Compliance Function | [Risks] | 0 | 0 | 0 | 0 | 0 |
| Internal Audit | Internal Audit Function | N/A (3rd line) | N/A | N/A | N/A | N/A | N/A |

**Solvency 2 Key Functions Engagement:**
- ✅ Risk Function: Reviews all risks, owns operational risks
- ✅ Actuarial Function: Reviews underwriting and reserving risks
- ✅ Compliance Function: Reviews regulatory and conduct risks
- ✅ Internal Audit: Independent assurance on risk management

---

## G. Solvency 2 Integration

### ORSA Alignment

**How this Risk Register feeds into Own Risk and Solvency Assessment (ORSA):**

| ORSA Component | Risk Register Input |
|----------------|---------------------|
| Risk profile assessment | All risks with Solvency 2 categories |
| Capital needs assessment | SCR impact by risk |
| Continuous compliance | Risks affecting solvency position |
| Forward-looking view | Strategic and emerging risks |
| Stress and scenario testing | Risk scenarios and impacts |

### Pillar 2 Governance Requirements

**Solvency 2 Article 44 - Risk Management:**
- ✅ Risk management system covers all material risks
- ✅ Risks identified, measured, monitored, managed, reported
- ✅ Risk management integrated into decision-making

**Solvency 2 Article 45 - ORSA:**
- ✅ Regular assessment of overall solvency needs
- ✅ Continuous compliance with capital requirements
- ✅ Deviation from assumptions underlying SCR

### Regulatory Reporting

**Risks feeding into regulatory reports:**

| Report | Risks Included | Frequency |
|--------|---------------|-----------|
| RSR (Regular Supervisory Report) | All material risks | Annual |
| SFCR (Solvency and Financial Condition Report) | Risk profile summary | Annual |
| QRTs (Quantitative Reporting Templates) | SCR risks | Quarterly/Annual |
| ORSA Report | All risks + forward view | Annual / Trigger |

---

## H. 4Ts Response Framework Summary

**Risk Response Distribution:**

| Response | Count | % | Total Risk Score | Key Examples |
|----------|-------|---|------------------|--------------|
| **TOLERATE** | 3 | 30% | 13 (Low) | R-006, R-008, R-010 - Within appetite |
| **TREAT** | 5 | 50% | 64 (High) | R-001, R-002, R-003, R-005, R-007 - Active mitigation |
| **TRANSFER** | 1 | 10% | 9 (Medium) | R-004 - Reinsurance/insurance obtained |
| **TERMINATE** | 1 | 10% | 8 (Medium) | R-011 - High-risk product withdrawn |
| **TOTAL** | 10 | 100% | 94 | |

---

## I. Prioritized Action Plan

### Priority 1: URGENT (Critical Risks or Significant Appetite Exceedance)

| Priority | Action | Risk(s) Addressed | Owner | Due Date | Cost | Expected Impact | Status |
|----------|--------|-------------------|-------|----------|------|-----------------|--------|
| 1 | [Action 1] | R-001 (OPERATIONAL) | CRO | [Date] | £[X]K | Reduce from 16 to 8 | In Progress |
| 2 | [Action 2] | R-003 (MARKET) | CIO | [Date] | £[X]K | Reduce from 16 to 10 | Not Started |

### Priority 2: HIGH (High Risks Within Appetite)

| Priority | Action | Risk(s) Addressed | Owner | Due Date | Cost | Expected Impact | Status |
|----------|--------|-------------------|-------|----------|------|-----------------|--------|
| 3 | [Action 3] | R-002 (UNDERWRITING) | CUO | [Date] | £[X]K | Reduce from 12 to 8 | Planning |
| 4 | [Action 4] | R-005 (LIQUIDITY) | CFO | [Date] | £[X]K | Reduce from 12 to 6 | Not Started |

---

## J. Monitoring and Review Framework

### Review Schedule

| Risk Level | Review Frequency | Reviewed By | Escalated To | Report Format |
|------------|------------------|-------------|--------------|---------------|
| **Critical (20-25)** | Weekly | Risk Owner + CRO | Board Risk Committee | Dashboard + narrative |
| **High (13-19)** | Monthly | Risk Owner | Risk Committee | Dashboard |
| **Medium (6-12)** | Quarterly | Risk Owner | CRO | Exception report |
| **Low (1-5)** | Annually | Action Owner | Risk Owner | Status update |

### Key Risk Indicators (KRIs)

**Leading Indicators:**
- [KRI 1: e.g., "New business volumes > budget by 20% → increases underwriting risk"]
- [KRI 2: e.g., "Claims frequency trend increase → indicates reserving risk"]
- [KRI 3: e.g., "Investment portfolio duration mismatch → indicates market risk"]

**Lagging Indicators:**
- [KRI 4: e.g., "Combined ratio > 100% → underwriting loss realized"]
- [KRI 5: e.g., "Operational loss > £XM → operational risk realized"]

### Reporting Requirements

**Monthly** (Board Risk Committee):
- Risk dashboard with heat map
- Top 10 risks by residual score
- Risk appetite compliance
- KRI status

**Quarterly** (Executive Committee):
- Full risk register review
- Risk trend analysis
- Action plan progress
- Emerging risks assessment

**Annually** (Board and Regulators):
- ORSA report
- SFCR risk profile
- Risk strategy review
- Risk appetite calibration

---

## Appendix A: Risk Assessment Scales

### Likelihood Scale (1-5)

| Score | Rating | Probability | Description |
|-------|--------|-------------|-------------|
| 1 | Rare | < 2% | Once in 50 years, exceptional circumstances |
| 2 | Unlikely | 2-10% | Once in 10-50 years, known but not expected |
| 3 | Possible | 10-25% | Once in 4-10 years, has happened before |
| 4 | Likely | 25-50% | Once in 2-4 years, expected to occur |
| 5 | Almost Certain | > 50% | Once a year or more, will happen |

### Impact Scale (1-5) - Insurance Context

| Score | Rating | Financial Impact | Solvency Impact | Regulatory Impact | Description |
|-------|--------|------------------|-----------------|-------------------|-------------|
| 1 | Negligible | < £1M | < 5pp SCR | No regulatory interest | Minor, easily absorbed |
| 2 | Minor | £1-5M | 5-10pp SCR | Informal supervisory query | Manageable within tolerances |
| 3 | Moderate | £5-20M | 10-20pp SCR | Formal supervisory letter | Management attention required |
| 4 | Major | £20-50M | 20-40pp SCR | Supervisory action plan | Threatens objectives |
| 5 | Catastrophic | > £50M | > 40pp SCR | Intervention/enforcement | Threatens viability |

### Risk Score Matrix

| Score Range | Risk Level | Color | Action Required |
|-------------|------------|-------|-----------------|
| 20-25 | Critical | 🟥 Red | Immediate Board escalation |
| 13-19 | High | 🟧 Orange | Risk Committee attention |
| 6-12 | Medium | 🟨 Yellow | Management monitoring |
| 1-5 | Low | 🟩 Green | Routine monitoring |

---

## Appendix B: Solvency 2 Risk Categories Reference

| Category | Solvency 2 Article | SCR Module | Description |
|----------|-------------------|------------|-------------|
| Underwriting | Article 105 | Underwriting risk | Premium, reserve, catastrophe, lapse |
| Market | Article 105 | Market risk | Interest rate, equity, property, currency, spread |
| Credit | Article 105 | Counterparty default | Reinsurance, derivatives, receivables |
| Operational | Article 258 | Operational risk | Process, people, systems, external |
| Liquidity | Article 260 | N/A (monitoring) | Cash flow, funding, asset liquidity |
| Strategic | N/A | N/A (ORSA) | Business model, competition, environment |
| Reputational | N/A | N/A (ORSA) | Brand, trust, stakeholder relationships |

---

## Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Chief Risk Officer** | [Name] | | |
| **Chief Actuary** | [Name] | | |
| **Chief Financial Officer** | [Name] | | |
| **Board Risk Committee Chair** | [Name] | | |

---

## Next Steps

1. **Immediate Actions** (This Week):
   - [ ] Escalate R-001 (OPERATIONAL) to Board Risk Committee
   - [ ] Initiate priority 1 mitigations
   - [ ] Update KRI dashboards

2. **Short-term Actions** (This Month):
   - [ ] Integrate risk register updates into ORSA
   - [ ] Complete quarterly risk review
   - [ ] Update SCR impact analysis

3. **Medium-term Actions** (This Quarter):
   - [ ] Risk appetite recalibration review
   - [ ] Emerging risks horizon scan
   - [ ] Internal audit of risk management

---

**Generated by**: ArcKit `/arckit.risk` command
**Generated on**: [DATE]
**ArcKit Version**: [VERSION]
**Project**: [PROJECT_NAME]
**Model**: [AI_MODEL]
