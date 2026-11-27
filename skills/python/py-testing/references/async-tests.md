# Python async testing

## Shared guidance
dev-testing: async-tests

## When to load
Test coroutine and cancellation behavior.

## Language-specific decisions
Use approved pytest-asyncio or IsolatedAsyncioTestCase; control event-loop ownership, signal completion with events rather than sleeps, observe task failures and bound awaits.

## Verification and evidence
Test timeout, cancellation, cleanup, task leaks and repeated runs.

## Avoid
Unawaited coroutines, shared event loops with leaked tasks.
