---
name: py-quality-gates
description: "Evaluate PRs, architecture regressions, test quality, security and delivery evidence; issue reproducible merge recommendations."
---
# Python Quality Gates

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
