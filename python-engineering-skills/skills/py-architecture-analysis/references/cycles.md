# Cycles and strongly connected components

## When to load
A dependency graph contains cycles.

## Procedure
Find strongly connected components in the chosen graph, including self-loops where meaningful. Separate runtime cycles from type-only cycles. Inspect shortest representative cycle and identify the dependency responsible for mixed responsibilities. Consider moving a contract to its consumer, extracting a stable value or changing composition.

## Required evidence and acceptance
Report members and edge paths for each cycle, baseline/head changes and impact; verify imports and affected tests after remediation.

## Guardrails
Do not fix by indiscriminate local imports or a shared utils package; not every type-only cycle is a runtime defect.
