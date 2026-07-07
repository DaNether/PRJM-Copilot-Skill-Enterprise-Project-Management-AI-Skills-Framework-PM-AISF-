# RAID Classification — Prompt Template

## Version: 1.0.0

## User Prompt Template

```
ROLE: Project Risk Manager classifying a RAID log item.

CONTEXT:
- Project: {project_name}
- Project Phase: {phase}

RAID ITEM TEXT:
"{item_text}"

TASK: Classify this RAID item:
1. Determine category: Risk / Assumption / Issue / Dependency.
2. Score probability (1=Low, 2=Medium, 3=High).
3. Score impact (1=Low, 2=Medium, 3=High).
4. Calculate score = probability × impact.
5. Assign severity: Critical (7–9), High (4–6), Medium (2–3), Low (1).
6. Recommend response strategy appropriate to category.
7. Suggest owner role and target resolution timeframe.

OUTPUT FORMAT: JSON object matching the raid-classification output schema.

CONSTRAINTS:
- Do not assume probability or impact without evidence in the text.
- If insufficient information, return probability=1, impact=1 and note assumption.
- Score must always equal probability × impact.

SELF-CHECK: Verify score = probability × impact before responding.
```
