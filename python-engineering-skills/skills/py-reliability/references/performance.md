# Profiling and performance

## Use when
Measured bottleneck or resource budget.

## Avoid when
Premature caching or rewriting clear Python without measurements.

## Implementation
Profile CPU, allocation and I/O with reproducible workload; optimize algorithm and data structures first; measure before/after; keep behavior tests.

## Verification and review
Report hardware, sample sizes, latency and memory tradeoffs.
