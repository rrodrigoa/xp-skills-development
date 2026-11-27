# Loki and LogQL investigation

## When to load
Investigating structured operational logs in Grafana.

## Procedure
Start with authorized tenant, service, environment and bounded time window. Select streams using low-cardinality index labels; parse structured fields, then filter by event/outcome, trace ID or safe correlation field. Narrow range before costly parsing or regex. Distinguish log line count from logical operation count and sampling/rate-limit losses. Use structured metadata where supported for high-cardinality correlation; avoid indexing run/request IDs. Verify parser failures and field type conversion; inspect representative redacted lines. Derive log-based metrics only if completeness, duplication and semantic definition are established.

## Required evidence and acceptance
Known event and trace ID can be found; verify parser error handling, redaction, scoped access, late/missing logs and query cost.

## Guardrails
Do not run broad raw-payload searches across tenants or infer exact error rate from sampled logs.
