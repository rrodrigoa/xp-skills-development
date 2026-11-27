# Architecture inventory and system map

## When to load
Starting an architecture assessment or unfamiliar repository.

## Procedure
Identify packages, public entry points, owners, processes, storage, external services, runtime composition and test boundaries. Trace representative operations from presentation to effects. Label current versus intended architecture; distinguish generated/vendor code and optional extras.

## Required evidence and acceptance
Produce a scoped package map, responsibility table, entry-point traces and evidence locations; state what was not inspected.

## Guardrails
Do not infer service boundaries from folder names alone; confirm actual behavior and runtime wiring.

## Observability inventory
Map critical journeys to instrumentation boundaries and ownership, collectors, stores, dashboards, SLOs, alert evaluators and notification routes. Identify trust and failure boundaries, missing-signal risks and dependency saturation. Use dev-reads health-contract and dev-observability instrumentation-plan; keep telemetry dependency direction explicit.
