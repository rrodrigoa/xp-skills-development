# Recording rules and shared query semantics

## When to load
Expensive or repeated queries underpin panels and alerts.

## Procedure
Define canonical derived signals with owner, input contracts, evaluation interval, output labels, units and missing-data behavior. Preserve enough dimensions for downstream scope; record compatible numerators and denominators separately when consumers need different aggregations. Align rule evaluation ordering and windows; account for rule lag and late samples. Verify rule naming and version compatibility. Adopt only when query reuse/performance justifies additional stored series. Manage changes in source control and compare old/new results before consumer migration.

## Required evidence and acceptance
Reconcile recording rule results with raw queries over representative ranges, resets and rollouts; measure storage/query cost and evaluation failures.

## Guardrails
Do not record only averaged ratios when downstream weighting is required or use precomputed series with unknown freshness.
