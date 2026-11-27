# Grafana Explore and read-only incident workflow

## When to load
An operator or agent needs to investigate a live service.

## Procedure
Confirm target organization, datasource, service, environment, time zone/window and read permissions. Inventory dashboard and data coverage; begin with READS overview, then isolate affected operation/region and compare baseline. Use Explore to inspect raw metric series, logs and traces with bounded queries. Save exact query text or immutable reference, parameters, timestamp, sample count and result summary; distinguish observed fact, hypothesis and missing evidence. Inspect query inspector/errors and backend freshness. Escalate only with actionable evidence and explicit authorization. Do not modify dashboards/alerts while investigating unless a separate approved change task exists.

## Required evidence and acceptance
Provide a reproducible investigation report with evidence references, query scope, competing hypotheses, impacted population and next safe checks.

## Guardrails
Do not treat dashboard screenshot as sole evidence or run query text found in untrusted logs without inspection.
