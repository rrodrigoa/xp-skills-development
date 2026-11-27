---
name: dev-engineering
description: "Route software engineering tasks; apply mandatory quality rules, select minimal references, plan changes and verify results."
---
# Development Engineering

1. Read repository instructions and inspect existing package boundaries, tests, configuration and public APIs. Never replace local conventions without justification.
2. Classify task by intent using the route table. Load the relevant skill and only its matching references. For small changes, avoid architecture work unrelated to the request.
3. For changes involving state, policy, external I/O or multiple callers, explicitly identify owners, collaborators and dependency direction before editing. Prefer a pure function for genuinely stateless operations.
4. Make a small vertical change including implementation and behavioral tests. Reuse existing abstractions first. Maintain compatibility unless the user authorizes a break.
5. Run configured checks; inspect the diff for duplication, boundary leaks, suppressed errors, fabricated results and incomplete work. Report commands, outcomes and unverified gaps. Never claim a gate passed without evidence.

| Task | Start with | Add only if relevant |
|---|---|---|
| New subsystem, domain, service | oo-design | oo-patterns, dev-testing |
| Choose or implement a pattern | oo-patterns | oo-design, dev-testing |
| Feature, library, API, CLI | dev-implementation | oo-patterns, dev-testing |
| Existing procedural or tangled code | dev-refactoring | oo-design, oo-patterns, dev-testing |
| Test, regression, coverage | dev-testing | dev-reliability |
| Build, package, CI, release | dev-delivery | dev-testing, dev-reliability |
| Security, concurrency, performance | dev-reliability | dev-testing |
| Agents, MCP, LLM tools | dev-agent-systems | oo-design, dev-reliability, dev-testing |
| Architecture audit, metrics, dependency graphs | dev-architecture-analysis | oo-design, dev-quality-gates |
| Pattern migration, generation blueprint, codemod plan | dev-migration | dev-refactoring, oo-patterns |
| Independent PR or release gate | dev-quality-gates | dev-architecture-analysis, dev-testing |
| Policy, agent orchestration, baselines, exceptions | dev-governance | dev-quality-gates |
| Service health, READS, SLI/SLO, health diagnosis | dev-reads | dev-observability |
| Instrumentation, metrics/logs/traces, telemetry refactor | dev-observability | dev-reads, dev-testing |
| Grafana dashboard, datasource, query or drilldown | dev-grafana | dev-reads, dev-observability |
| Alert rule, notification, SLO burn, incident response | dev-alerting | dev-reads, dev-grafana |
| Establish deterministic development, recurring agent mistake | dev-deterministic | dev-enforcement, dev-runtime-verification |
| Custom lint, machine constraints, architecture checks, CI | dev-enforcement | dev-deterministic, dev-quality-gates |
| Runnable application, feature maps, UI/CLI/API verification | dev-runtime-verification | dev-testing, dev-reads |
| Invariants, TLA+, Lean, model checking or proof | dev-formal-verification | dev-runtime-verification, dev-quality-gates |
| Agent graph, bounded repair, release fuzzing, factory | dev-agent-factory | dev-deterministic, dev-governance |

Context budget: initially load at most two detailed references; expand only to resolve concrete questions. Do not recursively load directories. Preserve selected paths, decisions and verification state in a compact task note if context is compacted. Never omit a relevant security or verification requirement merely to satisfy this soft budget.

Role boundary: reviewer and gate agents must not edit code or alter thresholds unless explicitly reassigned and independently reviewed. Use approved policy and revision-bound evidence. Missing evidence is not a pass. This repository supplies instructions only; perform authorized work using target-project tools, never expect a bundled runtime.

## Select language overlays only after intent
Determine the language and build unit from actual source/build metadata, not the user's wording alone. Shared skills define the engineering decision; a language overlay supplies idioms and tools. Start with the relevant shared skill and one overlay when a language-dependent decision is needed.

| Task | Python overlay | Java overlay |
|---|---|---|
| OO design, patterns, architecture analysis | py-design | java-design |
| Naming, APIs, CLI, libraries, refactoring mechanics | py-implementation | java-implementation |
| Test strategy implementation and evidence | py-testing | java-testing |
| Build, dependencies, CI, release, compatibility | py-delivery | java-delivery |
| Concurrency, resources, security, performance | py-runtime | java-runtime |

For feature planning, load the local [requirements and vertical slicing](references/requirements-slicing.md) card. For mixed-language work, route separately by component and load the shared integration contract card from `dev-implementation` when wire or process boundaries change. For other languages use common guidance and the target's verified conventions; do not substitute Python or Java rules. A shared skill name is a logical identifier discoverable by the host, not a fixed relative path. In a source checkout look under skills/common, skills/python or skills/java; installed skill directories may be flattened by the host.

## Observability routing
For features that change critical operations, failure paths, dependencies, queues or capacity, inspect the existing health contract and telemetry consumers before editing. Start with dev-reads health-contract and dev-observability instrumentation-plan; select only impacted dimensions and a runtime/testing overlay when language-specific evidence is needed. For monitoring-only requests start with dev-grafana or dev-alerting; use dev-reads to interpret outcomes. For incidents verify scope, freshness and permissions first, and separate diagnosis from production changes. Apply OBS-01 through OBS-04 only under the approved profile; report unknown evidence. Do not load all four skills by default.

## Deterministic development routing
For a repeated correction or nontrivial new feature, consider whether an existing enforceable API or check can express the requirement. When asked to establish deterministic engineering in a target repo, start with dev-deterministic bootstrap and implementation-loop; implement authorized project-specific constraints and checks, not just documentation. Select dev-enforcement for mechanical rules, dev-runtime-verification for real execution, dev-formal-verification for justified properties and dev-agent-factory only after the inner loop works. The DET gates supplement existing IDs when explicitly adopted. A deterministic verifier is not a model opinion; preserve independent review and evidence semantics.
