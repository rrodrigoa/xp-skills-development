---
name: dev-architecture-analysis
description: "Audit software architecture, dependency graphs, coupling, cohesion, complexity, contracts, and architectural regressions."
---
# Architecture Analysis

Read the project policy and identify the baseline revision, scope and architecture intent. Separate directly observed relationships from inferred semantic groups. Use the repository's available static and runtime analysis tools; this skill provides no analyzer. Report metric definitions, scope, exclusions, coverage gaps, paths and examples. Never treat metrics alone as proof of bad design. Use the contract card for normative rules, not heuristics. For a PR compare the same measurements at base and head, then route violations to `dev-quality-gates`.

## Reference selector
Read only the matching cards.

- [Architecture inventory and system map](references/inventory.md) — Starting an architecture assessment or unfamiliar repository.
- [Import dependency graph](references/import-graph.md) — Inspecting dependencies or cross-package leakage.
- [Call graph and data flow](references/call-data-graph.md) — Tracing behavior, mutable state or external effects.
- [Cycles and strongly connected components](references/cycles.md) — A dependency graph contains cycles.
- [Coupling and dependency stability](references/coupling.md) — Evaluating dependency concentration or package fragility.
- [Cohesion and responsibility analysis](references/cohesion.md) — A module or class appears to contain unrelated behavior.
- [Complexity and nesting](references/complexity.md) — Reviewing complicated control flow or hotspots.
- [Procedural density and OO smells](references/procedural-density.md) — Investigating function-heavy modules or static-heavy classes.
- [Duplication and semantic reuse](references/duplication.md) — Investigating copy-paste and repeated domain policies.
- [Change hotspots and temporal coupling](references/change-hotspots.md) — Prioritizing maintenance across repository history.
- [Public API surface and leakage](references/api-surface.md) — Assessing reusable libraries or cross-module contracts.
- [Architecture contract authoring](references/architecture-contracts.md) — Defining enforceable dependency and ownership rules.
- [Architecture fitness criteria](references/fitness-functions.md) — Turning architecture intentions into repeatable checks.
- [Architecture drift and regression](references/architecture-drift.md) — Comparing a PR or release with accepted architecture.
- [Semantic architecture grouping and diagrams](references/semantic-grouping.md) — Grouping tangled functions, files or graph nodes for human or agent comprehension.
- [Architecture audit report and prioritization](references/audit-report.md) — Delivering a review to an implementation agent or owner.

- [Polyglot architecture inventory](references/polyglot-boundaries.md) — Load for this specific topic.
