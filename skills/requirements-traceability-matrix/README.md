# Skill: requirements-traceability-matrix

**Version:** 1.0.0  
**Description:** Maintains a Requirements Traceability Matrix (RTM) mapping business requirements to design artefacts, test cases, and delivered features.

## Inputs

- project_name (string)
- requirements (array: {id, description, type, priority, source})
- test_cases (array: {id, title, requirement_id})
- delivered_features (array: {id, title, requirement_ids})

## Outputs

- rtm_table (array)
- coverage_pct (number)
- gaps (array)
- quality_scores (array: {req_id, completeness, testability, clarity})

## Usage

```yaml
skills:
  - id: requirements-traceability-matrix
    version: ">=1.0.0"
    binding: required
```
