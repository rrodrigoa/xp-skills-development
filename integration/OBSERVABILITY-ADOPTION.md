# Observability adoption and operating workflow

This is guidance for an existing coding/monitoring agent, not an installer or agent runtime. Begin with approved project scope, role, permissions, supported languages and existing telemetry stack. Never load the full catalog.

## Phase 1 — Baseline and health contract
Load dev-reads health-contract and coverage-review. Inventory critical user journeys and operations; define eligibility, start/end, terminal outcome, dependencies, constrained resources and unknown-data policy. Capture existing telemetry and operational baseline. Propose SLOs only with owner approval. Complete the [health contract](../templates/reads-health-contract.md).

## Phase 2 — Implementation and verification
Load dev-observability instrumentation-plan and ownership-oo. Trace code boundaries, existing SDK/exporter and consumers. Choose narrowly scoped instrument changes; use Python/Java runtime and testing overlays when needed. Preserve behavior, correlation, privacy and telemetry schema compatibility. Test known workloads, failures, retries, cancellations, missing data and overhead; verify representative collection. Complete the [instrumentation plan](../templates/observability-plan.md).

## Phase 3 — Monitoring
Load dev-grafana dashboard-contract and relevant query card. Establish health overview, scope, fresh/unknown states, raw-query correctness and diagnostic drilldown. Verify actual backend, version and permissions. Propose source-controlled changes; use [dashboard specification](../templates/grafana-dashboard-spec.md). Do not write production without approval.

## Phase 4 — Alerting and response
Load dev-alerting alert-contract and testing-rollout. Select symptom/risk alerts with owner, action, condition, severity, route, recovery and no-data policy. Use [alert contract](../templates/alert-contract.md); test state and delivery separately. Shadow, review and cut over with rollback only when authorized.

## Phase 5 — Independent gate and deployment
Use dev-quality-gates, adopted OBS IDs and original decision protocol. Evaluate actual candidate/deployment evidence; required unknowns HOLD unless a known required failure BLOCKs. No self-approval or automatic merge/deploy. Keep source, asset and deployment revision identity distinct.

## Phase 6 — Operate, learn and improve
Use dev-reads health-reasoning and dev-observability diagnostic-workflow; collect read-only bounded evidence and compare hypotheses. Use dev-alerting incident-response for escalation/authorized mitigation. Record [incident evidence](../templates/incident-evidence.md); verify user recovery, propose durable code changes and regression tests. Review [alert portfolio](../templates/alert-portfolio-review.md) and update policy through governance, not ad hoc threshold edits.

## Context examples
- Coding agent changing retries: dev-reads errors, dev-observability ownership-oo and verification; language overlay if needed.
- Operator seeing rising queue age: dev-reads async-streaming, dev-grafana diagnostic-session; add incident-response if action is requested.
- Evaluator reviewing alert PR: dev-quality-gates decision-protocol and alert-readiness-gate, then dev-alerting testing-rollout and missing-data as needed.
