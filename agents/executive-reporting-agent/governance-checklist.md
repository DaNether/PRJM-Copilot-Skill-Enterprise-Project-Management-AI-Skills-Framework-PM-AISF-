# Executive Reporting Agent — Governance Checklist

Version: 1.0.0 | Date: 2024-01-01

## Pre-Deployment Sign-Off

### Responsible AI

- [ ] System prompt reviewed for bias and discriminatory language.
- [ ] Output guardrails documented and tested.
- [ ] AI-generated content labelling implemented.
- [ ] Human-in-the-loop enforced for escalation decisions.

### Security

- [ ] No PII or credentials in system prompt or skill definitions.
- [ ] Connector uses OAuth 2.0 or managed identity.
- [ ] Least-privilege access scope confirmed with connector owners.
- [ ] Audit logging enabled and tested.
- [ ] Data classification label verified (Internal).

### Governance

- [ ] PMI PMBOK® alignment reviewed.
- [ ] Stakeholder approval obtained from PMO Director.
- [ ] Change log entry added for this version.
- [ ] Test cases passing (see tests/).

### Quality

- [ ] Output reviewed against sample data in examples/.
- [ ] Edge cases (no data, conflicting RAG, missing milestones) tested.
- [ ] Word-count guardrail (500 words) validated.

---

**Sign-off:**

| Role | Name | Date | Signature |
|------|------|------|-----------|
| PMO Director | | | |
| Security Architect | | | |
| Responsible AI Champion | | | |
