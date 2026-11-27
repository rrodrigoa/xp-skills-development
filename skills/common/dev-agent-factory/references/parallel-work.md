# Parallel agent orchestration and conflict management

## When to load
Multiple agents implement or verify changes.

## Implementation in the target project
Partition by ownership and dependencies; assign separate branches/workspaces, stable task IDs and shared contract version. Schedule dependent tasks after interfaces settle; prevent conflicting writes with leases/ownership; integrate incrementally and revalidate combined candidate. Enforce per-agent and aggregate budget, cancellation, deduplication and failure isolation.

## Required evidence and acceptance
Collision, stale-base, duplicate job and integration failure tests demonstrate safe behavior; final evidence applies to combined tree.

## Guardrails
Do not infer compatibility from independently green branches. More concurrency is not necessarily higher quality.
