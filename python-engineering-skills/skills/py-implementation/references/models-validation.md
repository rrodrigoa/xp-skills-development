# Data models and validation

## Use when
Structured input crosses a trust or serialization boundary.

## Avoid when
Validating identical trusted data repeatedly at every method.

## Implementation
Use dataclasses for domain values; Pydantic or explicit parsers at external boundaries; TypedDict for dict-shaped contracts. Map DTOs to domain, validate units, range and cross-field invariants.

## Verification and review
Test malformed, missing, extra and valid inputs; never rely on type hints for runtime validation.
