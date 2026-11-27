---
name: dev-quality-gates
description: "Evaluate PRs, architecture regressions, test quality, security and delivery evidence; issue reproducible merge recommendations."
---
# Quality Gates

Act as an independent reviewer, not a second implementation agent. Read the applicable approved policy and exact base/head revisions before evaluating. Start with [gate decision protocol](references/decision-protocol.md) and [gate catalog](references/gate-catalog.md); load only relevant checks. Do not modify source, tests, rules, thresholds or approvals to obtain a pass. Report findings with evidence, severity, applicability, exceptions and confidence. A recommendation is not permission to merge; the host owns enforcement.

## Reference selector
Read only the matching cards.

- [Gate decision protocol](references/decision-protocol.md) — Every merge or release evaluation.
- [Stable gate identifiers and default enforcement](references/gate-catalog.md) — Selecting which criteria apply to a project or PR.
- [PR scope and risk intake](references/pr-intake.md) — Beginning review of a change set.
- [Evidence and provenance](references/evidence.md) — Collecting results for a gate evaluator.
- [Architecture boundary and drift gate](references/architecture-gate.md) — Imports, domain ownership or module boundaries change.
- [Reuse, duplication and object design gate](references/reuse-gate.md) — New functions, classes, services or repeated policies are introduced.
- [Complexity and maintainability gate](references/complexity-gate.md) — Changed hotspots or control flow warrant assessment.
- [API and behavior compatibility gate](references/compatibility-gate.md) — Exports, schemas, CLI, exceptions or supported behaviors change.
- [Test execution and failure gate](references/test-execution-gate.md) — Any required suite applies.
- [Test quality and behavioral adequacy gate](references/test-quality-gate.md) — Code or tests change, even if all suites pass.
- [Coverage regression and changed-code gate](references/coverage-gate.md) — Coverage is configured as a quality measure.
- [Mutation testing and flaky-test assessment](references/mutation-flakiness.md) — Assessing whether tests detect defects or produce unstable signals.
- [Security and trust-boundary gate](references/security-gate.md) — Input, authorization, secrets, dependencies or external actions are affected.
- [Supply-chain and dependency gate](references/dependency-gate.md) — Dependencies, build metadata or lockfiles change.
- [Performance, resource and reliability gate](references/performance-gate.md) — Latency, throughput, concurrency, caching or resource behavior changes.
- [Packaging and release readiness gate](references/release-gate.md) — A distributable artifact or release is proposed.
- [Agent, prompt and MCP quality gate](references/agent-change-gate.md) — Model, tool schema, prompts, routing, orchestration or policies change.
- [Review integrity and anti-gaming](references/review-integrity.md) — An agent authored or is evaluating a change.
- [Merge protection and CI integration guidance](references/merge-enforcement.md) — Configuring a host to enforce gate decisions.
- [PR gate evaluator report](references/review-output.md) — Returning review results to a human or downstream agent.
- [Formatting, linting and type quality gate](references/static-quality.md) — Configured static checks apply to changed code.
- [Requirements completeness and delivery gate](references/requirements-gate.md) — A feature, bug fix or agent task is offered as complete.
- [Documentation and contract consistency gate](references/documentation-gate.md) — Public behavior, configuration, operations or architecture changes.

- [READS health contract and coverage gate](references/reads-health-gate.md) — Critical operations, outcomes, load or capacity behavior change.
- [Telemetry correctness, safety and compatibility gate](references/instrumentation-gate.md) — Instrumentation, telemetry schema, context or export changes.
- [Monitoring asset and diagnosis readiness gate](references/monitoring-gate.md) — Dashboards, queries, recording rules or datasource definitions change.
- [Alert actionability, routing and response readiness gate](references/alert-readiness-gate.md) — Alert rules, SLOs, notification policies, runbooks or critical behavior change.

- [Enforceable engineering constraints gate](references/deterministic-constraints-gate.md) — Architecture/API/check changes or repeated defect remediation.
- [Reproducible runtime verification gate](references/deterministic-runtime-gate.md) — Feature or defect changes requiring runtime evidence.
- [Formal property and correspondence evidence gate](references/deterministic-formal-gate.md) — Approved policy requires a model or proof for a critical property.
- [Controlled agent workflow and automation gate](references/deterministic-workflow-gate.md) — Agent graph, verification runner, release automation or self-improvement changes.

## Language-aware evaluation
Identify affected language/build units and the approved project profile. Use the corresponding language testing and delivery overlays to interpret evidence; use design or runtime overlays for changed risks. Evaluate each affected build unit and integration boundary, not just the dominant language. Do not equate compiler success with correctness or treat absence of an optional tool as a failure unless the approved policy requires it. Preserve gate IDs and the shared decision protocol.
