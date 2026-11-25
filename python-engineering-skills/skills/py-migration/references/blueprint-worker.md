# Background worker and pipeline blueprint

## When to load
Designing reusable asynchronous processing or jobs.

## Procedure
Define typed work item, state ownership, queue semantics, scheduling, concurrency/backpressure, idempotency and retries, cancellation, recovery and observability. Separate processing strategy from infrastructure and enforce transaction/acknowledgement ordering.

## Required evidence and acceptance
Test duplicate delivery, timeout, cancellation, crash/restart, capacity and invalid transitions; document delivery guarantees.

## Guardrails
Do not claim exactly-once delivery without evidence. No unbounded queues, retries or detached tasks.
