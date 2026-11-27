# Independent agent and machine evaluator

## When to load
A candidate needs objective approval.

## Implementation in the target project
Separate author, verification runner, policy owner and merge authority. Give verifier read-only access to candidate and approved evidence; run independent checks in constrained environment and validate artifacts rather than author narrative. Evaluate required gate IDs with existing decision protocol; preserve uncertainty for semantic judgments. Do not let agent-written status strings directly authorize merge.

## Required evidence and acceptance
Author cannot alter trusted verdict or self-approve; stale/fabricated evidence and missing approval trigger BLOCK/HOLD as appropriate.

## Guardrails
Different model instances alone do not guarantee independence; authority and evidence isolation are necessary.
