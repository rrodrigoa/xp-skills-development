# Datasource-neutral monitoring and query adapters

## When to load
Using Grafana with non-Prometheus metrics or mixed backends.

## Procedure
Identify datasource plugin, query language, metric type, units, rollups, identity, freshness, permissions and supported alert evaluation. Translate the READS semantic contract into native query operations, not a mechanical PromQL substitution; vendor-specific rate, alignment, percentile and missing-data semantics may differ. For SQL/event stores count deduplicated eligible events with appropriate timestamp and late-event rules; for cloud metric APIs verify aggregation and alignment period. When combining sources, state join keys, time alignment, units and coverage; prefer canonical metrics where possible. Use bounded queries, parameterization and approved read-only credentials. Check whether datasource plugins support backend alerting and whether their result format meets rule requirements.

## Required evidence and acceptance
Known synthetic data yields the same expected contract result through each supported backend; verify rollup, missing data, permissions and query costs.

## Guardrails
Do not assume all datasource APIs expose raw samples, support histograms or use the same query syntax.
