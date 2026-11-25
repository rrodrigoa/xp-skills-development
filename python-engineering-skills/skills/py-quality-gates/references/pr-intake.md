# PR scope and risk intake

## When to load
Beginning review of a change set.

## Procedure
Read request, issue, policy, changed paths, base/head and relevant history. Inspect diff plus surrounding code and callers; identify public API, state, security, infrastructure, migration, dependency and release impacts. Select required rules by actual impact, including indirectly affected paths.

## Required evidence and acceptance
Scope classification, changed interfaces, risk rationale, applicable gate IDs and missing context.

## Guardrails
Do not trust PR labels or author summary as proof. Generated changes still need contract and provenance checks.
