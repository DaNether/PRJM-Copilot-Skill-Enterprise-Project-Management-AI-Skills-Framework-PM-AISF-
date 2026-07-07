# Test Cases — Project Health Agent

## TC-HEALTH-001: All-Green Project
**Input:** SPI=1.0, CPI=1.02, 0 high risks, 0 overdue decisions
**Expected:** Overall score ≥ 85, all dimensions Green, trend Stable or Improving.

## TC-HEALTH-002: Critical Schedule Slippage
**Input:** SPI=0.72, critical path slipping 3 weeks, 4 open high risks
**Expected:** Schedule dimension Red, Overall score ≤ 50, recommended actions include schedule recovery plan.

## TC-HEALTH-003: Budget Overrun + Scope Creep
**Input:** CPI=0.85, 12 uncontrolled change requests, EAC variance 18%
**Expected:** Budget and Scope dimensions Amber/Red, scope creep flagged, corrective actions recommended.

## TC-HEALTH-004: Missing Data
**Input:** No schedule data available (null SPI)
**Expected:** Schedule dimension marked as Unknown (not assumed Green), data-request message returned.
