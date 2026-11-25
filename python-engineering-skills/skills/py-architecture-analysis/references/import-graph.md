# Import dependency graph

## When to load
Inspecting dependencies or cross-package leakage.

## Procedure
Resolve absolute and relative imports against the declared package roots. Record source, target, file and line, and classify runtime, type-only, optional, conditional, re-export and dynamic imports. Aggregate at module and package levels without losing edge provenance. Inspect entry points and plugin registration for additional edges.

## Required evidence and acceptance
Provide directed edges, unresolved imports and exclusions; verify sample edges against source and report strongly connected components.

## Guardrails
An import graph is not a call graph; lazy imports can conceal rather than fix coupling. Do not claim completeness for dynamic imports.
