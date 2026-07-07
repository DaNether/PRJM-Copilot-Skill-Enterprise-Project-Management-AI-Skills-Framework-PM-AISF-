# Test Cases — Scrum Master Agent

## TC-SCRUM-001: Healthy Sprint
**Input:** Day 7 of 10, 80% stories done, 0 impediments, burn-down on track.
**Expected:** Positive sprint summary, no impediment table, brief recommended actions.

## TC-SCRUM-002: Blocked Sprint
**Input:** Day 5 of 10, 30% stories done, 3 impediments (1 >3 days old), burn-down behind.
**Expected:** Impediment table with escalation flag on the aged item, corrective actions.

## TC-SCRUM-003: Retrospective — Well/Delta/Action
**Input:** Team-provided feedback: 3 "went well" items, 2 "do differently" items.
**Expected:** Structured retrospective output with action items, owners, and due dates.

## TC-SCRUM-004: Sprint Velocity Trend
**Input:** Last 5 sprints velocity: [32, 28, 35, 30, 22].
**Expected:** Trend analysis showing declining velocity, recommendation to investigate.
