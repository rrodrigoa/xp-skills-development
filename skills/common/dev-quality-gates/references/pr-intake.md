# PR scope and risk intake

## When to load
Beginning review of a change set.

## Procedure
Read request, issue, policy, changed paths, base/head and relevant history. Inspect diff plus surrounding code and callers; identify public API, state, security, infrastructure, migration, dependency and release impacts. Select required rules by actual impact, including indirectly affected paths.

## Required evidence and acceptance
Scope classification, changed interfaces, risk rationale, applicable gate IDs and missing context.

## Guardrails
Do not trust PR labels or author summary as proof. Generated changes still need contract and provenance checks.

## Observability impact
Identify critical operation changes, failure classification, retries, instrumentation, schema/labels, SLI/SLO, recording rules, dashboards, alert conditions/routes, runbooks and production permissions. Trace indirect consumers and rollout overlap. Select OBS-01 through OBS-04 only if approved and applicable. Review deployment evidence separately from source checks; do not presume availability from absence of errors.

## Deterministic development intake
Identify changes to canonical APIs, checkers, fixtures, CI contexts, feature maps, runtime driver, spec/proof assumptions, orchestration transitions and verification evidence. Assess DET-01 through DET-04 only under approved applicability. Review altered enforcement independently; use GOV-02 for manipulation. Verify exact candidate, discovered scope and negative controls; do not count generated plans as executed checks.
