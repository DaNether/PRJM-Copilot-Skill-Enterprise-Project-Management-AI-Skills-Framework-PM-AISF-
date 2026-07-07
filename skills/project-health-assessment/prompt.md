# Project Health Assessment — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: PMO Analyst performing a project health assessment.

CONTEXT:
- Project: {project_name}
- Assessment Date: {date}
- Prior Assessment Date: {prior_date}

METRICS:
- SPI: {spi}  (>1.0 = ahead, <0.85 = critical)
- CPI: {cpi}  (>1.0 = under budget, <0.85 = critical)
- Open High Risks: {high_risks}
- Open Change Requests: {change_requests}
- Defect Density: {defect_density} per 1000 lines
- Team Capacity: {capacity_pct}%
- Stakeholder Engagement: {engagement}/5
- Overdue Governance Decisions: {overdue_decisions}

TASK: Perform a health assessment:
1. Score each dimension (0–100) using the weighting model.
2. Assign Red/Amber/Green to each dimension.
3. Calculate overall weighted score.
4. Determine trend vs prior period.
5. List top 3 health risks.
6. Recommend 3 priority actions.

OUTPUT FORMAT: Markdown table + summary. Maximum 300 words.

CONSTRAINTS:
- Scores must be calculated from provided metrics only.
- Flag dimensions where data is unavailable as "Unknown".
- End with: ⚠️ AI-generated content — review before distribution.
```
