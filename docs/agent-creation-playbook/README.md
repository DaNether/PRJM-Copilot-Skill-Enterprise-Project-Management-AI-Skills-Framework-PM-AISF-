# Agent Creation Playbook

## Version 1.0.0

Step-by-step guide for building new agents in the PM-AISF framework.

---

## When to Create a New Agent

Create a new agent when you need to:
- Serve a distinct persona with a unique set of responsibilities.
- Combine 3+ skills into a coherent user experience.
- Provide a persistent conversation context for a domain.

Do **not** create a new agent to add a single prompt. Add the prompt to an existing skill instead.

---

## Agent Structure Checklist

```
agents/your-agent-name/
├── system-prompt.md          ✅ Required
├── skills.yaml               ✅ Required
├── governance-checklist.md   ✅ Required
├── CHANGELOG.md              ✅ Required
└── tests/
    └── test-cases.md         ✅ Required
```

---

## Step 1 — Define the Agent

Complete this brief before writing any files:

| Field | Your Answer |
|-------|-------------|
| Agent name | |
| Primary persona | |
| Top 3 user jobs | |
| Skills required | |
| Data sources | |
| Output formats | |
| Governance level | |

---

## Step 2 — Write the System Prompt

Follow this structure in `system-prompt.md`:

1. **Role** — Who is this agent? What is its expertise?
2. **Scope** — What is it authorised to do? What is explicitly out of scope?
3. **Behaviour** — Key behavioural rules (brevity, data-grounded, action-oriented).
4. **Output Structure** — Default output template with Markdown headings.
5. **Guardrails** — Hard constraints (length, classification, labelling).

### Guardrail Requirements (Mandatory)

All agents **must** include:
- ✅ AI-generated content footer: `⚠️ AI-generated content — review before distribution.`
- ✅ Data classification label in system prompt.
- ✅ Human-in-the-loop requirement documented.
- ✅ What the agent is NOT authorised to do.

---

## Step 3 — Define Skills Binding

In `skills.yaml`:
- Set `binding: required` for skills the agent cannot function without.
- Set `binding: optional` for enhancement skills.
- Always pin to a minimum version: `version: ">=1.0.0"`.

---

## Step 4 — Write Test Cases

Write at least 4 test cases in `tests/test-cases.md`:
1. Happy path (expected good data).
2. Edge case (missing/null data).
3. Error/escalation scenario.
4. Multi-turn or portfolio scenario (if applicable).

---

## Step 5 — Complete Governance Checklist

Before submitting a PR, complete every item in `governance-checklist.md` and obtain the required sign-offs.

---

## Naming Convention

Agent directory names must be lowercase, hyphen-separated, and end in `-agent`:

✅ `scrum-master-agent`  
❌ `ScrumMasterAgent`  
❌ `scrum_master`
