# Java serialization and wire contracts

## Shared guidance
dev-implementation: serialization, cross-language-contracts

## When to load
Exchange JSON or binary records.

## Language-specific decisions
Prefer explicit schema mapping using approved Jackson or codec; avoid native Java object deserialization of untrusted input. Restrict polymorphic type selection; distinguish missing/null, enum evolution, BigDecimal precision and Instant/time zone. Keep transport DTOs separate from internal entities.

## Verification and evidence
Round-trip fixtures with Python or other consumers, unknown fields, precision, malformed input and incompatible versions.

## Avoid
Unrestricted polymorphic deserialization or exposing ORM graph by default.
