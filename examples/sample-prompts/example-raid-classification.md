# Example: RAID Item Classification

This example demonstrates the raid-classification skill.

## Input

```
ROLE: Project Risk Manager classifying a RAID log item.
CONTEXT: Project Beta ERP Migration, Execution phase.

RAID ITEM TEXT:
"Our lead developer has handed in her notice. Her last day is 5 April. She is the
 only person who understands the custom payroll integration module."

TASK: Classify this RAID item...
[continues as per raid-classification prompt template]
```

## Expected Output

```json
{
  "category": "Risk",
  "probability": 3,
  "impact": 3,
  "score": 9,
  "severity": "Critical",
  "response_strategy": "Mitigate",
  "recommended_owner_role": "Project Manager",
  "recommended_due_date_days": 5,
  "rationale": "High probability (resignation confirmed) × High impact (sole knowledge holder for critical module) = Critical risk score 9. Immediate knowledge transfer required."
}
```

## Notes

- Score = probability (3) × impact (3) = 9 ✓
- Self-check validates arithmetic before response.
