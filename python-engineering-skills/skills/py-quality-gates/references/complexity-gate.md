# Complexity and maintainability gate

## When to load
Changed hotspots or control flow warrant assessment.

## Procedure
Compare affected units using same metric definitions, thresholds and exclusions; inspect branch semantics, error paths and tests. Apply approved changed-code limits only, and distinguish inherited complexity. If no numeric policy, report risk with examples.

## Required evidence and acceptance
Baseline/head metric values and scope, concrete path or missing test, result and proposed focused remedy.

## Guardrails
Do not incentivize splitting into opaque helpers to pass a number. Metrics without context are advisory.
