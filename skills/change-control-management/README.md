# Skill: change-control-management

**Version:** 1.0.0  
**Description:** Assesses change request impact across scope, schedule, budget, and risk dimensions, and drafts structured change request documents.

## Inputs

- change_title (string)
- change_description (string)
- requestor (string)
- project_context (object)
- baseline_data (object)

## Outputs

- change_impact_score (string: High/Medium/Low)
- schedule_impact_days (integer)
- budget_impact (number)
- scope_impact (string)
- risk_assessment (string)
- recommendation (string: Approve/Reject/Defer/More Info)
- change_request_document (string: Markdown)

## Usage

```yaml
skills:
  - id: change-control-management
    version: ">=1.0.0"
    binding: required
```
