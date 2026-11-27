---
name: dev-observability
description: "Design, implement, test and diagnose metrics, logs, traces, context, OpenTelemetry pipelines, agent telemetry and safe instrumentation."
---
# Observability engineering

Start from the user-facing health contract in dev-reads and existing instrument ownership. Select instrumentation-plan for a feature or diagnostic-workflow for an incident; use only relevant signal cards. Treat telemetry as a versioned product contract. Domain behavior, security and resource ownership must remain correct even when observability fails. Route Grafana and alert changes to their own skills.

## Reference selector
Read only the cards relevant to the task; start with one or two and expand for evidence, safety or unresolved decisions.

- [Observability-first feature design](references/instrumentation-plan.md) — Designing a service, feature, migration or refactor.
- [Object-oriented telemetry ownership and instrumentation boundaries](references/ownership-oo.md) — Changing code to support observability without degrading design.
- [Versioned telemetry schema and semantic contracts](references/telemetry-contract.md) — Adding, changing or removing telemetry.
- [Metric instruments, temporality and lifecycle](references/metrics-instruments.md) — Selecting metric type or diagnosing metric math.
- [Structured logs, events and diagnostic context](references/structured-logs.md) — Designing logs for humans and machines.
- [Distributed traces and meaningful spans](references/traces-spans.md) — Instrumenting multi-step operations or dependencies.
- [Context propagation and correlation](references/context-propagation.md) — Crossing process, thread, coroutine or message boundaries.
- [OpenTelemetry API, SDK, collector and export pipeline](references/otel-pipeline.md) — Designing or diagnosing the telemetry pipeline.
- [Auto versus manual instrumentation](references/auto-manual.md) — Introducing instrumentation in an existing application.
- [Cardinality, telemetry volume and cost budgets](references/cardinality-cost.md) — Selecting labels, attributes, sampling or retention.
- [Sampling, exemplars and representativeness](references/sampling.md) — Controlling trace volume or investigating rare events.
- [Telemetry security, privacy and audit separation](references/privacy-audit.md) — Telemetry may contain sensitive data or cross tenant boundaries.
- [Non-disruptive instrumentation and failure isolation](references/failure-isolation.md) — Adding telemetry to a performance-critical path.
- [Instrumentation tests and end-to-end verification](references/verification.md) — Testing changed telemetry or its consumers.
- [Telemetry evolution and safe rollout](references/migration.md) — Refactoring telemetry or changing a shared schema.
- [Runtime, container and Kubernetes observability](references/kubernetes-runtime.md) — Operating deployed services and workers.
- [AI agent, LLM and tool instrumentation](references/agent-telemetry.md) — Implementing or debugging an agentic system.
- [Evidence-driven incident investigation and code improvement](references/diagnostic-workflow.md) — An agent is asked to reason from telemetry or fix an observed issue.
- [Monitoring the monitoring pipeline](references/telemetry-health.md) — Signals go missing or observability reliability matters.
- [Safe monitoring tools and agent evidence contracts](references/monitoring-agent-tools.md) — Designing agent tools for metrics, logs, traces, dashboards or alert state.

For development-factory health, use dev-agent-factory factory-observability: distinguish runs, attempts, repair loops, verified outcomes, escaped defects and per-accepted-change cost. Link telemetry to evidence without leaking identifiers or secrets.
