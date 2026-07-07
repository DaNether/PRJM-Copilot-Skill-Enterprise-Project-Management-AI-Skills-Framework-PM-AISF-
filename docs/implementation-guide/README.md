# Implementation Guide

## PM-AISF Deployment Playbook — Version 1.0.0

This guide covers end-to-end deployment of the PM-AISF framework across enterprise platforms.

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| Microsoft 365 licence | E3 or above recommended |
| Azure subscription | For Azure OpenAI and Key Vault |
| Copilot Studio licence | For agent deployment |
| Azure DevOps / Jira | For sprint data connectors |
| Power Platform | For custom connectors and flows |

---

## Deployment Steps

### Step 1 — Clone and Review

```bash
git clone https://github.com/DaNether/PRJM-Copilot-Skill-Enterprise-Project-Management-AI-Skills-Framework-PM-AISF-.git
```

Review the `docs/governance-standards/` before deploying to production.

### Step 2 — Configure Data Sources

1. Register Azure AD app registrations for each connector.
2. Store client secrets in Azure Key Vault.
3. Update connector JSON files with your tenant ID and Key Vault references.

### Step 3 — Deploy Schemas

Publish JSON schemas to a central schema registry (e.g., Azure API Management, Confluence).

### Step 4 — Deploy OpenAPI Manifests

Import `manifests/copilot-studio-openapi/pm-aisf-openapi.yaml` into Copilot Studio.

### Step 5 — Configure Agents

For each agent in `agents/`:
1. Create a new agent in Copilot Studio.
2. Copy the system prompt from `system-prompt.md`.
3. Bind skills using the `skills.yaml` references.
4. Configure data source connectors.
5. Run test cases from `tests/test-cases.md`.

### Step 6 — Governance Sign-Off

Complete the `governance-checklist.md` for each agent before production release.

---

## Platform-Specific Notes

### Microsoft Copilot Studio
- Use the OpenAPI manifest for plugin actions.
- Configure adaptive card outputs for Teams integration.
- Set conversation language to match your organisation's locale.

### Azure OpenAI Assistants
- Use JSON schemas as function tool definitions.
- Set `max_tokens` appropriately per skill (see README per skill).
- Enable content filtering with enterprise policy.

### GitHub Copilot
- Add relevant prompts to `.github/copilot-instructions.md`.
- Use skill READMEs as reference documentation for the coding context.

---

## Monitoring & Observability

1. Enable Azure Monitor logging for all Copilot Studio agents.
2. Set up alerts for error rates > 5%.
3. Review audit logs weekly in the PMO governance cycle.
4. Track skill usage metrics monthly.

---

## Upgrade Path

1. Check the CHANGELOG for breaking changes before upgrading.
2. Test in a non-production environment first.
3. Update schemas before agents (backward-compatible changes only).
4. Re-run all test cases after upgrade.
