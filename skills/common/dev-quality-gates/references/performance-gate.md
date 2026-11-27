# Performance, resource and reliability gate

## When to load
Latency, throughput, concurrency, caching or resource behavior changes.

## Procedure
Select representative workloads and failure conditions, compare controlled baseline and candidate, report warmup, samples, distribution, environment and resource measurements. Check timeout, cancellation, bounded queues, retry policy and cleanup. Apply approved budgets and uncertainty margins.

## Required evidence and acceptance
Reproducible benchmark or scenario evidence, regression sizes, variance and relevant budget IDs.

## Guardrails
Do not compare incompatible machines or tiny samples as decisive proof. No production load or destructive stress without authorization.
