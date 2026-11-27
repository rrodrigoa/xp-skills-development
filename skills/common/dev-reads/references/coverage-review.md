# READS completeness and implementation review

## When to load
Reviewing telemetry for a feature or release.

## Procedure
Inventory critical operations and compare the health contract to code ownership, instrument sites, collected series and consumer queries. Look for missing terminal paths, retry double-counts, early returns, cancellation, hidden fallback, wrong denominator, missing probe, saturation proxy and inconsistent units. Check each measurement is actionable or diagnostic and has a consumer. Prioritize user-impact gaps, then cost and maintainability. Define a targeted implementation change and its tests; route telemetry implementation to dev-observability and alert design to dev-alerting.

## Required evidence and acceptance
Operation-by-dimension coverage matrix with exact evidence, gaps, owner, required fixes or approved exceptions. Verify new telemetry in a representative deployment before asserting monitoring readiness.

## Guardrails
Do not pass based on metric names or five panels alone; no universal requirement to implement every signal for every function.
