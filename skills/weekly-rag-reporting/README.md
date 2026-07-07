# Skill: weekly-rag-reporting

**Version:** 1.0.0  
**Description:** Generates structured weekly RAG-status project reports from live project data.

## Inputs

- project_name (string)\n- period (string: YYYY-MM-DD)\n- schedule_data (object)\n- budget_data (object)\n- open_raid_items (array)\n- milestones (array)

## Outputs

- RAG status (Red/Amber/Green)\n- Weekly report Markdown document\n- Key messages (array, max 5)\n- Actions required (array)

## Personas

- Project Manager\n- Delivery Manager\n- PMO Analyst

## Usage

Reference this skill in an agent's `skills.yaml`:

```yaml
skills:
  - id: weekly-rag-reporting
    version: ">=1.0.0"
    binding: required
```

## Prompt Files

See `prompt.md` for the full prompt template.

## Changelog

See `CHANGELOG.md` for version history.
