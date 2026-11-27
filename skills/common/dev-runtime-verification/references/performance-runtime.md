# Runtime performance evidence

## When to load
Latency, startup, UI responsiveness or resource change.

## Implementation in the target project
Define representative workload, metrics, warmup, sample sizes, baseline, environment and acceptance thresholds before measuring. Compare distributions and resource use under equivalent conditions; inspect traces for blocking work, allocation or GC. For UI measure interaction latency, startup and long tasks; for services use READS and workload bounds. Preserve raw samples and report noise.

## Required evidence and acceptance
Reproducible benchmark with approved budget, comparable base/candidate and diagnostic traces; regressions explicitly reported.

## Guardrails
No universal performance threshold; do not claim improvement from a single noisy run or synthetic workload alone.
