# Architecture drift and regression

## When to load
Comparing a PR or release with accepted architecture.

## Procedure
Compare base and head using same tool/version, graph scope and exclusions; identify new edges, cycles, boundary violations, public contracts and changed state ownership. Reconcile with accepted ADRs and exceptions. Classify inherited debt separately from introduced or worsened issues.

## Required evidence and acceptance
Report added/removed/worsened findings, affected contracts, evidence and baseline identity; propose a narrow remediation or exception.

## Guardrails
A baseline cannot authorize new violations. A fixed finding must not silently reappear; do not compare incompatible metrics.
