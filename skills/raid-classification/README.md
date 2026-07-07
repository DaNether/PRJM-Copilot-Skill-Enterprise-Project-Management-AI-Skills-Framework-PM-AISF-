# Skill: raid-classification

**Version:** 1.0.0  
**Description:** Classifies and prioritises RAID log items using probability×impact scoring and response strategy recommendations.

## Inputs

- item_text (string): free-text description of the RAID item
- item_category (string, optional): Risk/Assumption/Issue/Dependency
- project_context (string, optional)

## Outputs

- category (string: Risk/Assumption/Issue/Dependency)
- probability (integer: 1–3)
- impact (integer: 1–3)
- score (integer: 1–9)
- severity (string: Critical/High/Medium/Low)
- response_strategy (string: Avoid/Transfer/Mitigate/Accept/Monitor)
- recommended_owner_role (string)
- recommended_due_date_days (integer)

## Usage

```yaml
skills:
  - id: raid-classification
    version: ">=1.0.0"
    binding: required
```
