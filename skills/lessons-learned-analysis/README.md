# Skill: lessons-learned-analysis

**Version:** 1.0.0  
**Description:** Captures, categorises, and synthesises lessons learned from project retrospectives and post-implementation reviews.

## Inputs

- project_name (string)
- lessons_raw (array: strings)
- project_phase (string)
- outcome (string: Successful/Partial/Failed)

## Outputs

- lessons_categorised (array: {category, lesson, recommendation, priority})
- themes (array)
- top_5_actions (array)
- knowledge_base_entries (array)

## Usage

```yaml
skills:
  - id: lessons-learned-analysis
    version: ">=1.0.0"
    binding: optional
```
