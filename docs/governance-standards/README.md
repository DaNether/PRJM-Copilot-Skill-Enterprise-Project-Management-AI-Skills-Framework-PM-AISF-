# Governance Standards

## PM-AISF Enterprise Governance Framework — Version 1.0.0

---

## Overview

The PM-AISF governance framework ensures that all AI-powered project management capabilities meet enterprise standards for:

- **Responsible AI** — Fairness, accountability, transparency, privacy.
- **Security** — Zero-trust access, audit logging, data classification.
- **Quality** — Schema validation, test coverage, version control.
- **Compliance** — PMI ethics, GDPR, enterprise information security policy.

---

## Responsible AI Principles

### Transparency
- All AI-generated content must include the footer: `⚠️ AI-generated content — review before distribution.`
- Agent identity must be disclosed to users.
- Sources and data timestamps must be referenced in reports.

### Accountability
- Human-in-the-loop is required for:
  - Escalation decisions (P1/P2).
  - Closing RAID items.
  - Recording governance decisions.
  - Change request approvals.
  - Distributing executive communications.

### Fairness
- All prompts are reviewed for bias before production release.
- Retrospective and lessons-learned prompts explicitly prohibit individual blame language.
- No protected characteristics (age, gender, ethnicity, etc.) are referenced in project prompts.

### Privacy
- No PII is included in prompts or AI inputs without explicit consent.
- Data anonymisation is applied before processing through AI models.
- GDPR Article 22 requirements are met for automated decision-making.

### Reliability
- All agent outputs are validated against JSON schemas before distribution.
- Confidence thresholds are applied to forward-looking statements.
- Stale data (>24 hours old) must be flagged in reports.

---

## Data Classification

| Label | Description | AI Processing |
|-------|-------------|--------------|
| Public | Publicly available | Permitted |
| Internal | For internal use only | Permitted with audit log |
| Confidential | Restricted distribution | Permitted with enhanced audit + human review |
| Highly Confidential | Board/legal/HR only | Not permitted in standard agents |

Default classification for project data: **Internal**  
Steering committee packs: **Confidential**

---

## Audit Requirements

Every AI agent interaction must log:
1. User identity (UPN or anonymised ID).
2. Timestamp (UTC).
3. Agent name and version.
4. Input data hash (not the data itself).
5. Output data hash.
6. Data sources accessed.
7. Human review status (Pending / Approved / Rejected).

Audit logs must be retained for a minimum of **7 years** (or as per organisational policy).

---

## Version Control Policy

| Component | Version Policy |
|-----------|---------------|
| Agents | Semantic versioning; MAJOR increments require governance re-approval |
| Skills | Semantic versioning; MINOR and PATCH via PR review |
| Schemas | Semantic versioning; MAJOR increments require schema migration plan |
| Prompts | Semantic versioning; any change requires re-testing |

---

## Contribution Checklist

Before any PR is merged:

- [ ] Responsible AI review completed.
- [ ] No PII or secrets in any files.
- [ ] Schema validated against JSON Schema Draft 2020-12.
- [ ] Test cases cover happy path and at least 2 edge cases.
- [ ] CHANGELOG.md updated.
- [ ] Governance checklist in agent directory completed.
- [ ] Second reviewer approved.

---

## PMI Code of Ethics Alignment

All skills and prompts adhere to the PMI Code of Ethics and Professional Conduct:

| Value | Implementation |
|-------|---------------|
| Responsibility | Human-in-the-loop for material decisions |
| Respect | No blame language; inclusive communication |
| Fairness | Unbiased prompts; diverse stakeholder representation |
| Honesty | Explicit AI labelling; no fabricated data |
