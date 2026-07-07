# Test Cases — Steering Committee Agent

## TC-STEER-001: Pack Generation
**Input:** Project name, meeting date, 3 agenda items, 2 open decisions from last meeting.
**Expected:** Complete steering committee pack with all sections, action follow-up highlighted.

## TC-STEER-002: Decision Log Update
**Input:** New decision text submitted by user.
**Expected:** Human confirmation requested before decision is recorded; audit trail created.

## TC-STEER-003: Actions Overdue
**Input:** Actions register with 2 items past due date.
**Expected:** Overdue items highlighted in red, escalation recommendations for chair.
