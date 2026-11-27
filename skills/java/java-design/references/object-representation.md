# Java objects, records and domain models

## Shared guidance
oo-design: object-model, value-objects, behavior-vs-data

## When to load
Choose entity, value, DTO or service.

## Language-specific decisions
Use behavior-owning classes for entities and mutable lifecycle; records for transparent value carriers when supported (records are final and shallowly immutable). Validate constructor arguments and defensively copy mutable members. Define equality and hash semantics intentionally: entity identity is not necessarily every field; mutable equality keys are unsafe. Keep persistence and transport constraints outside domain when warranted.

## Verification and evidence
Test invalid construction, equality/hash contract, collection keys, defensive copying and transitions.

## Avoid
JavaBeans-style setters on invariant-bearing entities or treating all record fields as deeply immutable.
