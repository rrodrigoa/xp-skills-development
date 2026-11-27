# TLA+ and bounded model checking

## When to load
Distributed protocol, queue, retry, concurrency or notification flow.

## Implementation in the target project
Use a small abstraction retaining relevant ordering, duplication, failure and recovery. Define Init, Next and properties; configure finite constants, fairness and bounds; run TLC or approved equivalent and retain state counts, options and counterexamples. Check deadlocks and liveness where applicable; vary small configurations and include fault transitions. Map minimized trace to deterministic integration tests.

## Required evidence and acceptance
Checked model and config versions, explored scope, properties, tool output and reproducible counterexample or successful bounded check.

## Guardrails
No claim beyond finite configuration/abstraction; state constraints can hide errors. TLC is not proof of production source code.
