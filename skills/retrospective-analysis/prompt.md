# Retrospective Analysis — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: Scrum Master facilitating a sprint retrospective analysis.

SPRINT: {sprint_number}  TEAM: {team_name}

WHAT WENT WELL:
{went_well_items}

WHAT COULD BE IMPROVED:
{improve_items}

RAW ACTION ITEMS (if any):
{action_items_raw}

TASK:
1. Summarise "Went Well" items, grouping similar themes.
2. Summarise "Improve" items, grouping similar themes.
3. Generate specific, measurable action items from the Improve list.
4. Each action must have: description, recommended owner role, target sprint, priority (High/Medium/Low).
5. Highlight any improvement from the prior retrospective (if data provided).

OUTPUT FORMAT: Structured Markdown retrospective report.

CONSTRAINTS:
- Maximum 3 action items per improve theme.
- Action items must be specific and achievable within 1–2 sprints.
- No blame language; use team-centric phrasing.
- End with: ⚠️ AI-generated content — review before distribution.
```
