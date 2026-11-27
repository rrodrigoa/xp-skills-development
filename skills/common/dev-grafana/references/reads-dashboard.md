# READS service health dashboard

## When to load
Creating a health overview or standard service dashboard.

## Procedure
Top row: service/environment, release, time window, telemetry freshness and current SLO status. R row: demand, admitted and completed rate; show traffic volume. E row: terminal failed count and ratio, breakdown by bounded outcome and dependency. A row: user journey SLI, synthetic success, coverage and budget remaining. D row: p50/p95/p99 distributions or threshold good fraction, queue/processing separation, sample count. S row: bottleneck capacity/headroom, queue depth/age and rejection, with per-resource links. Include global and regional/operation breakdowns; avoid averaging percentiles. Distinguish unknown from zero/healthy; annotate deployments and incidents. Link panel definitions to READS contract and runbooks.

## Required evidence and acceptance
Known workload and failure replay verifies each row and labels, unit and time window; demonstrate drilldown from failed journey to traces/dependency/saturation.

## Guardrails
Do not use generic CPU/memory charts as the sole saturation view or fill missing availability with 100%.
