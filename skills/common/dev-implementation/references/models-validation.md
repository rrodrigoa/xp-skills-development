# Data models and validation

## Use when
Structured input crosses a trust or serialization boundary.

## Avoid when
Validating identical trusted data repeatedly at every method.

## Implementation
Use validated domain value types; schema-based validation or explicit parsers at external boundaries; typed records for transport contracts. Map DTOs to domain, validate units, range and cross-field invariants.

## Verification and review
Test malformed, missing, extra and valid inputs; never rely on type hints for runtime validation.
