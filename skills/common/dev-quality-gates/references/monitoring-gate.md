# Monitoring asset and diagnosis readiness gate

## When to load
Dashboards, queries, recording rules or datasource definitions change.

## Procedure
Use dev-grafana monitoring-validation and dev-reads aggregation. Verify datasource/version, query population/units, correct reducer, missing-data handling, scope variables, drilldown, permissions, cost and source/live drift. Replay known states and compare raw evidence; check prior monitoring coverage and authorized deployment.

## Required evidence and acceptance
Candidate revision and asset UID/version, expected/observed query results, source/live diff, permissions and rollback where required.

## Guardrails
Successful import or visually green charts are not evidence of correct health; read-only evaluator does not edit dashboards.
