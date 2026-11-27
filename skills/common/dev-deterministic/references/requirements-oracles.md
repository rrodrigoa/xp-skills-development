# Turn requirements into independent oracles

## When to load
A feature or bug fix needs unambiguous acceptance.

## Implementation in the target project
Identify actors, observable inputs/outputs, state, permissions, failures, constraints and non-goals. Assign stable requirement IDs; resolve ambiguous behavior with owner or record assumptions. Derive expected values independently from implementation; map each critical requirement to unit, integration, runtime or formal evidence. For bug fixes demonstrate failure on base before repair. Preserve product intent separately from implementation mechanics.

## Required evidence and acceptance
Every critical requirement has a reproducible assertion or explicit human decision. Negative controls fail, and expected results are not computed by the implementation under test.

## Guardrails
Passing self-derived tests can only show consistency. Do not silently decide ambiguous product behavior.
