# Call graph and data flow

## When to load
Tracing behavior, mutable state or external effects.

## Procedure
Start from public entry points and trace calls to domain operations, collaborators and side effects. Mark static resolution, inferred dispatch and runtime-observed edges separately. Trace data ownership, mutation and validation across boundaries, including callbacks and asynchronous execution.

## Required evidence and acceptance
Show representative successful and failing paths with symbol locations, state owners and trust boundaries; list unresolved dynamic dispatch.

## Guardrails
Do not invent dispatch targets. Runtime traces cover only executed scenarios, not every possible path.
