# Agent failure analysis and governed evolution

## When to load
Agent repeats failures or workflow misroutes.

## Implementation in the target project
Collect actual execution trace, tool errors, gate findings, input context and revision; classify root cause as product code, tool contract, skill guidance, routing, orchestration, or external dependency. Propose smallest change to owning layer, favor deterministic constraint over prompt wording. Create replay scenario from failure, compare baseline/candidate behavior and seek independent review for graph/skill/policy edits. Version and stage rollout; preserve rollback.

## Required evidence and acceptance
Failure reproduces, fix prevents recurrence on replay without regressing representative successes; changed control reviewed; evidence retained.

## Guardrails
Agent cannot silently modify its own policy, evaluator, permissions, or approval path. Improvement is a candidate change, not autonomous authority.
