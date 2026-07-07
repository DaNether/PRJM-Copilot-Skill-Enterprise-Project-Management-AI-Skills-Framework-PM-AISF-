# Power Platform Actions

**Version:** 1.0.0

Pre-built Power Automate flow templates that surface PM-AISF skills as reusable actions.

## Available Actions

| Action | Trigger | Description |
|--------|---------|-------------|
| Weekly RAG Report Generation | Scheduled (Monday 08:00) | Generates and distributes weekly RAG reports |
| RAID Item Escalation | When RAID score ≥ 7 | Auto-escalates critical RAID items |
| Sprint Status to Teams | Sprint day 1 and day 5 | Posts sprint status to Teams channel |
| Executive Dashboard Refresh | Scheduled (Monday 07:00) | Refreshes portfolio dashboard data |

## Import Instructions

1. Download the `.zip` solution file for the required action.
2. Import into Power Platform via **Solutions → Import**.
3. Configure environment variables (site URLs, connector references).
4. Activate the flow.

## Naming Convention

Flow names follow the pattern: `PMAISF-{SkillName}-{TriggerType}-v{version}`

Example: `PMAISF-WeeklyRAGReport-Scheduled-v1`
