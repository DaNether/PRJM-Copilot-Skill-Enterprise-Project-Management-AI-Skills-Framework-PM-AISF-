# Skill: executive-escalation

**Version:** 1.0.0  
**Description:** Identifies escalation-worthy issues and drafts executive briefings with recommended actions and urgency classifications.

## Inputs

- issue_summary (string)
- impact_description (string)
- urgency (string: Immediate/This Week/This Month)
- recommended_actions (array)
- project_context (string)

## Outputs

- escalation_required (boolean)
- urgency_level (string: P1/P2/P3)
- briefing_note (string: Markdown)
- recommended_executive_action (string)
- escalation_path (string)

## Usage

```yaml
skills:
  - id: executive-escalation
    version: ">=1.0.0"
    binding: required
```
