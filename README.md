# ArcKit - Enterprise Architecture Governance Toolkit

![ArcKit - Enterprise Architecture Governance Toolkit](docs/assets/arckit-banner-light.svg)

**Build better enterprise architecture through structured governance, vendor procurement, and design review workflows.**

ArcKit is a toolkit for enterprise architects that transforms architecture governance from scattered documents into a systematic, AI-assisted workflow for:
- 🏛️ Establishing and enforcing architecture principles
- 👥 Analyzing stakeholder drivers, goals, and outcomes
- 🛡️ Risk management (Solvency II / ISO 31000)
- 💼 Business case justification (Strategic Outline Business Case)
- 📋 Creating comprehensive requirements documents
- 🗄️ Data modeling with ERD, GDPR compliance, and data governance
- 🔬 Technology research with build vs buy analysis (web search powered)
- 🗺️ Strategic planning with Wardley Mapping
- 📊 Generating visual architecture diagrams (Mermaid)
- 🤝 Managing vendor RFP and selection processes
- ✅ Conducting formal design reviews (HLD/DLD)
- 🔧 ServiceNow service management design
- 🔗 Maintaining requirements traceability

---

## Quick Start

### Installation

Install ArcKit CLI:

```bash
# Install with pip
pip install git+https://github.com/tractorjuice/arc-kit.git

# Or with uv
uv tool install arckit-cli --from git+https://github.com/tractorjuice/arc-kit.git

# Or run without installing
uvx --from git+https://github.com/tractorjuice/arc-kit.git arckit init my-project
```

