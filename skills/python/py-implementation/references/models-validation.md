# Dataclasses and boundary validation

## Shared guidance
dev-implementation: models-validation

## When to load
Parse external data or establish domain invariants.

## Language-specific decisions
Select dataclasses or ordinary classes for domain values; Pydantic or explicit parsers at boundaries where approved. Define missing versus None, strict coercion and cross-field validation. Convert transport types rather than exposing internal dictionaries.

## Verification and evidence
Test unknown fields, invalid types, coercion, mutable defaults and domain constraints.

## Avoid
Treating successful Pydantic parsing as authorization or full business validation.
