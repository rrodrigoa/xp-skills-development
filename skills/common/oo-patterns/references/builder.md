# Builder

## Use when
Construction has ordered steps or many optional values with final validation.

## Avoid when
A simple validated constructor or named factory is enough.

## Implementation
Keep intermediate state private; build validates completeness and returns independent product; prefer immutable result.

## Verification and review
Test incomplete input and builder reuse without shared mutable state.

## Refactoring recipe
**Trigger:** A complex request is assembled through inconsistent optional arguments and partial mutation.

**Migration:** Capture defaults and required fields; separate incremental assembly from immutable final product; validate cross-field rules on build, migrate construction sites, keep convenience constructor for simple cases.

**Acceptance:** Test missing required values, invalid combinations, reuse/reset and immutability of built objects.

**Tradeoff:** Use an immutable value type or named constructor if there is no meaningful construction workflow.
