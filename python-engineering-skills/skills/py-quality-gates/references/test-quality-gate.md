# Test quality and behavioral adequacy gate

## When to load
Code or tests change, even if all suites pass.

## Procedure
Map changed behavior and risk to assertions; inspect positive, negative, boundary, state transitions, failure, cancellation and relevant adversarial cases. Check test doubles represent contract and that assertions fail for plausible defects. Look for disabled assertions, broad mocks and tests that mirror implementation.

## Required evidence and acceptance
Behavior-to-test matrix, gaps with locations, evidence of meaningful assertions and required new scenarios.

## Guardrails
Do not require all test types for trivial changes. Do not block purely on test count or subjective style unless policy specifies it.
