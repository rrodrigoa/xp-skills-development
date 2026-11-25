# Async, threads and processes

## Use when
I/O concurrency or CPU parallelism.

## Avoid when
Async wrapping blocking I/O or unbounded task creation.

## Implementation
Use asyncio for async I/O, threads for blocking I/O, processes for CPU when appropriate; structured concurrency, semaphores and deadlines; synchronize shared mutable state.

## Verification and review
Test cancellation, overload, ordering where required and cleanup.
