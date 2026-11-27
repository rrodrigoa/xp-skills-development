# Cardinality, telemetry volume and cost budgets

## When to load
Selecting labels, attributes, sampling or retention.

## Procedure
Estimate series as the product of bounded attribute values and resource dimensions, multiplied by histogram buckets/derived series where applicable; estimate logs/traces by event rate, bytes, retention, replication and sampling. Inspect actual series/churn, ingest limits, storage and query latency. Use templated route, operation, stable outcome and bounded error categories. Keep request/run/user IDs, raw URLs, stack traces and arbitrary text out of metric labels and log index labels; use permitted structured fields or trace attributes with access controls. Set SDK/collector limits and approved budgets, monitor dropped attributes/data, and review worst-case rollout or tenant growth. Prefer reducing unnecessary telemetry before sampling away needed evidence.

## Required evidence and acceptance
Provide expected and observed cardinality/volume, top contributors, budget ownership, growth/load tests and rejection/redaction behavior.

## Guardrails
Do not use a universal cardinality cap or put secrets in non-indexed fields merely because they are not labels.
