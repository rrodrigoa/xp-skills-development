# Alert rule lifecycle and evaluation states

## When to load
Implementing or reviewing Grafana/Prometheus rules.

## Procedure
Identify evaluator type (Grafana-managed or datasource-managed), actual version, evaluation interval/group, query/expression, dimensions and alert instance identity. Model normal, pending, firing and recovery/keep-firing behavior using supported states; distinguish rule health from condition state. Determine how state changes on reset, edit, restart or missing dimensions; preserve identity for stable routing/dedup. Specify window length and evaluation lag; do not assume pending time equals observed outage duration. Review how labels and annotations are derived, and how alert engine and notification engine interact.

## Required evidence and acceptance
Replay expected state transitions over simulated evaluation times and verify instance count, notification timestamps, recovery and restart/edited-rule behavior.

## Guardrails
Do not assume Grafana and Prometheus/Alertmanager states or features are identical across versions.
