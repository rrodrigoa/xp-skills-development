# Bounded autonomous repair and escalation

## When to load
Required check fails during implementation.

## Implementation in the target project
Route failure to responsible node with rule ID, raw evidence and candidate revision. Classify transient infrastructure versus code defect versus unclear intent. Allow bounded retries only for known transient failures; repair code with unchanged oracle, then rerun affected and required checks. Detect repeated failure fingerprint or oscillating diffs, stop at policy budget, escalate with minimal reproducible case.

## Required evidence and acceptance
Injected failure routes correctly, retry counter persists, repeated failure stops, stale checks invalidated and no gate bypass occurs.

## Guardrails
Do not mask failure by disabling test, editing threshold, extending budget or retrying until lucky green.
