# Behavioral objects versus data carriers

## Use when
A proposed model is just fields and accessors, or a service manipulates many unrelated objects.

## Procedure
Classify transport records, immutable values, entities, policies and application services. A transport record intentionally carries data; a value owns equality and validation; an entity owns identity and transitions; a service coordinates external collaborators. Put the rule in the smallest owner with the information required. Avoid forcing persistence annotations or transport fields to dictate the domain model. Use a pure calculation for independent deterministic policy when no lifecycle or polymorphic identity is required.

## Review
Identify a real invariant, all writers, and the operations that protect it. Tests should exercise invalid construction, transitions and independent instances. A record-only DTO is not an anemic domain-model defect; a service that bypasses an entity's invariants is.
