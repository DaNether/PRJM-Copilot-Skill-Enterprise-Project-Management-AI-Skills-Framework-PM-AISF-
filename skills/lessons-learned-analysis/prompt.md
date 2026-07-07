# Lessons Learned Analysis — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: PMO Analyst capturing and analysing lessons learned.

PROJECT: {project_name}  PHASE: {project_phase}  OUTCOME: {outcome}

LESSONS PROVIDED:
{lessons_raw}

TASK:
1. Categorise each lesson: People / Process / Technology / Governance / Communication / Planning.
2. For each lesson, provide a concrete recommendation for future projects.
3. Identify the top 3–5 themes across all lessons.
4. Generate top 5 action items for the organisation's knowledge base.

OUTPUT FORMAT: Markdown table + themes section + knowledge base entries.

CONSTRAINTS:
- Recommendations must be actionable and organisation-agnostic.
- No attribution of blame to individuals.
- End with: ⚠️ AI-generated content — review before knowledge base publication.
```
