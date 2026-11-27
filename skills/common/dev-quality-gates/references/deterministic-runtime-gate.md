# Reproducible runtime verification gate

## When to load
Feature or defect changes requiring runtime evidence.

## Implementation in the target project
Use dev-runtime-verification feature-map, runtime-driver, independent-oracles and proof-artifacts as relevant. Inspect approved user journey, independent expected states, actual candidate build, setup/reset, negative controls and recorded results. Verify driver failures propagate and evidence is not stale.

## Required evidence and acceptance
Required journey assertions, environment, tool versions and artifacts; missing required execution UNKNOWN; demonstrated behavioral violation FAIL.

## Guardrails
Screenshots alone cannot satisfy a required semantic or security assertion.
