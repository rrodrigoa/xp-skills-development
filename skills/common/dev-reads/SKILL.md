---
name: dev-reads
description: "Define and reason about Request rate, Errors, Availability, Duration and Saturation; health contracts, SLIs, SLOs and diagnosis."
---
# READS service health

Use this skill to decide what service health means, independently of tools. Begin with health-contract for a new service or health-reasoning for an incident; select the dimension or workload card needed. READS is a minimum service-health model, not a mandate that every function emit five metrics. Use dev-observability for implementation, dev-grafana for presentation/querying and dev-alerting for response policy.

## Reference selector
Read only the cards relevant to the task; start with one or two and expand for evidence, safety or unresolved decisions.

- [READS service health contract](references/health-contract.md) — Defining health for a new or existing service.
- [R — Request rate and workload accounting](references/request-rate.md) — Measuring demand, throughput and dropped work.
- [E — Error semantics and classification](references/errors.md) — Defining errors or diagnosing rising failure rates.
- [A — Availability and successful user journeys](references/availability.md) — Measuring whether a capability works for users.
- [D — Duration and latency distribution](references/duration.md) — Measuring responsiveness and long-tail delays.
- [S — Saturation and capacity headroom](references/saturation.md) — Measuring approaching limits before widespread failure.
- [READS, RED, USE and golden signals](references/red-use.md) — Selecting complementary monitoring frameworks.
- [SLI, SLO, SLA and error budgets](references/sli-slo.md) — Defining measurable reliability targets.
- [Aggregation, populations and scope](references/aggregation.md) — Combining signals across instances, regions or time.
- [Idle, missing, stale and low-volume signals](references/idle-missing.md) — A zero, gap or unstable ratio appears.
- [READS for queues, streams and batch jobs](references/async-streaming.md) — Work is accepted now and completed later.
- [READS at dependency and fan-out boundaries](references/dependencies.md) — A service calls databases, APIs, tools or other services.
- [READS for AI agents, LLMs and MCP](references/agent-reads.md) — Designing or operating an agentic workflow.
- [READS for CLI tools and libraries](references/cli-library.md) — Instrumenting non-server software.
- [Health reasoning and cross-signal diagnosis](references/health-reasoning.md) — Investigating a READS anomaly.
- [READS completeness and implementation review](references/coverage-review.md) — Reviewing telemetry for a feature or release.
- [Worked READS contract for a request service](references/worked-service.md) — An agent needs a concrete example of measurement design.
