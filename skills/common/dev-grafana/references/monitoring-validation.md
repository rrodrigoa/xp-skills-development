# Grafana monitoring asset testing and drift detection

## When to load
Reviewing dashboards, queries or monitoring changes.

## Procedure
Validate each datasource UID, query syntax/version, expected labels, unit/reducer, time range and panel/alert semantics. Replay known healthy, error, slow, saturation, idle, no data and partial-coverage states; compare raw backend result with displayed value. Verify variable scoping, drilldown links, permissions, dashboard ownership and provisioned/live drift. Check query cost and refresh behavior. Include monitoring chain failure and mixed-version rollout cases. Compare source definitions and deployed asset revisions before signoff; review only authorized scoped changes.

## Required evidence and acceptance
Panel-by-panel expected/observed table, query evidence, screenshot only as supplemental evidence, drift and permissions checks, gaps and rollback.

## Guardrails
Do not approve assets based solely on successful import or appearance; missing live validation is UNKNOWN for a required live gate.
