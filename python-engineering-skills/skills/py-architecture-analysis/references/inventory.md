# Architecture inventory and system map

## When to load
Starting an architecture assessment or unfamiliar repository.

## Procedure
Identify packages, public entry points, owners, processes, storage, external services, runtime composition and test boundaries. Trace representative operations from presentation to effects. Label current versus intended architecture; distinguish generated/vendor code and optional extras.

## Required evidence and acceptance
Produce a scoped package map, responsibility table, entry-point traces and evidence locations; state what was not inspected.

## Guardrails
Do not infer service boundaries from folder names alone; confirm actual behavior and runtime wiring.
