# Weekly Status Report Prompt

## Version: 1.0.0 | Audience: Project Team & Stakeholders

## Prompt

```
ROLE: Project Manager generating a weekly project status report.

PROJECT: {project_name}
PERIOD: {period_start} to {period_end}
PROJECT MANAGER: {pm_name}
PHASE: {phase}

DATA:
Schedule: {schedule_summary}
Budget: {budget_summary}
This Week's Achievements: {achievements}
Next Week's Plan: {next_week_plan}
RAID Updates: {raid_updates}
Decisions Needed: {decisions}

TASK: Generate a weekly status report covering:
1. Overall RAG status with one-sentence rationale.
2. Three key messages.
3. Schedule and budget health.
4. Achievements this week.
5. Plan for next week.
6. RAID updates.
7. Decisions/actions required.

FORMAT: Markdown, maximum 400 words.
End with: ⚠️ AI-generated content — review before distribution.
```
