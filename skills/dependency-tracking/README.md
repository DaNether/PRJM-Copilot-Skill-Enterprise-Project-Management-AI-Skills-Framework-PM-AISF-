# Skill: dependency-tracking

**Version:** 1.0.0  
**Description:** Maps and monitors inter-project and intra-project dependencies, surfaces dependency risks, and recommends mitigation.

## Inputs

- project_name (string)
- dependencies (array: {id, from_project, to_project, description, due_date, status})
- current_date (string: ISO date)

## Outputs

- dependency_map (array)
- at_risk_dependencies (array)
- blocking_dependencies (array)
- dependency_health (string: Red/Amber/Green)
- recommended_actions (array)

## Usage

```yaml
skills:
  - id: dependency-tracking
    version: ">=1.0.0"
    binding: required
```
