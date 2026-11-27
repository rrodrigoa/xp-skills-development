# Java creational patterns

## Shared guidance
oo-patterns: abstract-factory, builder, factory-method, prototype, singleton

## When to load
Choose construction policy and lifetime.

## Language-specific decisions
Use Supplier or named factory for simple creation; builders for meaningful staged or multi-parameter construction with validation on build. Factory Method uses a stable inherited workflow only if justified. Prototype needs explicit copy semantics; copy constructor or factory usually clearer than Cloneable. Prefer DI-scoped instance; enum singleton only for genuinely process-local stateless/safe state.

## Verification and evidence
Test creation variants, invalid combinations, failed initialization, defensive copy and scope boundaries.

## Avoid
Builder for every record, global singleton for request state, assuming singleton spans JVMs/class loaders.
