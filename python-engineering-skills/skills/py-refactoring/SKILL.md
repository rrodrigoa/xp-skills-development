---
name: py-refactoring
description: "Refactor procedural Python, large modules, god objects, duplicated code, coupling and legacy APIs without behavior regressions."
---
# Python Refactoring

Inventory existing call sites, behavior, state and failure semantics. Add characterization tests before moving code. Refactor in small steps with tests after each step. Move behavior to the actual owner, not a static-method utility class. Keep public compatibility or document approved migration. Measure improvement by cohesion, coupling, duplication and testability, not class count. Avoid unrelated rewrites.

## Reference selector
Read only relevant files from this list.

- [Characterization tests and safe baseline](references/characterization.md) — Legacy behavior is unclear or untested.
- [Procedural-to-object refactoring](references/procedural-to-objects.md) — Functions repeatedly pass mutable context, flags, client and state.
- [Extract method/function](references/extract-method.md) — Long routine has distinct named steps.
- [Extract class](references/extract-class.md) — One class owns multiple distinct lifecycles or policies.
- [Move behavior to owner](references/move-method.md) — Feature envy or behavior depends on another object's internals.
- [Replace conditionals with polymorphism](references/replace-conditionals.md) — Growing type/strategy switch duplicated across operations.
- [Introduce parameter object](references/parameter-object.md) — Same related values travel together across APIs.
- [Consolidate duplicate behavior](references/remove-duplication.md) — Same semantics and fixes repeated in multiple callers.
- [Break cyclic dependencies](references/break-cycles.md) — Imports fail or layers mutually depend.
- [Incremental migration and compatibility](references/legacy-migration.md) — Public legacy API needs structural improvement.
- [Code smells and architecture review](references/review-smells.md) — Reviewing AI-produced or sprawling code.
- [Refactoring plan and risk control](references/refactoring-plan.md) — Multi-file restructuring with external consumers.

For multi-module migrations, generation specifications or checkpoint planning, select `py-migration`. Pattern-specific migration recipes are in `py-patterns`. For a metric-backed architecture inventory use `py-architecture-analysis`.
