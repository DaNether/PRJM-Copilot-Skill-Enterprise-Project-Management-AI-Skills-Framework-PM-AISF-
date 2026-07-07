# Prompt Engineering Guide

## PM-AISF Prompt Engineering Standards — Version 1.0.0

---

## Principles

### 1. Role Definition
Always begin with a clear persona and scope statement.

```
ROLE: Senior Project Manager generating a weekly status report for the project sponsor.
```

### 2. Context Injection
Provide structured context before the task. Use labelled sections.

```
CONTEXT:
- Project: {project_name}
- Phase: {phase}
- Period: {period}
- RAG Status Last Week: {prior_rag}
```

### 3. Structured Output
Explicitly specify output format, structure, and length.

```
OUTPUT FORMAT: Markdown with the following sections:
1. RAG Status (one line)
2. Key Messages (3 bullet points)
3. Schedule Summary (2–3 sentences)
...
MAXIMUM LENGTH: 400 words.
```

### 4. Guardrails
Include hard constraints in every prompt.

```
CONSTRAINTS:
- Do not speculate beyond provided data.
- RAG status must match enterprise definition.
- Do not include PII.
- End with: ⚠️ AI-generated content — review before distribution.
```

### 5. Self-Check Instruction
End prompts with a validation step to reduce errors.

```
SELF-CHECK: Before responding, verify that:
1. RAG status is consistent with schedule and budget data.
2. All calculations are correct.
3. Output is within the word limit.
```

---

## Anti-Patterns (Avoid These)

| Anti-Pattern | Problem | Fix |
|-------------|---------|-----|
| "Write a project report" | Too vague | Use the full template with context |
| "Assume the project is on track" | Encourages fabrication | Provide actual data |
| No output format specified | Inconsistent outputs | Always specify format and length |
| No guardrails | Hallucination risk | Always include constraints |
| No AI labelling instruction | Governance violation | Always include footer instruction |

---

## Variable Naming Convention

Variables in prompt templates use `{snake_case}` in curly braces:

✅ `{project_name}`, `{period_start}`, `{rag_status}`  
❌ `[ProjectName]`, `<PERIOD>`, `{{project.name}}`

---

## Prompt Versioning

Each prompt file includes:
```markdown
## Version: 1.0.0
```

Increment the version when:
- **MAJOR**: Breaking change to output structure or variable names.
- **MINOR**: New section or variable added (backward compatible).
- **PATCH**: Wording improvement; no structural change.

---

## Testing Prompts

Before committing a new prompt:
1. Test with at least one happy-path example from `examples/sample-projects/`.
2. Test with at least one edge case (missing data, null values).
3. Validate structured outputs against the relevant schema.
4. Have a second person review for bias and harmful content.

---

## Prompt Length Guidelines

| Use Case | Max Tokens (Input) | Max Words (Output) |
|----------|-------------------|-------------------|
| Weekly RAG report | 800 | 400 |
| Executive briefing | 1000 | 500 |
| Sprint summary | 600 | 250 |
| RAID classification | 400 | 150 (JSON) |
| Stakeholder email | 500 | 300 |

---

## Chain-of-Thought for Complex Prompts

For multi-step analysis (health assessments, change impact), use explicit chain-of-thought:

```
TASK: Follow these steps in order:
1. First, assess each dimension independently.
2. Then, calculate the weighted score.
3. Then, determine the overall RAG status.
4. Finally, generate recommended actions.

Show your working for the score calculation.
```
