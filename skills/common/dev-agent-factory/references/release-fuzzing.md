# Release-triggered exploration and repair

## When to load
A verified release warrants automated testing.

## Implementation in the target project
On authorized release event, identify immutable artifact, deploy isolated test instance and execute mapped journeys and bounded stateful fuzz scenarios. Deduplicate failures by reproducible signature, record seed/trace and impact. Create scoped repair task against correct revision; reproduce, fix, verify, evaluate independently and require approved merge policy. Re-run release smoke and monitor health.

## Required evidence and acceptance
Trace from release artifact to counterexample, candidate, gate evidence and disposition; duplicate triggers idempotent; limits and rollback tested.

## Guardrails
Do not automatically merge, deploy or run destructive tests by default. Never fuzz live users or real accounts without explicit scope.
