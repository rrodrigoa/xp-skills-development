# Python creational pattern mapping

## Shared guidance
oo-patterns: abstract-factory, builder, factory-method, prototype, singleton

## When to load
Construct or scope objects.

## Language-specific decisions
Use factories as callables or typed classes; named constructors and keyword arguments often replace builders. dataclasses.replace is useful for value copies but not deep cloning; make copy ownership explicit. Scope one instance to the composition root rather than relying on global singleton or module cache across processes.

## Verification and evidence
Test factory variants, initialization failure, copy isolation and resource cleanup.

## Avoid
Metaclass singletons, needless builder chains, shared mutable defaults.
