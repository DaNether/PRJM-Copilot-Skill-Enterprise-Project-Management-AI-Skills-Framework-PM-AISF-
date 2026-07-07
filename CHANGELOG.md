# Changelog — PM-AISF Framework

All notable changes to the PM-AISF framework are documented here.  
Format: [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).  
Versioning: [Semantic Versioning](https://semver.org/).

---

## [1.0.0] — 2024-01-01

### Added

**Agents (6)**
- `executive-reporting-agent` — C-suite and steering committee reporting.
- `project-health-agent` — Multi-dimension project health scoring.
- `scrum-master-agent` — Scrum ceremony facilitation and sprint tracking.
- `raid-management-agent` — RAID log classification and management.
- `steering-committee-agent` — Governance pack generation and decision logging.
- `requirements-agent` — RTM maintenance and change impact assessment.

**Skills (11)**
- `weekly-rag-reporting` — RAG-status weekly reports.
- `project-health-assessment` — Eight-dimension health scoring.
- `raid-classification` — P×I risk scoring and response strategies.
- `stakeholder-communication` — Audience-adaptive communications.
- `executive-escalation` — P1/P2/P3 escalation classification.
- `sprint-status-review` — Sprint burn-down and impediment tracking.
- `retrospective-analysis` — Theme grouping and action item generation.
- `change-control-management` — Change request impact assessment.
- `dependency-tracking` — Cross-project dependency monitoring.
- `lessons-learned-analysis` — Six-category taxonomy and knowledge base entries.
- `requirements-traceability-matrix` — RTM, coverage calculation, gap analysis.

**Prompts (6 domains)**
- `executive-reports` — Portfolio dashboard and programme board pack.
- `status-reports` — Weekly and monthly report templates.
- `stakeholder-updates` — Go-live and change notification templates.
- `sprint-management` — Sprint planning and review templates.
- `risk-management` — Risk register update and escalation brief.
- `decision-logs` — Decision capture and impact assessment.

**Schemas (4)**
- `rag-report.schema.json` — Weekly status report structure.
- `raid.schema.json` — RAID log with P×I scoring.
- `project-health.schema.json` — Eight-dimension health model.
- `executive-dashboard.schema.json` — Portfolio executive view.

**Manifests**
- `pm-aisf-openapi.yaml` — Copilot Studio OpenAPI 3.0 manifest.
- `azure-devops-connector.json` — Azure DevOps custom connector.
- `sharepoint-connector.json` — SharePoint Graph API connector.

**Examples**
- Sample projects: Alpha (Green), Beta (Amber).
- Sample RAID log: Beta ERP critical risks.
- Sample status report: Alpha weekly Green report.
- Sample prompts: RAG report and RAID classification examples.

**Documentation**
- `implementation-guide/` — End-to-end deployment playbook.
- `agent-creation-playbook/` — Step-by-step agent development guide.
- `prompt-engineering-guide/` — Standards, anti-patterns, and testing guidance.
- `governance-standards/` — Responsible AI, security, audit, and PMI alignment.
- `best-practices/` — Design, prompt, schema, governance, and integration best practices.

**Repository**
- Comprehensive `README.md` with architecture, platform support, quick start, and catalogues.
- `CHANGELOG.md` (this file).
- `LICENSE` (MIT).
