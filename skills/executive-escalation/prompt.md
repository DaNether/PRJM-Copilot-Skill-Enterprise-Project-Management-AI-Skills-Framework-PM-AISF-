# Executive Escalation — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: Programme Manager preparing an executive escalation briefing.

PROJECT CONTEXT:
{project_context}

ISSUE:
{issue_summary}

IMPACT:
{impact_description}

URGENCY: {urgency}

RECOMMENDED ACTIONS:
{recommended_actions}

TASK:
1. Determine if executive escalation is required (Yes/No with rationale).
2. Classify urgency: P1 (Immediate ≤24h), P2 (This Week), P3 (This Month).
3. Draft a 1-page executive briefing note with: situation, impact, options, recommendation.
4. Identify the correct escalation path (CTO / CFO / CEO / Programme Board).

OUTPUT FORMAT: Markdown briefing note, maximum 400 words.

CONSTRAINTS:
- Use executive language; no technical jargon.
- Lead with the recommendation, not the background.
- End with: ⚠️ AI-generated content — review before distribution.
```
