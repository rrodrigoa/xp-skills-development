# GRASP Pure Fabrication and Indirection

## When to load
No domain object should directly own a necessary technical or cross-cutting responsibility.

## Design procedure
Introduce a non-domain responsibility (Pure Fabrication), such as a repository adapter or serializer, when it improves cohesion and isolates technology. Use an intermediary (Indirection) when it shields two components from unwanted direct coupling. Name the abstraction by the actual capability and define its lifetime, failure contract and clients. Remove indirection that does not change ownership, translate a contract or isolate meaningful variation.

## Verification
Show which direct dependency is removed, how the new abstraction can be tested, and which client benefits. Verify error propagation and lifecycle at the intermediary.

## Avoid
Pass-through layers with identical signatures and no independent responsibility; a generic service locator hiding dependencies.
