# Enterprise Project Management AI Skills Framework (PM-AISF)

> **prjm-copilot-skill** — A reusable Project Management AI Skills Library for Microsoft Copilot Studio, Microsoft 365 Copilot, GitHub Copilot, Azure OpenAI, and future AI agents.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PMI Aligned](https://img.shields.io/badge/PMI-Aligned-blue.svg)](docs/governance-standards/)
[![Agile Ready](https://img.shields.io/badge/Agile-Ready-green.svg)](docs/best-practices/)

---

## Table of Contents

1. [Overview](#overview)
2. [Repository Structure](#repository-structure)
3. [Architecture](#architecture)
4. [Supported Platforms](#supported-platforms)
5. [Personas & Use Cases](#personas--use-cases)
6. [Quick Start](#quick-start)
7. [Agent Catalogue](#agent-catalogue)
8. [Skills Catalogue](#skills-catalogue)
9. [Prompt Engineering](#prompt-engineering)
10. [OpenAPI Manifests & Connectors](#openapi-manifests--connectors)
11. [Schemas](#schemas)
12. [Governance & Responsible AI](#governance--responsible-ai)
13. [PMI Alignment](#pmi-alignment)
14. [Agile Practices](#agile-practices)
15. [Security Requirements](#security-requirements)
16. [Agent Development Standards](#agent-development-standards)
17. [Integration Guide](#integration-guide)
18. [Contributing](#contributing)
19. [Versioning](#versioning)
20. [License](#license)

---

## Overview

The **Enterprise Project Management AI Skills Framework (PM-AISF)** is an open, version-controlled Center of Excellence for building, governing, and operating AI-powered project management capabilities across an enterprise.

It provides:

- **Reusable AI skills** — pre-built, tested, and governance-compliant prompt packages for common PM tasks.
- **Agent blueprints** — ready-to-deploy agent configurations for Copilot Studio and Azure OpenAI.
- **OpenAPI manifests** — machine-readable action definitions for Copilot Studio custom connectors.
- **JSON schemas** — structured data contracts for RAID logs, RAG reports, health dashboards, and executive views.
- **Sample datasets** — representative test data for prompt engineering, validation, and demos.
- **Governance standards** — responsible AI principles, auditability checklists, and PMI/Agile compliance guidance.

### Key Objectives

| Objective | Description |
|-----------|-------------|
| Standardisation | Uniform AI capabilities across all Copilot agents and platforms |
| Reusability | Prompt packages that can be dropped into any agent or workflow |
| Governance | PMI, Agile, and Responsible AI alignment out of the box |
| Extensibility | Open schema contracts and versioned APIs for custom integrations |
| Security | Zero-trust posture, data classification, and auditability built in |

---

## Repository Structure

```
prjm-copilot-skill/
│
├── agents/                          # Ready-to-deploy Copilot agent configurations
│   ├── executive-reporting-agent/
│   ├── project-health-agent/
│   ├── scrum-master-agent/
│   ├── raid-management-agent/
│   ├── steering-committee-agent/
│   └── requirements-agent/
│
├── skills/                          # Reusable AI skill definitions
│   ├── weekly-rag-reporting/
│   ├── project-health-assessment/
│   ├── raid-classification/
│   ├── stakeholder-communication/
│   ├── executive-escalation/
│   ├── sprint-status-review/
│   ├── retrospective-analysis/
│   ├── change-control-management/
│   ├── dependency-tracking/
│   ├── lessons-learned-analysis/
│   └── requirements-traceability-matrix/
│
├── prompts/                         # Prompt libraries by domain
│   ├── executive-reports/
│   ├── status-reports/
│   ├── stakeholder-updates/
│   ├── sprint-management/
│   ├── risk-management/
│   └── decision-logs/
│
├── manifests/                       # OpenAPI & Power Platform definitions
│   ├── copilot-studio-openapi/
│   ├── custom-connectors/
│   └── power-platform-actions/
│
├── schemas/                         # JSON Schema contracts
│   ├── rag-report-schema/
│   ├── raid-schema/
│   ├── project-health-schema/
│   └── executive-dashboard-schema/
│
├── examples/                        # Sample data and prompt demonstrations
│   ├── sample-projects/
│   ├── sample-raid-logs/
│   ├── sample-status-reports/
│   └── sample-prompts/
│
└── docs/                            # Documentation and standards
    ├── implementation-guide/
    ├── agent-creation-playbook/
    ├── prompt-engineering-guide/
    ├── governance-standards/
    └── best-practices/
```

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                  AI Skills Framework (PM-AISF)              │
│                                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐   │
│  │ Copilot  │  │ M365     │  │ GitHub   │  │  Azure   │   │
│  │ Studio   │  │ Copilot  │  │ Copilot  │  │  OpenAI  │   │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘  └────┬─────┘   │
│       │              │              │              │         │
│       └──────────────┴──────────────┴──────────────┘        │
│                             │                               │
│                     ┌───────▼────────┐                      │
│                     │  Skills Layer  │                      │
│                     │  (reusable)    │                      │
│                     └───────┬────────┘                      │
│                             │                               │
│          ┌──────────────────┼──────────────────┐            │
│          │                  │                  │            │
│   ┌──────▼──────┐  ┌────────▼──────┐  ┌───────▼──────┐    │
│   │   Prompts   │  │   Schemas     │  │  Manifests   │    │
│   │  (library)  │  │  (contracts)  │  │  (OpenAPI)   │    │
│   └─────────────┘  └───────────────┘  └──────────────┘    │
│                                                             │
│                   ┌─────────────────┐                      │
│                   │   Data Sources  │                      │
│                   │ M365 · ADO · SP │                      │
│                   │ Planner · Jira  │                      │
│                   └─────────────────┘                      │
└─────────────────────────────────────────────────────────────┘
```

### Layers

| Layer | Purpose |
|-------|---------|
| **Agent Layer** | Orchestrates skills; surfaces Copilot experiences |
| **Skills Layer** | Encapsulates domain logic; versioned and reusable |
| **Prompt Layer** | Natural-language instructions with structured outputs |
| **Schema Layer** | Typed contracts for data in/out of each skill |
| **Manifest Layer** | OpenAPI definitions for Copilot Studio actions |
| **Data Layer** | Connectors to enterprise systems of record |

---

## Supported Platforms

| Platform | Integration Type | Notes |
|----------|-----------------|-------|
| Microsoft Copilot Studio | Native agent + OpenAPI actions | Full support |
| Microsoft 365 Copilot | Declarative agent / plugin | Skills via M365 plugin manifest |
| GitHub Copilot | Instructions + extensions | `.github/copilot-instructions.md` patterns |
| Azure OpenAI | Assistants API + function calling | JSON schemas used as tool definitions |
| Microsoft Teams | Adaptive Cards + Bot Framework | Status reports rendered as cards |
| Microsoft Planner | Graph API connector | Task synchronisation |
| Project Online / PWA | OData connector | Portfolio health data |
| Azure DevOps | REST API connector | Sprint, work item, pipeline data |
| Jira | REST API connector | Issue and epic data |
| ServiceNow | REST API connector | Change and incident data |
| SharePoint | Graph API + search | Document and list data |
| Dataverse | Power Platform connector | Structured PM data store |
| Power Platform | Custom connectors + Power Automate | Workflow automation |

---

## Personas & Use Cases

| Persona | Primary Skills | Key Prompts |
|---------|---------------|-------------|
| **Project Manager** | weekly-rag-reporting, raid-classification, dependency-tracking | status-reports, risk-management |
| **Product Manager** | requirements-traceability-matrix, sprint-status-review | sprint-management, stakeholder-updates |
| **Scrum Master** | sprint-status-review, retrospective-analysis, lessons-learned-analysis | sprint-management |
| **Program Manager** | project-health-assessment, executive-escalation, dependency-tracking | executive-reports |
| **Delivery Manager** | change-control-management, raid-classification, project-health-assessment | status-reports, risk-management |
| **Executive Sponsor** | project-health-assessment, executive-escalation | executive-reports, decision-logs |
| **PMO Analyst** | weekly-rag-reporting, lessons-learned-analysis | status-reports, stakeholder-updates |

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/DaNether/PRJM-Copilot-Skill-Enterprise-Project-Management-AI-Skills-Framework-PM-AISF-.git
cd PRJM-Copilot-Skill-Enterprise-Project-Management-AI-Skills-Framework-PM-AISF-
```

### 2. Choose your integration path

**Path A — Copilot Studio Agent**

1. Open [Copilot Studio](https://copilotstudio.microsoft.com).
2. Create a new agent.
3. Import the OpenAPI manifest from `manifests/copilot-studio-openapi/`.
4. Copy the system prompt from the relevant `agents/<agent-name>/system-prompt.md`.
5. Add skills as topics using the prompt files from `prompts/`.

**Path B — Azure OpenAI Assistants**

1. Create an Assistant in [Azure OpenAI Studio](https://oai.azure.com).
2. Upload tool definitions from `schemas/` as JSON function definitions.
3. Use the system instruction from `agents/<agent-name>/system-prompt.md`.
4. Test with examples from `examples/sample-prompts/`.

**Path C — GitHub Copilot Instructions**

1. Copy relevant prompt files into `.github/copilot-instructions.md`.
2. Reference skill definitions to guide Copilot responses in your repository.

### 3. Validate with sample data

Use the files in `examples/` to test your agent configuration before production deployment.

---

## Agent Catalogue

| Agent | Description | Key Skills |
|-------|-------------|-----------|
| [executive-reporting-agent](agents/executive-reporting-agent/) | Generates C-suite and steering committee reports | executive-escalation, project-health-assessment, weekly-rag-reporting |
| [project-health-agent](agents/project-health-agent/) | Monitors project health and surfaces risks | project-health-assessment, raid-classification, dependency-tracking |
| [scrum-master-agent](agents/scrum-master-agent/) | Facilitates Scrum ceremonies and sprint management | sprint-status-review, retrospective-analysis, lessons-learned-analysis |
| [raid-management-agent](agents/raid-management-agent/) | Manages RAID logs and classification | raid-classification, change-control-management, dependency-tracking |
| [steering-committee-agent](agents/steering-committee-agent/) | Prepares steering committee packs and decision logs | executive-escalation, stakeholder-communication, decision-logs |
| [requirements-agent](agents/requirements-agent/) | Maintains requirements traceability and change control | requirements-traceability-matrix, change-control-management |

---

## Skills Catalogue

| Skill | Version | Description |
|-------|---------|-------------|
| [weekly-rag-reporting](skills/weekly-rag-reporting/) | 1.0 | Generates RAG-status weekly project reports |
| [project-health-assessment](skills/project-health-assessment/) | 1.0 | Scores and classifies project health across dimensions |
| [raid-classification](skills/raid-classification/) | 1.0 | Classifies and prioritises RAID log items |
| [stakeholder-communication](skills/stakeholder-communication/) | 1.0 | Drafts tailored stakeholder communications |
| [executive-escalation](skills/executive-escalation/) | 1.0 | Identifies escalation needs and drafts briefings |
| [sprint-status-review](skills/sprint-status-review/) | 1.0 | Summarises sprint progress and blockers |
| [retrospective-analysis](skills/retrospective-analysis/) | 1.0 | Structures retrospective findings and action items |
| [change-control-management](skills/change-control-management/) | 1.0 | Assesses change impact and drafts change requests |
| [dependency-tracking](skills/dependency-tracking/) | 1.0 | Maps and monitors inter-project dependencies |
| [lessons-learned-analysis](skills/lessons-learned-analysis/) | 1.0 | Captures and categorises lessons learned |
| [requirements-traceability-matrix](skills/requirements-traceability-matrix/) | 1.0 | Maintains RTM and gap analysis |

---

## Prompt Engineering

See [`docs/prompt-engineering-guide/`](docs/prompt-engineering-guide/) for detailed guidance.

### Prompt Design Principles

1. **Role definition** — Always begin with a clear persona and scope statement.
2. **Context injection** — Provide structured context (project name, dates, RAG status) before the task.
3. **Structured output** — Request JSON, Markdown table, or Adaptive Card output explicitly.
4. **Guardrails** — Include explicit constraints (word limits, classification bounds, tone).
5. **Validation hooks** — End prompts with a self-check instruction to improve output quality.

### Prompt Template Pattern

```
ROLE: You are a [persona] assisting a [audience].

CONTEXT:
- Project: {project_name}
- Reporting Period: {period}
- RAG Status: {rag_status}
- Key Facts: {facts}

TASK: {task_description}

OUTPUT FORMAT: {format_spec}

CONSTRAINTS:
- {constraint_1}
- {constraint_2}

SELF-CHECK: Before responding, verify that your output meets all constraints above.
```

---

## OpenAPI Manifests & Connectors

The `manifests/` directory contains:

- **`copilot-studio-openapi/`** — OpenAPI 3.0 YAML/JSON files importable directly into Copilot Studio as plugin actions.
- **`custom-connectors/`** — Power Platform custom connector definitions (JSON) for use in Power Automate and Power Apps.
- **`power-platform-actions/`** — Pre-built Power Automate flow templates that surface PM-AISF skills as reusable actions.

---

## Schemas

All data contracts follow [JSON Schema Draft 2020-12](https://json-schema.org/specification.html).

| Schema | File | Description |
|--------|------|-------------|
| RAG Report | `schemas/rag-report-schema/rag-report.schema.json` | Weekly status report structure |
| RAID Log | `schemas/raid-schema/raid.schema.json` | Risks, Assumptions, Issues, Dependencies |
| Project Health | `schemas/project-health-schema/project-health.schema.json` | Health dimension scoring |
| Executive Dashboard | `schemas/executive-dashboard-schema/executive-dashboard.schema.json` | Portfolio-level executive view |

---

## Governance & Responsible AI

See [`docs/governance-standards/`](docs/governance-standards/) for the full governance framework.

### Core Principles

| Principle | Implementation |
|-----------|---------------|
| **Transparency** | All AI-generated content is labelled; sources cited |
| **Accountability** | Human-in-the-loop required for escalations and change decisions |
| **Fairness** | Prompts reviewed for bias; diverse stakeholder representation |
| **Privacy** | No PII in prompts; data classification labels enforced |
| **Reliability** | Structured output validation; schema enforcement |
| **Security** | Least-privilege connectors; audit logging enabled |

### Auditability

- All agent interactions must be logged to a compliant audit store (e.g., Azure Monitor, Dataverse).
- Generated reports carry a metadata footer with model version, timestamp, and confidence indicators.
- RAID decisions require human sign-off before actioning.

---

## PMI Alignment

The framework maps to the **PMI PMBOK® Guide (7th Edition)** performance domains:

| PMBOK Domain | PM-AISF Capability |
|-------------|-------------------|
| Stakeholders | stakeholder-communication, executive-escalation |
| Team | retrospective-analysis, lessons-learned-analysis |
| Development Approach | sprint-status-review, change-control-management |
| Planning | dependency-tracking, requirements-traceability-matrix |
| Project Work | weekly-rag-reporting, project-health-assessment |
| Delivery | raid-classification, change-control-management |
| Measurement | project-health-assessment, executive-reporting-agent |
| Uncertainty | raid-classification, risk-management prompts |

Skills also align to **PMI Agile Practice Guide** and **PMI Code of Ethics and Professional Conduct**.

---

## Agile Practices

| Ceremony / Artefact | Supporting Skill | Supporting Prompt |
|--------------------|-----------------|------------------|
| Sprint Planning | sprint-status-review | sprint-management/ |
| Daily Stand-up | sprint-status-review | sprint-management/ |
| Sprint Review | sprint-status-review | sprint-management/ |
| Retrospective | retrospective-analysis | sprint-management/ |
| Backlog Refinement | requirements-traceability-matrix | sprint-management/ |
| Release Planning | dependency-tracking | risk-management/ |
| PI Planning (SAFe) | dependency-tracking, project-health-assessment | executive-reports/ |

---

## Security Requirements

1. **Authentication** — All connectors use OAuth 2.0 or managed identity; no shared secrets in prompts.
2. **Authorisation** — Role-based access control (RBAC) enforced at the connector level.
3. **Data Classification** — Prompts and outputs must respect sensitivity labels (Public / Internal / Confidential / Highly Confidential).
4. **Secrets Management** — API keys and connection strings stored in Azure Key Vault; never hard-coded.
5. **Network** — All API calls over HTTPS/TLS 1.2+; private endpoints preferred for enterprise deployments.
6. **Audit Logging** — All agent actions logged with user identity, timestamp, and input/output hashes.
7. **Data Residency** — AI processing must remain within the approved geographic boundary.
8. **PII / GDPR** — No personal data passed to AI models without explicit consent and anonymisation.

---

## Agent Development Standards

See [`docs/agent-creation-playbook/`](docs/agent-creation-playbook/) for step-by-step guidance.

### Mandatory Components per Agent

| Component | File | Purpose |
|-----------|------|---------|
| System prompt | `system-prompt.md` | Core persona and instructions |
| Skill manifest | `skills.yaml` | Skill bindings and versions |
| Schema references | `schemas.yaml` | Input/output schema pointers |
| Test cases | `tests/` | Validation scenarios |
| Governance checklist | `governance-checklist.md` | Pre-deployment sign-off |
| Change log | `CHANGELOG.md` | Version history |

### Versioning Convention

Agents and skills follow [Semantic Versioning](https://semver.org/):

- **MAJOR** — Breaking change to skill interface or schema.
- **MINOR** — New capability added; backward compatible.
- **PATCH** — Bug fix or prompt tuning; no interface change.

---

## Integration Guide

See [`docs/implementation-guide/`](docs/implementation-guide/) for platform-specific setup instructions.

### Microsoft 365 Copilot

1. Register a plugin manifest in the Microsoft 365 admin centre.
2. Point the manifest to the OpenAPI definitions in `manifests/copilot-studio-openapi/`.
3. Grant required Graph API permissions (read-only recommended).

### Azure DevOps

1. Create a Personal Access Token (PAT) with Work Items read scope.
2. Store the PAT in Azure Key Vault.
3. Reference the Key Vault secret in the custom connector definition in `manifests/custom-connectors/`.

### Jira

1. Create an Jira API token under your Atlassian account.
2. Store the token in Azure Key Vault.
3. Use the Jira custom connector definition in `manifests/custom-connectors/`.

---

## Contributing

We welcome contributions that improve the framework's coverage, quality, or governance posture.

1. Fork the repository and create a feature branch: `git checkout -b feature/your-skill-name`.
2. Follow the file and naming conventions in this README.
3. Add or update tests in the relevant `tests/` directory.
4. Complete the governance checklist in `docs/governance-standards/contribution-checklist.md`.
5. Open a Pull Request with a clear description and link to the relevant issue.

### Contribution Checklist

- [ ] Prompt reviewed for bias and harmful content.
- [ ] No PII or secrets in any files.
- [ ] Schema validated against JSON Schema Draft 2020-12.
- [ ] Test cases cover happy path and at least two edge cases.
- [ ] CHANGELOG.md updated.
- [ ] Documentation updated if interfaces changed.

---

## Versioning

| Component | Current Version |
|-----------|----------------|
| Framework | 1.0.0 |
| Skills (all) | 1.0.0 |
| Schemas (all) | 1.0.0 |
| OpenAPI Manifests | 1.0.0 |

See [CHANGELOG.md](CHANGELOG.md) for full version history.

---

## License

This project is licensed under the [MIT License](LICENSE).

> **Disclaimer**: This framework provides AI-assisted project management capabilities. All AI-generated content should be reviewed by a qualified project management professional before use in official communications or decisions. The authors make no warranty as to the accuracy or completeness of AI-generated outputs.

---

*Maintained by the PM-AISF Center of Excellence. For questions, open an issue or contact the repository maintainers.*
