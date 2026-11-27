# Python performance and diagnostics

## Shared guidance
dev-reliability: performance, observability

## When to load
Investigate CPU, memory or I/O regressions.

## Language-specific decisions
Use project-approved profiler, tracemalloc or sampling tools; distinguish Python allocations from native memory and process RSS. Use representative data, warmup where appropriate and repeatable environment.

## Verification and evidence
Record workload, runtime, distributions, resource peaks and bottleneck evidence.

## Avoid
Rewriting readable Python without measurements or extrapolating one microbenchmark.
