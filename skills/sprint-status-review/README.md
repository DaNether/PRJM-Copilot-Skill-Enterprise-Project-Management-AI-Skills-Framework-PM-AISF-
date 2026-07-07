# Skill: sprint-status-review

**Version:** 1.0.0  
**Description:** Summarises sprint progress, velocity, burn-down, and blockers for Scrum teams.

## Inputs

- sprint_number (integer)
- sprint_start (string: ISO date)
- sprint_end (string: ISO date)
- current_day (integer)
- committed_points (integer)
- completed_points (integer)
- impediments (array)
- sprint_goal (string)

## Outputs

- burn_down_trend (string: On Track/Behind/Ahead)
- completion_pct (number)
- impediment_summary (array)
- sprint_goal_achievable (boolean)
- recommended_actions (array)
- sprint_summary (string: Markdown)

## Usage

```yaml
skills:
  - id: sprint-status-review
    version: ">=1.0.0"
    binding: required
```
