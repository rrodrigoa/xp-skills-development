# Fault injection and recovery scenarios

## When to load
Dependency, persistence, retry or workflow risk.

## Implementation in the target project
Model failure modes such as timeout, dropped response, duplicate delivery, partial commit, process restart and resource exhaustion. Inject via test harness in isolated environment; assert bounded retries, cancellation, correct terminal outcomes, idempotence, cleanup and telemetry. Restore environment and record causal evidence.

## Required evidence and acceptance
Each approved fault scenario has observable assertion and recovery result; negative control detects failure handling regression.

## Guardrails
Avoid destructive or production tests without explicit approval. Mocked fault behavior must match actual contract.
