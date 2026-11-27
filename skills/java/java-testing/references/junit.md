# JUnit platform and test organization

## Shared guidance
dev-testing: unit-tests, test-strategy

## When to load
Add Java unit and behavioral tests.

## Language-specific decisions
Use project-selected JUnit version and engine; JUnit Jupiter parameterized tests cover variants and boundaries. Keep fixtures minimal, assert state and observable outcomes, and use assertThrows with useful type/details. Separate test lifecycle from shared mutable state.

## Verification and evidence
Verify actual engine discovery, nonzero counts, failing behavior and deterministic repeated runs.

## Avoid
Tests silently ignored due to engine mismatch or no meaningful assertions.
