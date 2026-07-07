# Skill: project-health-assessment

**Version:** 1.0.0  
**Description:** Scores and classifies project health across eight dimensions using a weighted scoring model.

## Inputs

- project_name (string)
- schedule_performance_index (number: SPI)
- cost_performance_index (number: CPI)
- open_risks_high (integer)
- change_requests_open (integer)
- defect_density (number)
- team_capacity_pct (number)
- stakeholder_engagement_score (number: 1–5)
- governance_overdue_decisions (integer)

## Outputs

- overall_score (number: 0–100)
- overall_rag (string: Red/Amber/Green)
- dimension_scores (object)
- trend (string: Improving/Stable/Deteriorating)
- top_risks (array)
- recommended_actions (array)

## Personas

- Project Manager
- Programme Manager
- Delivery Manager
- PMO Analyst

## Usage

```yaml
skills:
  - id: project-health-assessment
    version: ">=1.0.0"
    binding: required
```
