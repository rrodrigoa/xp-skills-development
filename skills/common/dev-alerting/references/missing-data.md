# No data, error, stale and missing-series handling

## When to load
An alert sees empty, incomplete or failed query results.

## Procedure
Differentiate query error, no series, stale data, zero denominator, one missing dimension and valid zero. For Grafana-managed rules inspect configured No Data/Error policies and missing-series eviction; generated datasource error/no-data alerts and resolved notifications can have different labels/reasons. For datasource-managed rules verify backend semantics independently. Keep last state only as a bounded policy with separate monitoring failure detection. Define heartbeat/coverage rule and route telemetry pipeline faults to its owner. Decide failure behavior for critical user SLI using approved policy, not universal fail-open/closed. Alert on partial loss where critical cohorts vanish.

## Required evidence and acceptance
Inject missing all, missing one series, query timeout, stale values, fresh zero and recovery; inspect state reason, routing and operator-visible unknown status.

## Guardrails
Do not treat missing series eviction as recovery or suppress errors indefinitely without independent coverage.
