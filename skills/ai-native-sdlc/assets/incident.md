# Incident: <short observed symptom>

Use evidence from the current investigation. Replace unknowns explicitly; do not reconstruct missing facts as observations. Delete these instructions from the finished record.

- Event ID / authoritative record: <reference>
- Service and environment: <values>
- Observation window and timezone: <values>
- Allowed response for this investigation: <read-only, local patch, or specifically authorized operation>

## Observations

| Time | Observation | Source | Reliability or missing context |
| --- | --- | --- | --- |
| <time> | <measured symptom> | <link or log location> | <caveat> |

- User impact: <observed extent or unknown>
- Recent relevant changes: <verified revisions/deployments, or unknown>

## Hypotheses

| Possible cause | Supporting evidence | Contradicting or missing evidence | Next discriminating check |
| --- | --- | --- | --- |
| <cause> | <evidence> | <gap> | <check> |

## Response and recovery

- Proposed action and rationale: <action>
- Applicable authorization / runbook: <reference, scope, or missing>
- Actions actually performed and results: <tool-confirmed evidence>
- Recovery condition and observation period: <existing service criterion, or proposed criterion requiring agreement>
- Recovery evidence: <result, or not established>

## Follow-up

- Remaining problem and desired behavior: <input for a change record>
- Regression scenario: <condition, action, expected result>
- Linked change record: <reference, or not created>
- Next action and owner: <values>
