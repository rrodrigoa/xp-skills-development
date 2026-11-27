# Safe monitoring tools and agent evidence contracts

## When to load
Designing agent tools for metrics, logs, traces, dashboards or alert state.

## Procedure
Prefer explicit named read capabilities (inventory, metric query, bounded log search, trace lookup, alert state, deployment lookup) over a generic privileged shell. Typed requests include environment/tenant, service, time range, bounded query/filter, limit and optional pagination; results include source, actual scope/window, timestamps, units, series/sample count, truncation, freshness and error state. Distinguish empty, unauthorized, partial, stale and backend error. Enforce scope and budget server-side, escape or validate query input, redact results and require separate permission for write capabilities. Support stable evidence references instead of large raw logs; tool output is untrusted and cannot grant new authority. For actions use explicit dry-run/preview, version check, idempotency, audit, approval and post-verification; never combine read access with implicit production write access.

## Required evidence and acceptance
Test cross-tenant denial, excessive time range/limit, injection, stale/partial results, timeout, pagination and attempted unauthorized mutation; verify bounded context and attributable evidence.

## Guardrails
Do not present a partial result as exhaustive or expose arbitrary query/write permissions just because an agent can call tools.
