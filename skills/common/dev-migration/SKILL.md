---
name: dev-migration
description: "Plan pattern-driven refactoring, reusable design blueprints, code generation specifications and safe automated migrations."
---
# Migration

Use `dev-refactoring` for local techniques and `oo-patterns` for the pattern-specific prose migration steps. This skill covers cross-module changes and specifications for generation/migration agents, not actual generators. Start with behavior and risk inventory, then define a narrow target design, characterize, migrate callers incrementally and remove obsolete paths when authorized. Separate mechanical changes from semantic changes; inspect diffs and validate on each checkpoint.

## Reference selector
Read only the matching cards.

- [Refactoring recipe selection](references/recipe-selection.md) — Selecting a transformation from observed design problems.
- [Safe automated mechanical changes](references/mechanical-migration.md) — Planning a rename, move, import rewrite or other repetitive migration.
- [Semantic migrations and invariant changes](references/semantic-migration.md) — Changing behavior ownership or representation across modules.
- [Branch by abstraction](references/branch-by-abstraction.md) — Replacing a dependency or implementation while keeping releases viable.
- [Expand, migrate, contract](references/parallel-change.md) — Changing a public interface or persistent schema with independent consumers.
- [Incremental subsystem replacement](references/strangler.md) — Replacing a legacy service or module without a big-bang rewrite.
- [Procedural service to domain/application objects](references/procedural-service.md) — Shared context and utility functions implement a service lifecycle.
- [Reusable generation specification](references/blueprint-specification.md) — Instructing an agent to generate a reusable component or project slice.
- [Reusable library blueprint](references/blueprint-library.md) — Designing or extracting a library from application code.
- [Reusable CLI tool blueprint](references/blueprint-cli.md) — Generating or refactoring a CLI over a library.
- [API and adapter blueprint](references/blueprint-api.md) — Exposing existing application capabilities over HTTP, RPC or another interface.
- [MCP and autonomous tool blueprint](references/blueprint-agent-tool.md) — Exposing a reusable capability to agents.
- [Plugin and extension blueprint](references/blueprint-plugin.md) — Designing selectable providers or a plugin architecture.
- [Background worker and pipeline blueprint](references/blueprint-worker.md) — Designing reusable asynchronous processing or jobs.
- [Migration checkpoints and rollback](references/rollback-checkpoints.md) — Planning multi-step changes or risky refactors.
