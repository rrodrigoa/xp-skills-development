# Telemetry correctness, safety and compatibility gate

## When to load
Instrumentation, telemetry schema, context or export changes.

## Procedure
Use dev-observability telemetry-contract, verification, privacy-audit and ownership-oo as relevant. Check single terminal observation, matching units/type/temporality, bounded dimensions, no duplicate auto/manual collection, trace continuity, redaction, exporter isolation and overhead. Check consumer compatibility and mixed-version migration; inspect actual test output and backend samples if required. Known prohibited sensitive capture or contract break is FAIL; missing evidence is UNKNOWN.

## Required evidence and acceptance
Revision-bound test and pipeline evidence, schema/consumer diff, privacy and cost/overhead assessment, migration/rollback.

## Guardrails
Do not require live access if policy accepts staging; never substitute unit tests for a specifically required deployed check.