**Latest Release**: [v0.9.1](https://github.com/tractorjuice/arc-kit/releases/tag/v0.9.1)

### Initialize a Project

```bash
# Create a new architecture governance project
arckit init payment-modernization --ai claude

# Or use OpenAI Codex CLI
arckit init payment-modernization --ai codex

# Or initialize in current directory
arckit init . --ai claude
```

### Start Using ArcKit

```bash
cd payment-modernization
claude  # or your chosen AI assistant

# Inside your AI assistant, use ArcKit commands:
/arckit.principles Create principles for a financial services company
/arckit.requirements Build a payment processing system...
/arckit.sow Generate RFP for vendor selection
```

---

## Why ArcKit?

### Problem: Architecture Governance is Broken

Traditional enterprise architecture suffers from:
- ❌ Scattered documents across tools (Word, Confluence, PowerPoint)
- ❌ Inconsistent governance enforcement
- ❌ Manual vendor evaluation with bias
- ❌ Lost traceability between requirements and design
- ❌ Stale documentation that doesn't match reality

### Solution: Structured, AI-Assisted Governance

ArcKit provides:
- ✅ **Template-Driven Quality**: Comprehensive templates ensure nothing is forgotten
- ✅ **Systematic Workflows**: Clear processes from requirements → procurement → design review
- ✅ **AI Assistance**: Let AI handle document generation, you focus on decisions
- ✅ **Enforced Traceability**: Automatic gap detection and coverage analysis
- ✅ **Version Control**: Git-based workflow for all architecture artifacts

---

## Enterprise & Insurance Compliance

ArcKit includes dedicated commands for enterprise and insurance regulatory compliance:
- `/arckit.soc2` — Assess SOC 2 Trust Service Criteria (Security, Availability, Confidentiality, Processing Integrity, Privacy).
- `/arckit.iso27001` — Assess ISO 27001:2022 controls across Organizational, People, Physical, and Technological domains.
- `/arckit.solvency2` — Perform Solvency II Pillar 2 governance assessments.
- `/arckit.orsa` — Generate Own Risk and Solvency Assessment (ORSA) reports.
- `/arckit.secure` — Generate Secure by Design artefacts covering ISO 27001 and SOC 2 controls.
- `/arckit.dpia` — General Data Protection Regulation (GDPR) impact assessments.

---

## The ArcKit Workflow

ArcKit guides you through the enterprise architecture lifecycle:

### Phase 0: Project Planning
**`/arckit.plan`** → Create project plan with timeline, phases, and gates

Visualize your entire project delivery:
- Standard delivery phases (Discovery → Alpha → Beta → Live)
- Mermaid Gantt chart with timeline, dependencies, and milestones
- Workflow diagram showing gates and decision points
- Tailored timeline based on project complexity
- Integration of all ArcKit commands into schedule
- Gate approval criteria for governance

### Phase 1: Establish Governance
**`/arckit.principles`** → Create enterprise architecture principles

Define your organisation's architecture standards:
- Cloud strategy (AWS/Azure/GCP)
- Security frameworks (Zero Trust, compliance)
- Technology standards
- FinOps and cost governance

### Phase 2: Stakeholder Analysis
**`/arckit.stakeholders`** → Analyze stakeholder drivers, goals, and outcomes

**Do this BEFORE business case** to understand who cares about the project and why:
- Identify all stakeholders (internal and external)
- Document underlying drivers (strategic, operational, financial, compliance, risk, personal)
- Map drivers to SMART goals
- Map goals to measurable outcomes
- Create Stakeholder → Driver → Goal → Outcome traceability
- Identify conflicts and synergies
- Define engagement and communication strategies

### Phase 3: Risk Assessment
**`/arckit.risk`** → Create comprehensive risk register

**Do this BEFORE business case** to identify and assess risks systematically:
- Aligned with Solvency II risk categories (Underwriting, Market, Credit, Operational, Liquidity)
- Assess inherent risk (before controls) and residual risk (after controls)
- Apply 4Ts response framework (Tolerate, Treat, Transfer, Terminate)
- Link every risk to stakeholder from RACI matrix
- Monitor risk appetite compliance
- Feed into SOBC Management Case Part E

### Phase 4: Business Case Justification
**`/arckit.sobc`** → Create Strategic Outline Business Case (SOBC)

**Do this BEFORE requirements** to justify investment and secure approval:
- Standard 5-case model (Strategic, Economic, Commercial, Financial, Management)
- Analyze strategic options (Do Nothing, Minimal, Balanced, Comprehensive)
- Map benefits to stakeholder goals (complete traceability)
- Provide high-level cost estimates (Rough Order of Magnitude)
- Economic appraisal (ROI range, payback period, NPV)
- Procurement and funding strategy
- Governance and risk management (uses risk register)
- Enable go/no-go decision BEFORE detailed requirements work

### Phase 5: Define Requirements
**`/arckit.requirements`** → Document comprehensive requirements

Create detailed requirements **informed by stakeholder goals** (if SOBC approved):
- Business requirements with rationale
- Functional requirements with acceptance criteria
- Non-functional requirements (performance, security, scalability, compliance)
- Integration requirements (upstream/downstream systems)
- Data requirements (DR-xxx)
- Success criteria and KPIs

### Phase 5.5: Data Modeling
**`/arckit.data-model`** → Create comprehensive data model with ERD

Create data model based on Data Requirements (DR-xxx):
- Visual Entity-Relationship Diagram (ERD) using Mermaid
- Detailed entity catalog with attributes, types, validation rules
- PII identification and GDPR compliance
- Data governance matrix (business owners, stewards, custodians)
- CRUD matrix showing component access patterns
- Data integration mapping (upstream sources, downstream consumers)
- Data quality framework with measurable metrics
- Requirements traceability (DR-xxx → Entity → Attribute)

### Phase 5.7: Data Protection Impact Assessment
**`/arckit.dpia`** → Generate DPIA for GDPR compliance

**MANDATORY for high-risk processing** - assess privacy risks before technology selection:
- Standard screening criteria (sensitive data, large scale, vulnerable subjects, AI/ML, etc.)
- Auto-populated from data model (entities, PII, special category data, lawful basis)
- Risk assessment focused on impact on individuals (privacy harm, discrimination)
- Data subject rights implementation checklist (SAR, deletion, portability)
- Children's data assessment (age verification, parental consent)
- AI/ML algorithmic processing assessment (bias, explainability, human oversight)
- Regulator prior consultation flagging for high residual risks
- International transfer safeguards (SCCs, BCRs, adequacy decisions)
- Bidirectional links to risk register (DPIA-xxx risk IDs)
- Links mitigations to Secure by Design security controls

### Phase 6: Technology Research
**`/arckit.research`** → Research technology, services, and products

Research available solutions to meet requirements with build vs buy analysis:
- Dynamic category detection from requirements (authentication, payments, databases, etc.)
- Commercial SaaS options with pricing, reviews, and ratings (WebSearch)
- Open source alternatives with GitHub stats and community maturity
- Total Cost of Ownership (TCO) comparison (3-year)
- Build vs Buy vs Adopt recommendations
- Vendor shortlisting for deeper evaluation
- Integration with Wardley mapping (evolution positioning)
- Feeds into SOBC Economic Case (cost data, options analysis)

### Phase 7: Strategic Planning with Wardley Mapping
**`/arckit.wardley`** → Create strategic Wardley Maps

Visualize strategic positioning with:
- Component evolution analysis (Genesis → Custom → Product → Commodity)
- Build vs Buy decision framework
- Vendor comparison and procurement strategy
- Evolution predictions and strategic gameplay

### Phase 7.5: Strategic Roadmap
**`/arckit.roadmap`** → Create multi-year architecture roadmap

Create strategic roadmap for multi-year transformation programs:
- **Multi-year timeline**: 3-5 year roadmap with Mermaid Gantt chart
- **Strategic themes**: Cloud migration, data modernization, security & compliance, DevOps transformation
- **Capability evolution**: Maturity progression from L1 (Initial) to L5 (Optimized) over time
- **Investment planning**: CAPEX/OPEX budget by financial year, ROI projections, benefits realization
- **Governance framework**: ARB monthly, Programme Board monthly, Steering Committee quarterly
- **Dependencies**: Mermaid flowchart showing initiative sequencing and critical path
- **Success metrics**: Cloud adoption %, technical debt reduction, deployment frequency, time to market
- **Traceability**: Links roadmap themes to stakeholder drivers, architecture principles, requirements

**Roadmap feeds into**: `/arckit.plan` for detailed phase execution, `/arckit.sobc` for investment business case, `/arckit.backlog` for prioritized user stories.

### Phase 7.7: Architecture Decision Records
**`/arckit.adr`** → Document architectural decisions

Create Architecture Decision Records (ADRs) following MADR v4.0 format:
- **Decision metadata**: Sequential numbering (ADR-001, ADR-002), status (Proposed/Accepted/Superseded)
- **Stakeholder RACI**: Deciders (accountable), Consulted (SMEs, two-way), Informed (one-way communication)
- **Context and problem statement**: Why this decision is needed, business/technical/regulatory drivers
- **Decision drivers**: Technical forces (performance, security, scalability), business forces (cost, time), compliance forces (SOC2, ISO 27001, GDPR)
- **Options analysis**: Minimum 2-3 options plus "Do Nothing" baseline, each with pros/cons, cost (CAPEX/OPEX/TCO), Wardley evolution stage
- **Y-Statement**: Structured justification - "In the context of X, facing Y, we decided for Z to achieve A, accepting B"
- **Consequences**: Positive (benefits, capabilities), Negative (trade-offs, technical debt), Neutral (training, infrastructure), Risks and mitigations
- **Validation**: How implementation will be verified (design reviews, code reviews, testing, monitoring)
- **Traceability**: Links to requirements, principles, stakeholders, research, Wardley maps, diagrams, risk register

### Phase 8: Vendor Procurement (if needed)
**`/arckit.sow`** → Generate Statement of Work (RFP)

Create RFP-ready documents with:
- Scope of work and deliverables
- Technical requirements
- Vendor qualifications
- Evaluation criteria
- Contract terms

**`/arckit.evaluate`** → Create vendor evaluation framework

Set up systematic scoring:
- Technical evaluation criteria (100 points)
- Cost evaluation methodology
- Reference check templates
- Decision matrix

**`/arckit.evaluate`** (compare mode) → Compare vendor proposals

Side-by-side analysis of:
- Technical approaches
- Cost breakdowns
- Risk assessments
- Value propositions

### Phase 9: Design Review
**`/arckit.hld-review`** → Review High-Level Design

Validate designs against:
- Architecture principles compliance
- Requirements coverage
- Security and compliance
- Scalability and resilience
- Operational readiness

**`/arckit.dld-review`** → Review Detailed Design

Implementation-ready validation:
- Component specifications
- API contracts (OpenAPI)
- Database schemas
- Security implementation
- Test strategy

### Phase 10: Sprint Planning
**`/arckit.backlog`** → Generate prioritised product backlog

Transform requirements into sprint-ready user stories:
- Convert requirements (BR/FR/NFR/INT/DR) to standard user stories
- Multi-factor prioritization (MoSCoW + risk + value + dependencies)
- Organise into sprint plan with capacity balancing
- Generate traceability matrix (requirements → stories → sprints)
- Export to Jira/Azure DevOps (CSV) or custom tools (JSON)

### Phase 11: ServiceNow Service Management Design
**`/arckit.servicenow`** → Generate ServiceNow service design

Bridge architecture to operations:
- CMDB design (derived from architecture diagrams)
- SLA definitions (derived from NFRs)
- Incident management design
- Change management plan
- Monitoring and alerting plan
- Service transition plan

### Phase 12: Traceability
**`/arckit.traceability`** → Generate traceability matrix

Ensure complete coverage:
- Requirements → Design mapping
- Design → Test mapping
- Gap analysis and orphan detection
- Change impact tracking

### Phase 13: Quality Assurance
**`/arckit.analyze`** → Comprehensive governance quality analysis

Periodically assess governance quality across all artifacts:
- Architecture principles compliance
- Requirements coverage and traceability
- Stakeholder alignment verification
- Risk management completeness
- Design review quality
- Documentation completeness and quality
- Gap identification and recommendations

**When to use**: Run periodically (before milestones, design reviews, or procurement decisions) to identify gaps and ensure governance standards are maintained.

### Phase 14: Compliance Assessment
**`/arckit.soc2`** → SOC 2 Assessment

Assess compliance with Trust Service Criteria:
- Security (Common Criteria)
- Availability
- Confidentiality
- Processing Integrity
- Privacy

**`/arckit.iso27001`** → ISO 27001 Assessment

Assess compliance with ISO 27001:2022 controls:
- Organizational controls
- People controls
- Physical controls
- Technological controls

**`/arckit.solvency2`** → Solvency II Pillar 2 Governance

Assess governance and risk management requirements for insurers:
- System of Governance
- Key Functions (Risk, Compliance, Audit, Actuarial)
- Risk Management System
- ORSA Process

**`/arckit.orsa`** → ORSA Reporting

Generate Own Risk and Solvency Assessment report structure:
- Business Strategy
- Risk Profile
- Solvency Needs
- Stress Testing

**`/arckit.secure`** → Secure by Design Assessment

General security assessment covering:
- ISO 27001 / SOC 2 Controls
- Cloud Security Principles
- GDPR Security Requirements
- Threat Modeling

### Phase 15: Project Story & Reporting
**`/arckit.story`** → Generate comprehensive project story

Create narrative historical record with complete timeline analysis:
- **Timeline Analysis**: 4 visualization types (Gantt chart, linear flowchart, detailed table, phase duration pie chart)
- **Timeline Metrics**: Project duration, velocity, phase analysis, critical path identification
- **Complete Timeline**: All events from git log or file modification dates with days-from-start
- **8 Narrative Chapters**: Foundation → Business Case → Requirements → Research → Procurement → Design → Delivery → Compliance
- **Traceability Demonstration**: End-to-end chains with Mermaid diagrams showing stakeholder → goals → requirements → stories → sprints
- **Governance Achievements**: Showcase compliance (SOC2, ISO 27001), risk management, decision rationale
- **Strategic Context**: Wardley Map insights, build vs buy decisions, vendor selection rationale
- **Lessons Learned**: Pacing analysis, timeline deviations, recommendations for future projects
- **Comprehensive Appendices**: Artifact register, chronological activity log, DSM, command reference, glossary

**When to use**: At project milestones or completion to create shareable story for stakeholders, leadership, or portfolio reporting. Perfect for demonstrating systematic governance and ArcKit workflow value.

---

## Supported AI Agents

| Agent | Support | Notes |
|-------|---------|-------|
| [Claude Code](https://www.anthropic.com/claude-code) | ✅ | Recommended |
| [OpenAI Codex CLI](https://chatgpt.com/features/codex) | ✅ | ChatGPT Plus/Pro/Enterprise ([Setup Guide](.codex/README.md)) |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | ✅ | |

### Using with Codex CLI

For OpenAI Codex CLI users, commands use the `/prompts:` format:

```bash
# Set CODEX_HOME to use project-specific commands
export CODEX_HOME="$(pwd)/.codex"
codex --auto

# Then use ArcKit commands
/prompts:arckit.principles Create principles for financial services
/prompts:arckit.stakeholders Analyze stakeholders for cloud migration
/prompts:arckit.requirements Create comprehensive requirements
```

See [.codex/README.md](.codex/README.md) for full Codex CLI setup and usage.


## Project Structure

ArcKit creates this structure:

```
payment-modernization/
├── .arckit/
│   ├── memory/
│   │   └── architecture-principles.md    # Global principles
│   ├── scripts/
│   │   └── bash/                          # Automation scripts
│   └── templates/                         # Document templates
├── projects/
│   └── 001-payment-gateway/
│       ├── stakeholder-drivers.md         # Stakeholder analysis
│       ├── risk-register.md                # Risk register
│       ├── sobc.md                         # Strategic Outline Business Case
│       ├── requirements.md                 # Comprehensive requirements
│       ├── data-model.md                   # Data model with ERD, GDPR compliance
│       ├── wardley-maps/                   # Strategic Wardley Maps
│       │   ├── current-state.md            # Current architecture positioning
│       │   ├── future-state.md             # Target architecture vision
│       │   ├── gap-analysis.md             # Current vs future comparison
│       │   └── procurement-strategy.md     # Build vs buy decisions
│       ├── sow.md                          # Statement of Work (RFP)
│       ├── evaluation-criteria.md          # Vendor evaluation framework
│       ├── vendors/
│       │   ├── acme-corp/
│       │   │   ├── proposal.pdf
│       │   │   ├── scoring.md
│       │   │   ├── hld-v1.md
│       │   │   └── reviews/
│       │   │       └── hld-v1-review.md
│       │   ├── beta-systems/
│       │   │   └── ...
│       │   └── comparison.md
│       ├── servicenow-design.md            # Service management design
│       ├── traceability-matrix.md
│       └── final/
│           ├── selected-vendor.md
│           ├── approved-hld.md
│           └── dld/
└── .claude/commands/                      # AI assistant commands
```

---

## Available Commands

### Core Commands

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.principles` | Establish architecture governance | `memory/architecture-principles.md` |
| `/arckit.stakeholders` | Analyze stakeholder drivers, goals, and outcomes | `projects/XXX/stakeholder-drivers.md` |
| `/arckit.risk` | Create comprehensive risk register | `projects/XXX/risk-register.md` |
| `/arckit.sobc` | Create Strategic Outline Business Case | `projects/XXX/sobc.md` |
| `/arckit.requirements` | Define comprehensive requirements | `projects/XXX/requirements.md` |
| `/arckit.platform-design` | Design multi-sided platform strategy | `projects/XXX/platform-design.md` |
| `/arckit.data-model` | Create data model with ERD, GDPR compliance, data governance | `projects/XXX/data-model.md` |
| `/arckit.research` | Research technology, services, and products with build vs buy analysis | `projects/XXX/research-findings.md` |
| `/arckit.wardley` | Create strategic Wardley Maps for build vs buy and procurement strategy | `projects/XXX/wardley-maps/{map-name}.md` |
| `/arckit.roadmap` | Create multi-year strategic architecture roadmap with capability evolution and governance | `projects/XXX/roadmap.md` |
| `/arckit.adr` | Document architectural decisions with MADR v4.0 format | `projects/XXX/decisions/ADR-{NUM}-{title}.md` |
| `/arckit.sow` | Generate vendor RFP | `projects/XXX/sow.md` |

### Sprint Planning

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.backlog` | Generate prioritised product backlog - convert requirements to user stories, organise into sprints | `projects/XXX/backlog.md` (+ optional CSV/JSON) |

### Vendor Management

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.evaluate` | Create evaluation framework and score vendors | `projects/XXX/evaluation-criteria.md`, `projects/XXX/vendor-comparison.md` |

### Design Review

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.hld-review` | Review high-level design | `projects/XXX/vendors/[vendor]/reviews/hld-review.md` |
| `/arckit.dld-review` | Review detailed design | `projects/XXX/vendors/[vendor]/reviews/dld-review.md` |

### Architecture Diagrams

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.diagram` | Generate visual architecture diagrams using Mermaid (C4, deployment, sequence, data flow) | `projects/XXX/diagrams/{diagram-type}-{name}.md` |

### Service Management

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.servicenow` | Generate ServiceNow service design (CMDB, SLAs, incident/change management, monitoring) | `projects/XXX/servicenow-design.md` |

### Traceability

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.traceability` | Generate traceability matrix | `projects/XXX/traceability-matrix.md` |

### Quality Assurance

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.analyze` | Comprehensive governance quality analysis across all artifacts | `projects/XXX/analysis-report.md` |

### Compliance Assessment

| Command | Purpose | Output |
|---------|---------|--------|
| `/arckit.soc2` | SOC 2 Trust Service Criteria assessment | `projects/XXX/soc2-assessment.md` |
| `/arckit.iso27001` | ISO 27001:2022 assessment | `projects/XXX/iso27001-assessment.md` |
| `/arckit.solvency2` | Solvency II Pillar 2 governance assessment | `projects/XXX/solvency2-governance.md` |
| `/arckit.orsa` | Own Risk and Solvency Assessment (ORSA) report | `projects/XXX/orsa-report.md` |
| `/arckit.secure` | Secure by Design assessment (ISO 27001 / SOC 2) | `projects/XXX/secure-by-design.md` |
| `/arckit.dpia` | Data Protection Impact Assessment (GDPR) | `projects/XXX/dpia.md` |

---

## Wardley Mapping for Strategic Architecture

ArcKit uses Wardley Maps to expose the strategic position of every component before you commit to a solution. The `/arckit.wardley` command produces ready-to-visualise maps that:
- Trace user needs through the supporting value chain so gaps and duplicated effort are obvious.
- Plot evolution from Genesis → Commodity to reveal when to build, buy, reuse, or retire capabilities.
- Feed procurement, vendor evaluation, and design reviews with shared situational awareness.

Maps are emitted in the Open Wardley Map format — paste them straight into [https://create.wardleymaps.ai](https://create.wardleymaps.ai) for a visual view. Full example outputs live in the public demos such as `arckit-test-project-v1-m365` (cloud migration strategy) and `arckit-test-project-v8-cabinet-office-genai` (cross-government GenAI platform).

---

## Architecture Diagrams with Mermaid

**ArcKit generates visual architecture diagrams using Mermaid for clear technical communication.**

### What are Architecture Diagrams?

Architecture diagrams visualize system structure, interactions, and deployment for:
- **Technical Communication**: Share architecture with stakeholders
- **Design Documentation**: Document current and future state
- **Vendor Evaluation**: Compare vendor technical approaches
- **Compliance**: Visualize security boundaries and PII handling

### Diagram Types

ArcKit supports 6 essential diagram types based on the C4 Model and enterprise architecture best practices:

| Diagram Type | Level | Purpose | When to Use |
|--------------|-------|---------|-------------|
| **C4 Context** | Level 1 | System in context with users and external systems | After requirements, to show system boundaries |
| **C4 Container** | Level 2 | Technical containers and technology choices | After HLD, for vendor review |
| **C4 Component** | Level 3 | Internal components within a container | After DLD, for implementation |
| **Deployment** | Infrastructure | Cloud resources and network topology | Compliance compliance, cost estimation |
| **Sequence** | Interaction | API flows and request/response patterns | Integration requirements, API design |
| **Data Flow** | Data | How data moves, PII handling, GDPR compliance | GDPR, DPIA requirements |

Use `/arckit.diagram` directly, or supply an explicit type such as `context`, `container`, `sequence`, or `dataflow`. Outputs bundle component inventories with Wardley evolution tags, built-in compliance scaffolding, network patterns, GDPR annotations, and traceability back to requirements and tests.

## ServiceNow Service Management Design

ArcKit turns architecture artefacts into an operations-ready ServiceNow pack. The `/arckit.servicenow` command builds:
- CMDB hierarchies, SLAs, and change risk straight from requirements, diagrams, and Wardley Maps.
- ITIL-aligned runbooks covering incident, change, monitoring, and transition activities.

---

## Documentation

Key references live in `docs/` and top-level guides:
- Quick tour: [docs/index.html](docs/index.html) mirrors the public landing page.
- Lifecycle visuals: [WORKFLOW-DIAGRAMS.md](WORKFLOW-DIAGRAMS.md) and [DEPENDENCY-MATRIX.md](DEPENDENCY-MATRIX.md) cover command flow and relationships.
- Core guides: [docs/principles.md](docs/principles.md), [docs/requirements.md](docs/requirements.md), [docs/procurement.md](docs/procurement.md), [docs/design-review.md](docs/design-review.md).
- Traceability: [docs/traceability.md](docs/traceability.md) documents end-to-end coverage patterns.

---

## Comparison to Other Tools

| Feature | ArcKit | Sparx EA | Ardoq | LeanIX | Confluence |
|---------|--------|----------|-------|--------|------------|
| **AI-Assisted** | ✅ | ❌ | ❌ | ❌ | ❌ |
| **Wardley Mapping** | ✅ | ❌ | ⚠️ Limited | ❌ | ❌ |
| **Version Control** | ✅ Git | ❌ | ❌ | ❌ | ⚠️ Limited |
| **Vendor RFP** | ✅ | ❌ | ❌ | ❌ | ⚠️ Manual |
| **Design Review Gates** | ✅ | ⚠️ Manual | ❌ | ❌ | ⚠️ Manual |
| **Traceability** | ✅ Automated | ⚠️ Manual | ✅ | ⚠️ Limited | ❌ |
| **Cost** | Free | $$$$ | $$$$ | $$$$ | $$ |
| **Learning Curve** | Low | High | Medium | Medium | Low |

---

## Requirements

- **Python 3.11+**
- **Git** (optional but recommended)
- **AI Coding Agent**: Claude Code, OpenAI Codex CLI, or Gemini CLI
- **uv** for package management: [Install uv](https://docs.astral.sh/uv/)

---

## Installation from Source

```bash
# Clone the repository
git clone https://github.com/tractorjuice/arc-kit.git
cd arc-kit

# Install in development mode
pip install -e .

# Run the CLI
arckit init my-project
```

---

## Documentation

Full guidance lives in `docs/` and the static site.
- Quick tour: [docs/index.html](docs/index.html) (mirrors the public landing page).
- Core guides: [docs/principles.md](docs/principles.md), [docs/requirements.md](docs/requirements.md), [docs/procurement.md](docs/procurement.md), [docs/design-review.md](docs/design-review.md).
- Reference packs: [WORKFLOW-DIAGRAMS.md](WORKFLOW-DIAGRAMS.md) and [DEPENDENCY-MATRIX.md](DEPENDENCY-MATRIX.md) cover lifecycle visualisations and the 35×35 command matrix.
- Traceability: [docs/traceability.md](docs/traceability.md) documents end-to-end requirements coverage.

## Relationship to Spec Kit

ArcKit is inspired by [Spec Kit](https://github.com/github/spec-kit) but targets a different audience:

| | Spec Kit | ArcKit |
|---|----------|--------|
| **Audience** | Product Managers, Developers | Enterprise Architects, Procurement |
| **Focus** | Feature development (0→1 code generation) | Architecture governance & vendor management |
| **Workflow** | Spec → Plan → Tasks → Code | Requirements → RFP → Design Review → Traceability |
| **Output** | Working code | Architecture documentation & governance |

---

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Areas we need help**:
- Integration with enterprise tools (Jira, Azure DevOps)
- Additional AI agent support
- Template improvements based on real-world usage
- Documentation and examples
- ServiceNow API integration for automated CI creation

---

## Troubleshooting

### Token Limit Error

If you see: `API Error: Claude's response exceeded the 32000 output token maximum`

**The Problem**: ArcKit generates large documents that can exceed Claude's 32K token output limit.

**⚠️ IMPORTANT**: Your Claude subscription plan determines the maximum tokens:
- 🔴 Free/Pro plans: **32K max** (cannot be increased)
- ✅ Team/Enterprise plans: Can increase to 64K via environment variable

**Solutions**:

1. **For Team/Enterprise plans** - Increase token limit:
   ```bash
   export CLAUDE_CODE_MAX_OUTPUT_TOKENS=64000
   ```

2. **For ALL plans** (including Free/Pro) - Use **Write tool strategy**:
   ```
   User: /arckit.requirements but write directly to file using Write tool, show me only a summary
   ```

   This tells Claude to use the Write tool to create the file (doesn't count toward output tokens) and only show you a summary.

**Which commands are affected?**
- 🔴 HIGH RISK: `/arckit.research`, `/arckit.sobc`, `/arckit.requirements`, `/arckit.data-model`, `/arckit.sow`
- 🟡 MEDIUM RISK: `/arckit.risk`, `/arckit.evaluation`, `/arckit.principles`

**See full guide**: [docs/TOKEN-LIMITS.md](docs/TOKEN-LIMITS.md)

### Common Issues

**Command not found**: Ensure Claude Code is installed and commands are loaded
```bash
# Check if .claude/commands/ directory exists
ls .claude/commands/
```

**Template not found**: Ensure you've run `/arckit.principles` first
```bash
# Check if templates exist
ls templates/
```

**Project creation fails**: Ensure you have an ArcKit repository initialized
```bash
# Initialize if needed
arckit init .
```

---

## Support

- **Issues**: [GitHub Issues](https://github.com/tractorjuice/arc-kit/issues)
- **Releases**: [GitHub Releases](https://github.com/tractorjuice/arc-kit/releases)
- **Latest Version**: [v0.9.1](https://github.com/tractorjuice/arc-kit/releases/tag/v0.9.1)

---

## License

MIT License - see [LICENSE](LICENSE) for details

---

## Acknowledgements

ArcKit is inspired by the methodology and patterns from [Spec Kit](https://github.com/github/spec-kit), adapted for enterprise architecture governance workflows.

---

<p align="center">
  <img src="docs/assets/ArcKit_Logo_Horizontal_Dark.svg" alt="ArcKit" height="40">
</p>

<p align="center">
  <strong>Built with ❤️ for enterprise architects who want systematic, AI-assisted governance.</strong>
</p>
