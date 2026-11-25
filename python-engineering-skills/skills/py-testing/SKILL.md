---
name: py-testing
description: "Design Python unit, integration, contract, end-to-end, property, negative, penetration and regression tests; coverage and test doubles."
---
# Python Testing

Identify public behavior and risk. Choose the smallest test level that proves it, with real integrations where mocks cannot prove contracts. Include positive, negative and boundary cases; security-sensitive paths need adversarial tests. Use deterministic fixtures and explicit assertions. Run focused tests then relevant full suite; report actual failures and unrun environments. Never weaken tests merely to pass.

## Reference selector
Read only relevant files from this list.

- [Testing strategy and risk](references/test-strategy.md) — New feature or project test plan.
- [Unit testing with pytest](references/unit-tests.md) — Testing policy, object invariants and pure functions.
- [Fixtures, fakes, mocks and stubs](references/fixtures-doubles.md) — External or nondeterministic dependencies.
- [Integration tests](references/integration.md) — Real database, filesystem, queue or HTTP contract matters.
- [Contract tests](references/contract.md) — Multiple implementations, versioned APIs or MCP tools.
- [End-to-end and CLI tests](references/e2e.md) — Installed application or full workflow behavior.
- [Property-based and fuzz tests](references/property.md) — Large input space, parsing, invariants or roundtrips.
- [Negative and adversarial tests](references/negative-penetration.md) — Untrusted inputs, permissions, files, tools or network boundaries.
- [Coverage and mutation testing](references/coverage.md) — Quality gates and regression risk.
- [Async and concurrency tests](references/async-tests.md) — Tasks, cancellation, queues or shared state.
- [Regression tests and bug fixes](references/regression.md) — A reproducible defect.
- [Performance tests and benchmarks](references/performance-tests.md) — Latency, throughput or memory goals.
- [Review test quality](references/review-tests.md) — AI-generated tests may assert little or overmock.

For independent review and merge decisions, use `py-quality-gates` rather than self-certifying test adequacy. Apply only approved target-project thresholds.
