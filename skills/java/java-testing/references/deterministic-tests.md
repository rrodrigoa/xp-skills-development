# Java deterministic tests and reproducible failures

## When to load
Testing nondeterministic behavior and rule enforcement.

## Implementation in the target project
Use dev-runtime-verification controlled-time and property-fuzz. Inject java.time.Clock and random source; use explicit latches/barriers and bounded futures; use JUnit isolation, jqwik properties with reported seeds/shrinking and Testcontainers where approved. Verify Surefire/Failsafe or Gradle discovery and actual negative cases.

## Required evidence and acceptance
Replay failing case with tool and JDK version; independent check confirms discovered tests, failures and skipped reasons.

## Guardrails
Do not rely on Thread.sleep for synchronization or assume one schedule proves thread safety.
