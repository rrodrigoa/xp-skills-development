# Import dependency graph

## When to load
Inspecting dependencies or cross-package leakage.

## Procedure
Resolve language-level dependencies against declared package and module roots. Record source, target, file and line; classify compile-time, runtime, optional, conditional, re-export and dynamically resolved edges. Aggregate at module and package levels without losing edge provenance. Inspect entry points and plugin registration for additional edges.

## Required evidence and acceptance
Provide directed edges, unresolved imports and exclusions; verify sample edges against source and report strongly connected components.

## Guardrails
An import graph is not a call graph; lazy imports can conceal rather than fix coupling. Do not claim completeness for dynamic imports.

For a mixed-language system, model source imports, compiled dependencies, build-module dependencies, generated clients, reflection/service discovery and runtime calls as distinct edge kinds. Link only proven cross-language edges through explicit schemas, RPC endpoints, bindings or subprocess protocols. Use the language design/delivery overlay for extraction methods and their limits.
