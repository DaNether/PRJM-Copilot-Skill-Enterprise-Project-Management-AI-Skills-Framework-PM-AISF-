# Test Cases — Requirements Agent

## TC-REQ-001: RTM Coverage
**Input:** 20 requirements, 15 mapped to test cases.
**Expected:** Coverage = 75%, 5 gaps identified with recommended test creation actions.

## TC-REQ-002: Change Impact
**Input:** Change request modifying 3 approved requirements.
**Expected:** Impact assessment showing affected test cases, downstream dependencies, and recommended actions.

## TC-REQ-003: Requirement Quality Score
**Input:** Requirement: "The system should be fast."
**Expected:** Low quality score, flagged as ambiguous (no measurable criterion), improvement suggestion provided.
