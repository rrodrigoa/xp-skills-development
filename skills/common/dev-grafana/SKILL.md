---
name: dev-grafana
description: "Design READS dashboards, query metrics/logs/traces, correlate evidence, validate and govern Grafana assets and monitoring investigations."
---
# Grafana monitoring and diagnosis

Identify actual Grafana version, datasource, organization, scope and permissions. Use dashboard-contract for design or diagnostic-session for investigation. Use READS semantics from dev-reads and instrumentation contracts from dev-observability. Grafana is a presentation/query and optional alerting platform, not the definition of service health. Use dev-alerting for rule/notification behavior. Do not assume a particular backend or edition.

## Reference selector
Read only the cards relevant to the task; start with one or two and expand for evidence, safety or unresolved decisions.

- [Dashboard design and audience contract](references/dashboard-contract.md) — Designing or reviewing a Grafana dashboard.
- [READS service health dashboard](references/reads-dashboard.md) — Creating a health overview or standard service dashboard.
- [Panel visualization, transformations and units](references/panel-semantics.md) — Selecting visualization or debugging misleading charts.
- [Dashboard variables and scope safety](references/variables.md) — Building reusable dashboards across environments or services.
- [Prometheus and PromQL query reasoning](references/promql.md) — Writing or reviewing metric queries.
- [Recording rules and shared query semantics](references/recording-rules.md) — Expensive or repeated queries underpin panels and alerts.
- [Loki and LogQL investigation](references/loki-logql.md) — Investigating structured operational logs in Grafana.
- [Tempo, TraceQL and trace exploration](references/tempo-traceql.md) — Investigating distributed request or agent traces.
- [Cross-signal correlation and drilldown](references/correlation.md) — Connecting metrics, logs, traces and deployment events.
- [SLO and error-budget dashboards](references/slo-dashboard.md) — Visualizing reliability objectives and remaining budget.
- [Grafana dashboard and datasource lifecycle](references/provisioning.md) — Creating or changing monitoring assets as managed artifacts.
- [Grafana query performance and capacity](references/query-performance.md) — Slow dashboards or expensive queries affect monitoring.
- [Grafana Explore and read-only incident workflow](references/diagnostic-session.md) — An operator or agent needs to investigate a live service.
- [Grafana monitoring asset testing and drift detection](references/monitoring-validation.md) — Reviewing dashboards, queries or monitoring changes.
- [Datasource-neutral monitoring and query adapters](references/datasource-adapters.md) — Using Grafana with non-Prometheus metrics or mixed backends.
