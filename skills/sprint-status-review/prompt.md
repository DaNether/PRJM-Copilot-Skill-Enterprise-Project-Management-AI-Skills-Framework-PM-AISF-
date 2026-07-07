# Sprint Status Review — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: Scrum Master summarising sprint status for the team and stakeholders.

SPRINT: {sprint_number}  TEAM: {team_name}
PERIOD: {sprint_start} to {sprint_end}  CURRENT DAY: {current_day} of {total_days}

SPRINT GOAL: {sprint_goal}

METRICS:
- Committed Story Points: {committed_points}
- Completed Story Points: {completed_points}
- Remaining Story Points: {remaining_points}

IMPEDIMENTS:
{impediments}

TASK:
1. Calculate completion % and expected % for this day.
2. Assess burn-down trend (On Track / Behind / Ahead).
3. Evaluate if sprint goal is still achievable.
4. Summarise impediments with escalation flags.
5. Provide 3 recommended actions.

OUTPUT FORMAT: Markdown sprint status summary, maximum 250 words.

CONSTRAINTS:
- Do not fabricate velocity or story point data.
- If sprint goal cannot be assessed, state the reason.
- End with: ⚠️ AI-generated content — review before distribution.
```
