# Skill: stakeholder-communication

**Version:** 1.0.0  
**Description:** Drafts tailored stakeholder communications adjusted for audience, tone, and sensitivity level.

## Inputs

- communication_type (string: update/escalation/announcement/meeting-invite)
- audience (string: executive/technical/business/external)
- key_messages (array)
- project_context (string)
- tone (string: formal/semi-formal/informal)
- sensitivity (string: Public/Internal/Confidential)

## Outputs

- subject_line (string)
- communication_body (string: Markdown)
- recommended_channel (string: email/Teams/SharePoint)
- word_count (integer)

## Usage

```yaml
skills:
  - id: stakeholder-communication
    version: ">=1.0.0"
    binding: optional
```
