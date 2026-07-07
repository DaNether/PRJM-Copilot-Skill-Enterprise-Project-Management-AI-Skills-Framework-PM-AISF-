# Test Cases — RAID Management Agent

## TC-RAID-001: New Risk Classification
**Input:** "Vendor contract renewal delayed by 3 weeks. Possible impact on go-live."
**Expected:** Category=Risk, Probability=2, Impact=3, Score=6, Status=High, response strategy recommended.

## TC-RAID-002: Critical Issue Escalation
**Input:** Risk score 9 item with no mitigation owner.
**Expected:** Escalation flag set, notification message drafted, human sign-off requested.

## TC-RAID-003: Stale Items Report
**Input:** RAID log with 5 items not updated in >14 days.
**Expected:** Stale items list with owner names and recommended action to re-engage.

## TC-RAID-004: Dependency Mapping
**Input:** Project A depends on Project B completing API delivery by Q2.
**Expected:** Dependency item created, cross-project link noted, risk of slippage assessed.
