# Metrics, logs and tracing

## Use when
Production services need diagnosis or a feature affects service health.

## Implementation
Use dev-reads health-contract for what to measure and dev-observability instrumentation-plan for how. Keep telemetry owned at meaningful boundaries, classify logical outcomes separately from attempts, and respect privacy and overhead budgets. Use dev-grafana for query and dashboard design; dev-alerting for actionable alert rules.

## Verification and review
Use dev-observability verification and the applicable approved OBS gates. Confirm real emitted and collected data where required; distinguish missing data and actual zero.

## Avoid
Duplicated signal definitions, high-cardinality labels, sensitive payloads and paging on every error.
