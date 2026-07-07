# Skill: retrospective-analysis

**Version:** 1.0.0  
**Description:** Structures retrospective findings into What Went Well, What Could Be Improved, and Action Items with owners and due dates.

## Inputs

- sprint_number (integer)
- team_name (string)
- went_well_items (array)
- improve_items (array)
- action_items_raw (array, optional)

## Outputs

- went_well_summary (array)
- improve_summary (array)
- action_items (array: {action, owner_role, due_sprint, priority})
- retrospective_report (string: Markdown)

## Usage

```yaml
skills:
  - id: retrospective-analysis
    version: ">=1.0.0"
    binding: required
```
