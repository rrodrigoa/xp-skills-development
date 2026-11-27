# Java concurrency and async tests

## Shared guidance
dev-testing: async-tests; dev-reliability: async

## When to load
Test executors, futures or concurrent state.

## Language-specific decisions
Use barriers, latches and controlled executors rather than fixed sleeps; bound waits and inspect exceptions from Future/CompletionStage. Assert interrupt, cancellation, resource close and task termination. Use stress tools such as jcstress when appropriate and authorized, separate from deterministic unit tests.

## Verification and evidence
Repeat under representative scheduling, verify no thread/task leaks and document probabilistic limitations.

## Avoid
Flaky sleeps, swallowed execution exceptions or assuming a single run proves race freedom.
