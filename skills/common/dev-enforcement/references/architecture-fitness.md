# Executable architecture fitness rules

## When to load
Layer, module or dependency constraints.

## Implementation in the target project
Translate approved architecture contract into dependency rules. Collect import/build and dynamic registration edges as appropriate, resolve transitive dependencies and distinguish allowed adapter/composition edges. Fixture a direct and transitive illegal edge, allowed edge and unresolved dependency. Compare with baseline and prevent new violations; treat analyzer coverage gaps as unknown.

## Required evidence and acceptance
Report rule IDs, graph/tool version, fixture results, violations and analysis exclusions; CI consumes exact outcome.

## Guardrails
A directory layout alone is not enforcement. Static analysis misses reflection and runtime wiring.
