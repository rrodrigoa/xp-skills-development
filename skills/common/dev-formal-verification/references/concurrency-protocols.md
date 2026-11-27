# Concurrency and distributed protocol invariants

## When to load
Locks, leases, workflows, retries and messaging.

## Implementation in the target project
Model ownership, epochs, deadlines, in-flight effects, duplicate/reordered messages, crash recovery and fairness. Specify mutual exclusion, monotonicity, no lost committed work and eventual completion under explicit availability assumptions. Explore small concurrent populations and adverse schedules; derive concrete fault tests and monitor relevant READS signals.

## Required evidence and acceptance
Safety/liveness claims separated; bounded checks and runtime tests identify explored faults and assumptions.

## Guardrails
Do not assume exactly-once delivery, synchronized clocks or fair scheduling unless guaranteed and validated.
