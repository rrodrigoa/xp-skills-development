# Semantic architecture grouping and diagrams

## When to load
Grouping tangled functions, files or graph nodes for human or agent comprehension.

## Procedure
Cluster by responsibility, shared state, callers, domain language and change coupling. Preserve original symbol IDs and all source edges; mark inferred groups with rationale and confidence. Use hierarchical package, component and symbol views with explicit cross-group dependencies.

## Required evidence and acceptance
Deliver mapping of each item to group, unassigned/ambiguous items, representative evidence and graph provenance; validate that grouping does not hide forbidden edges.

## Guardrails
A semantic group is a hypothesis, not a proposed class by default. Never invent edges or remove dependencies for visual cleanliness.
