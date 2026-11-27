# JVM performance, JFR and JMH

## Shared guidance
dev-reliability: performance, observability

## When to load
Investigate Java CPU, allocation or latency regression.

## Language-specific decisions
Use JFR or approved profilers for representative workload; inspect allocation, GC, lock contention and I/O. Use JMH for microbenchmarks with warmup, forks and dead-code safeguards; distinguish heap, native and direct-buffer memory. Tune only against measured bottlenecks.

## Verification and evidence
Record JDK/GC/heap settings, workload, percentile latency, throughput and resource peaks.

## Avoid
Single cold timing or JVM flag changes without before/after evidence.
