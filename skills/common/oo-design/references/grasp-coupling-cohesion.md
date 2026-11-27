# GRASP Low Coupling and High Cohesion

## When to load
Responsibilities are distributed across too many collaborators or concentrated in a god object.

## Design procedure
Group operations that change for the same reason or preserve the same invariant. Identify fan-out, state writers, change hotspots and dependency directions. Prefer stable narrow capabilities at external boundaries. A tightly cohesive component can legitimately have several methods; a small wrapper with no responsibility adds coupling without benefit. Compare alternatives by impact of a representative change and ease of independent tests.

## Verification
Record dependency and responsibility changes before/after, inspect changed callers and run behavioral tests. Use coupling/cohesion metrics as triage, not absolute cross-language quality measures.

## Avoid
Creating one class per method, flattening every object into one orchestrator, or introducing an interface solely to improve a metric.
