# Non-disruptive instrumentation and failure isolation

## When to load
Adding telemetry to a performance-critical path.

## Procedure
Set explicit semantics for telemetry failure: ordinary diagnostics must not replace the business result, mask the original exception or block beyond a bounded budget; required audit paths may intentionally fail closed under policy. Avoid synchronous remote writes on hot paths, unbounded queues, locks around network calls or recursive logging. Reuse handles and limit allocation and expensive formatting. Ensure cleanup and timing happen on all terminal paths while preserving cancellation. Monitor dropped telemetry and backpressure using an independent or bounded self-monitoring mechanism. Specify shutdown flush and exporter resource ownership.

## Required evidence and acceptance
Benchmark with telemetry enabled/disabled and backend down; verify original exceptions, cancellation, memory/CPU overhead, bounded queues and visible drops.

## Guardrails
Do not swallow business errors in instrumentation or silently drop mandatory audit evidence.
