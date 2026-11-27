# Hypothesis and Python coverage

## Shared guidance
dev-testing: property, coverage; dev-quality-gates: coverage-gate, mutation-flakiness

## When to load
Exercise invariants and test effectiveness.

## Language-specific decisions
Use Hypothesis when approved; retain minimized counterexamples. Use coverage.py or configured pytest-cov with branch and source scope recorded; combine parallel worker data correctly.

## Verification and evidence
Report denominator, exclusions, tested revision, failing seeds and mutation results when required.

## Avoid
Coverage percentage as proof of correctness or omitting untested modules.
