# Async and concurrency tests

## Use when
Tasks, cancellation, queues or shared state.

## Avoid when
Sleep-based race tests.

## Implementation
Use events/barriers, fake clocks where practical, bounded awaits and pytest-asyncio or stdlib IsolatedAsyncioTestCase. Ensure task exceptions observed.

## Verification and review
Assert cancellation, cleanup, contention and no leaked tasks.
