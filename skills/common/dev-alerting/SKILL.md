---
name: dev-alerting
description: "Design actionable SLO and threshold alerts, evaluate rules, route notifications, test delivery, reduce fatigue and guide safe response."
---
# Alerting and incident response

Start with alert-contract for design, incident-response for active incidents or alert-value for portfolio review. Use dev-reads for user impact and SLI semantics; dev-observability for telemetry trust; dev-grafana for dashboards and queries. Alert evaluation and notification delivery are distinct. Production writes, silences, acknowledgements and mitigations require explicit authorization and approved scope. Never let an agent alter policy to hide failures.

## Reference selector
Read only the cards relevant to the task; start with one or two and expand for evidence, safety or unresolved decisions.

- [Alert design contract and actionability](references/alert-contract.md) — Proposing a new alert or reviewing existing ones.
- [SLO burn-rate alerts and multiwindow design](references/slo-burn.md) — Alerting on reliability objective consumption.
- [Threshold selection, windows and hysteresis](references/thresholds.md) — Designing static or dynamic alert conditions.
- [Severity, ownership and notification routing](references/severity-routing.md) — Defining alert recipients and escalation.
- [Alert rule lifecycle and evaluation states](references/rule-lifecycle.md) — Implementing or reviewing Grafana/Prometheus rules.
- [No data, error, stale and missing-series handling](references/missing-data.md) — An alert sees empty, incomplete or failed query results.
- [Grouping, deduplication and inhibition](references/group-dedup.md) — Reducing alert storms without losing incident visibility.
- [Silences, mute timings and maintenance windows](references/silences-maintenance.md) — Suppressing known planned notifications under authorization.
- [Grafana Alerting architecture and rule ownership](references/grafana-alerting.md) — Creating or changing a rule in Grafana.
- [Prometheus rules and Alertmanager integration](references/prometheus-alertmanager.md) — Using a datasource-managed alerting stack.
- [Actionable annotations, runbooks and response instructions](references/runbooks.md) — Preparing an alert for on-call use.
- [Alert testing, shadow evaluation and rollout](references/testing-rollout.md) — Introducing or modifying alert rules or routing.
- [Alert quality, value and continuous improvement](references/alert-value.md) — Reviewing alert portfolio and fatigue.
- [Anomaly detection and adaptive alerting](references/anomaly.md) — Considering statistically learned baselines or anomaly alerts.
- [Incident triage, escalation and safe mitigation](references/incident-response.md) — An alert fires or an agent is asked to act.
- [Alert pipeline health and delivery assurance](references/alert-chain-health.md) — Monitoring alert evaluation and notification reliability.
- [Alert configuration change control and rollback](references/change-governance.md) — An agent edits alert rules or notification policy.
- [READS alert selection by dimension](references/reads-alert-matrix.md) — Translating the service health contract into candidate alerts.
