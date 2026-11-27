# Python dependency and ownership analysis

## Shared guidance
dev-architecture-analysis: import-graph, procedural-density, cycles

## When to load
Audit modules and hidden coupling.

## Language-specific decisions
Resolve packages using actual source roots; inspect relative imports, __all__, TYPE_CHECKING, optional imports and entry points. Distinguish top-level pure functions, stateful functions, bound methods and static methods. AST and Import Linter can provide evidence but dynamic imports and monkeypatching require separate inspection.

## Verification and evidence
Record edge provenance, unresolved paths, generated exclusions and changed baselines; sample dynamic edges at runtime if authorized.

## Avoid
Class quotas or relying on import graph as a call graph.
