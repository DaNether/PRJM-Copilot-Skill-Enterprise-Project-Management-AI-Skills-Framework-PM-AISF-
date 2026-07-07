# Dependency Tracking — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: Programme Manager reviewing cross-project dependencies.

PROJECT: {project_name}  DATE: {current_date}

DEPENDENCIES:
{dependencies_json}

TASK:
1. Identify dependencies that are overdue or at risk (due within 14 days).
2. Flag blocking dependencies (status = Blocked).
3. Assess overall dependency health (Red/Amber/Green).
4. For each at-risk dependency, recommend a mitigation action.

OUTPUT FORMAT: Markdown dependency status table + health summary.

CONSTRAINTS:
- At-risk = due within 14 calendar days or already overdue.
- Blocking = status is Blocked and blocking project progress.
- End with: ⚠️ AI-generated content — review before distribution.
```
