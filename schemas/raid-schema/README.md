# RAID Schema

**Version:** 1.0.0 | **Standard:** JSON Schema Draft 2020-12

Defines the structure for RAID (Risks, Assumptions, Issues, Dependencies) logs.

## ID Format

RAID item IDs follow the pattern: `{category_initial}-{number}` e.g.:
- `R-001` — Risk
- `A-001` — Assumption
- `I-001` — Issue
- `D-001` — Dependency

## Severity Bands (Risks)

| Score | Severity |
|-------|----------|
| 7–9   | Critical |
| 4–6   | High     |
| 2–3   | Medium   |
| 1     | Low      |

Score = Probability (1–3) × Impact (1–3)
