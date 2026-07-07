# Example: Weekly RAG Report Generation

This example demonstrates how to use the weekly-rag-reporting skill prompt with the Alpha Digital Transformation project data.

## Input

```
ROLE: Project Manager generating a weekly project status report.

PROJECT: Alpha Digital Transformation
PERIOD: 08 March 2024 to 15 March 2024
PROJECT MANAGER: Jane Smith
PHASE: Execution — Solution Design

SCHEDULE DATA:
- SPI: 1.02
- Schedule variance: 0 days
- Critical path: No slippage
- Next milestone: Solution Design Approval (15 May 2024) — On Track

BUDGET DATA:
- Approved budget: £2,500,000
- Actual spend: £1,100,000 (44% of budget, 42% through project)
- CPI: 1.01
- Forecast at completion: £2,480,000 (£20,000 under budget)

OPEN RAID ITEMS:
- R-001: UX vendor onboarding delay (Low) — being monitored
- I-001: SharePoint permissions — RESOLVED

TASK: Generate a weekly project status report...
[continues as per weekly-status-report.md template]
```

## Expected Output

See `alpha-weekly-report-2024-03-15.md` for the expected output.

## Notes

- The prompt uses structured context injection (schedule data, budget data, RAID items).
- Variables in `{curly_braces}` are substituted at runtime.
- The output validates against `schemas/rag-report-schema/rag-report.schema.json`.
