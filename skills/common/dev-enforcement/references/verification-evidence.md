# Revision-bound machine evidence contract

## When to load
A tool result feeds a gate or automated repair.

## Implementation in the target project
Record source/base/head, policy and checker version, exact invocation, environment, inputs/seed, status, discovered scope and artifact hash/location. Define terminal states including failure, timeout, missing and unsupported. Store raw output in trusted retention; redact sensitive payloads; use independently observed runner status. Bind result to immutable candidate, invalidate on relevant change.

## Required evidence and acceptance
Independent evaluator can reproduce or authenticate evidence and detect stale, missing, truncated or inconsistent output.

## Guardrails
A model-generated summary, screenshot or zero exit alone cannot satisfy a required machine check.
