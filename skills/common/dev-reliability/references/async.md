# Async, threads and processes

## Use when
I/O concurrency or CPU parallelism.

## Avoid when
Async wrapping blocking I/O or unbounded task creation.

## Implementation
Choose the concurrency model based on workload, cancellation semantics and runtime capabilities; structured concurrency, semaphores and deadlines; synchronize shared mutable state.

## Verification and review
Test cancellation, overload, ordering where required and cleanup.
