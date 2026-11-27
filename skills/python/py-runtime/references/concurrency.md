# Python threads, processes and asyncio

## Shared guidance
dev-reliability: async, resource-bounds

## When to load
Choose concurrency or parallelism.

## Language-specific decisions
Use asyncio for compatible async I/O, threads for blocking I/O, processes or suitable native code for CPU work as measured. Do not assume GIL behavior across runtimes or free-threaded builds. Keep queues bounded and cancel owned tasks; isolate mutable state.

## Verification and evidence
Measure throughput and saturation, test timeout and cancellation, verify process/thread/task cleanup.

## Avoid
Blocking event loop, unlimited tasks or relying on GIL for atomic compound operations.
