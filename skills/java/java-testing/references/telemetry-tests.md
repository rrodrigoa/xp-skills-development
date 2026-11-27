# Java observability testing and verification

## Shared guidance
dev-observability: verification, telemetry-contract, privacy-audit; dev-reads: coverage-review

## When to load
Testing instrumentation changes before merge or release.

## Procedure
Use JUnit and isolated SDK test exporters/readers or Micrometer test registry supported by installed version; avoid global registry leakage and order-dependent tests. Inject clock/ticker for deterministic duration where appropriate. Assert recorded semantic counts, histogram boundaries, span topology, log fields, errors and context across executors/reactive work. Exercise transaction success/rollback, timeouts, cancellation and retries. Use approved integration environment or Testcontainers where useful to verify real exporter/backend mapping and queries; do not claim live deployment validation from a mock registry.

## Required evidence and acceptance
Actual test results with expected/observed counts and topology, redaction and telemetry failure tests; backend evidence tied to deployment identity where required.

## Guardrails
Do not mock only logger method calls, rely on sleeps for timing, or report unavailable integration evidence as PASS.
