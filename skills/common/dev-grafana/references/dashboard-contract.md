# Dashboard design and audience contract

## When to load
Designing or reviewing a Grafana dashboard.

## Procedure
Identify audience, decisions, service, environment, owner and data sources before choosing panels. A service overview answers health and impact; dependency/resource views answer likely causes; incident drilldowns answer specific hypotheses. Group top-level panels by READS, add SLO and budget status where approved, show data freshness and traffic/sample counts, then link to detailed diagnostics. Use stable scope variables and default time ranges suited to signal cadence. Every panel has a question, unit, population, aggregation, legend, missing-data behavior and action/interpretation. Avoid unrelated charts and duplication. Ensure accessible visual encoding beyond color and concise descriptions.

## Required evidence and acceptance
Provide dashboard specification and test with a known incident and idle period; confirm another operator can identify impacted scope and drill down without private knowledge.

## Guardrails
Do not design a wall of charts from available metrics or assume a green panel proves service health.
