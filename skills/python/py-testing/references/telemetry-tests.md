# Python observability testing and verification

## Shared guidance
dev-observability: verification, telemetry-contract, privacy-audit; dev-reads: coverage-review

## When to load
Testing instrumentation changes before merge or release.

## Procedure
Use approved pytest/unittest fixtures with isolated meter/tracer providers and in-memory exporters/readers supported by installed SDK; do not mutate global providers in a way that leaks across tests. Inject deterministic timing where meaningful and assert actual metric records/spans plus structured logging fields (capture via appropriate fixture). Test async cancellation and concurrent context isolation, multiprocess collection where relevant, known counters/buckets and redaction. For end-to-end evidence run an authorized representative collector/backend, verify translated names, units and query results; distinguish test exporter evidence from deployed evidence.

## Required evidence and acceptance
Actual test results with expected/observed counts and topology, redaction and telemetry failure tests; backend evidence tied to deployment identity where required.

## Guardrails
Do not mock only logger method calls, rely on sleeps for timing, or report unavailable integration evidence as PASS.
