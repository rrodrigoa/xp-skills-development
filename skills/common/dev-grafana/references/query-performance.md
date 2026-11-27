# Grafana query performance and capacity

## When to load
Slow dashboards or expensive queries affect monitoring.

## Procedure
Measure query duration, returned series/points, datasource load, cache behavior and dashboard refresh fan-out. Use bounded time range and scope, appropriate step/resolution, recording rules for repeated expensive calculations and sane panel refresh. Avoid unbounded variables, unnecessary transformations or per-instance dashboards that fan out broadly. Investigate datasource timeouts, query queue, ingestion lag and cardinality separately from client rendering. Preserve meaningful temporal detail for short spikes and SLO windows. Document cost versus freshness and use approved budgets.

## Required evidence and acceptance
Compare before/after latency and series count over representative scopes/time ranges while validating numerical equivalence and incident visibility.

## Guardrails
Do not hide spikes by coarsening resolution or silently remove critical scope to make the dashboard faster.
