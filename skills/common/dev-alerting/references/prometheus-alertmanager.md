# Prometheus rules and Alertmanager integration

## When to load
Using a datasource-managed alerting stack.

## Procedure
Distinguish Prometheus/ruler evaluation from Alertmanager routing, grouping, inhibition and silences. Confirm rule group cadence, expression return labels, pending duration and supported recovery settings. Validate rule syntax and unit tests using approved toolchain (e.g. promtool where applicable), including known input series, resets and missing samples. Confirm evaluator sends to intended Alertmanager, receiver matching and dedup labels; check HA/replica label handling and alert delivery health. Keep ownership and route configuration versioned in the target project; verify actual engine version.

## Required evidence and acceptance
Rule evaluation tests and integration delivery to authorized test receiver; verify missing data, HA duplication, recovery and fallback.

## Guardrails
Do not equate syntax success with correct alert behavior or assume Grafana-managed rules use identical test tooling.
