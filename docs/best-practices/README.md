# Best Practices

## PM-AISF Enterprise Best Practices — Version 1.0.0

---

## Agent Design

1. **One agent, one persona** — Each agent should serve one primary persona. Avoid trying to serve all roles in one agent.
2. **Skills over monoliths** — Compose agents from skills rather than embedding all logic in the system prompt.
3. **Fail gracefully** — Agents must handle missing data without hallucinating. Always check for null/empty inputs.
4. **Least privilege** — Request only the data scopes your agent needs.
5. **Human-in-the-loop by default** — Assume human review is required for material outputs until proven otherwise.

---

## Prompt Writing

1. **Test before you commit** — Every new prompt must have at least one working example in `examples/`.
2. **Short prompts, structured context** — Keep the instruction section concise. Put detail in the context injection.
3. **Explicit output format** — Always specify the exact output format. Never say "write a report".
4. **Versioning is mandatory** — Increment the version number with every prompt change.
5. **Review for bias** — Have a colleague review prompts for language that could disadvantage any group.

---

## Data & Schema

1. **Schema-first design** — Define the output schema before writing the prompt.
2. **Validate always** — Run schema validation in CI/CD for any skill that returns structured data.
3. **Semantic versioning** — Follow SemVer strictly. A breaking schema change is a MAJOR version.
4. **Document all fields** — Every schema property must have a `description`.
5. **Test with edge cases** — Always test schemas with null values, empty arrays, and boundary values.

---

## Governance

1. **Governance checklist is mandatory** — Do not deploy to production without completing it.
2. **Audit logging must be enabled** — This is non-negotiable for enterprise deployments.
3. **Review cadence** — Schedule a quarterly review of all deployed agents for prompt drift and data freshness.
4. **Incident response** — Document the process for revoking an agent if it produces harmful output.
5. **AI transparency** — Always disclose to users that they are interacting with AI.

---

## Integration

1. **Test connectors independently** — Validate each connector in isolation before wiring to an agent.
2. **Mock data for development** — Use `examples/sample-projects/` data during agent development.
3. **Rate limiting** — Implement rate limiting on all connector calls to avoid API quota exhaustion.
4. **Error handling** — All connector calls must have a timeout and fallback message.
5. **Secrets in Key Vault** — Never store API keys, tokens, or passwords in agent configuration or code.

---

## PMI & Agile Alignment

1. **PMBOK alignment check** — When adding a new skill, map it to the relevant PMBOK 7 performance domain.
2. **Agile ceremonies** — Sprint-related skills must align to the Scrum Guide (2020).
3. **Terminology consistency** — Use PMI/Agile standard terminology (e.g., "sprint" not "iteration" for Scrum).
4. **RAG consistency** — Always use the enterprise RAG definition (Green/Amber/Red) — never invent new statuses.
