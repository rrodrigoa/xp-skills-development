# Cross-signal correlation and drilldown

## When to load
Connecting metrics, logs, traces and deployment events.

## Procedure
Align service identity, environment, operation, timestamp and release metadata across sources. Use exemplars to link a histogram observation to a retained trace; use trace/span correlation to find logs. Use deployment/config annotations and trace-to-metric links with explicit time windows. Support navigation from health overview to regional/operation cohort, dependency, then raw evidence. Correlation is a hypothesis aid: confirm population, sample availability and causal path. When no exemplar/trace exists, offer alternative log/metric investigation rather than declaring no issue.

## Required evidence and acceptance
Demonstrate an incident drilldown with known trace, corresponding logs and deployment marker; test missing trace, differing labels and clock skew.

## Guardrails
Never assume all data sources have identical retention, time precision or access permissions.
