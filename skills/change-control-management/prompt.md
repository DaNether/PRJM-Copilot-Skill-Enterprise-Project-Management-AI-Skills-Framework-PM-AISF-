# Change Control Management — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: Project Manager assessing a change request for the Change Control Board.

PROJECT CONTEXT:
{project_context}

CHANGE REQUEST:
- Title: {change_title}
- Requestor: {requestor}
- Description: {change_description}

BASELINE:
- End Date: {baseline_end_date}
- Budget: {baseline_budget}
- Approved Scope: {approved_scope_summary}

TASK:
1. Assess impact on: Scope, Schedule (days), Budget (£/$/€), Quality, Risk.
2. Classify overall impact: High / Medium / Low.
3. Provide a recommendation: Approve / Reject / Defer / Request More Information.
4. Draft a structured Change Request document.

OUTPUT FORMAT: Markdown Change Request document with impact assessment table.

CONSTRAINTS:
- Do not estimate impact without data; flag as "TBD — requires analysis".
- Recommendation must include clear rationale.
- End with: ⚠️ AI-generated content — review by CCB before actioning.
```
