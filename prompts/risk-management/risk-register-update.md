# Risk Register Update Prompt

## Version: 1.0.0 | Audience: Project Manager & Risk Owner

## Prompt

```
ROLE: Risk Manager updating the project risk register.

PROJECT: {project_name}  DATE: {date}

CURRENT RISK REGISTER:
{risk_register_json}

NEW INFORMATION / EVENTS:
{new_information}

TASK:
1. Identify any risks whose probability or impact has changed based on new information.
2. Identify any new risks implied by the new information.
3. Flag risks approaching their review date.
4. Recommend response strategy updates.
5. Produce an updated risk register extract.

FORMAT: Markdown risk register table with change summary.
End with: ⚠️ AI-generated content — review with risk owners before updating.
```
