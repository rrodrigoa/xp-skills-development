# Java threads, executors and virtual threads

## Shared guidance
dev-reliability: async, resource-bounds

## When to load
Choose blocking or asynchronous execution.

## Language-specific decisions
Use executor ownership, bounded work admission and deadlines. Virtual threads are available on supported JDKs (final since 21) and can simplify blocking I/O; do not pool them merely to limit concurrency—bound scarce resources independently. CPU-bound work remains constrained by cores. Check actual JDK behavior and framework support; avoid assuming preview structured concurrency APIs are available.

## Verification and evidence
Measure representative load, queue pressure, cancellation, task failure and shutdown; verify JDK matrix.

## Avoid
Unbounded platform thread creation, treating virtual threads as unlimited connections or assuming faster CPU work.
