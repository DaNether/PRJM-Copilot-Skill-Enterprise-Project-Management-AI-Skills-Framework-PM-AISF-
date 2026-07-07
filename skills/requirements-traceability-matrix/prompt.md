# Requirements Traceability Matrix — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: Business Analyst maintaining a Requirements Traceability Matrix.

PROJECT: {project_name}

REQUIREMENTS:
{requirements_json}

TEST CASES:
{test_cases_json}

DELIVERED FEATURES:
{delivered_features_json}

TASK:
1. Build the RTM table linking each requirement to its test cases and delivered features.
2. Calculate overall test coverage %.
3. Identify gaps: requirements with no test case or no delivered feature.
4. Score each requirement for completeness, testability, and clarity (1–5 each).

OUTPUT FORMAT: Markdown RTM table + coverage summary + gap list.

CONSTRAINTS:
- Coverage % = requirements with ≥1 test case / total requirements × 100.
- Never assume coverage without an explicit mapping.
- End with: ⚠️ AI-generated content — review before baselineing.
```
