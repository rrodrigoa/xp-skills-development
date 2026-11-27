# Python object and value representation

## Shared guidance
oo-design: object-model, value-objects, behavior-vs-data

## When to load
Domain entities, immutable values and transport models.

## Language-specific decisions
Use ordinary classes for identity and lifecycle; dataclasses for value-like aggregates, frozen where appropriate; enforce invariants during construction and operations. Frozen dataclasses are shallow; copy mutable inputs or choose immutable members. Separate Pydantic boundary models from domain when their concerns differ. A module-level function is natural for a pure calculation.

## Verification and evidence
Check equality, hash stability, invalid construction, mutable aliasing, independent instances and transition failures.

## Avoid
Classes that merely namespace static functions; blanket dataclass conversion of entities.
