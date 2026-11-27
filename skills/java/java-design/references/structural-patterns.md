# Java structural patterns

## Shared guidance
oo-patterns: adapter, bridge, composite, decorator, facade, flyweight, proxy

## When to load
Compose wrappers, translate interfaces or organize recursive models.

## Language-specific decisions
Use explicit delegation with interface compatibility. Decorators wrap behavior and ordering; annotations or dynamic proxies are implementation techniques, not substitutes for contracts. Separate bridge axes; expose narrow facades. Flyweights share immutable intrinsic state; proxy access checks must cover all call paths.

## Verification and evidence
Test interface substitution, wrapper ordering, recursive traversal, equality and resource ownership; inspect proxy interception limitations.

## Avoid
Inheritance merely to reuse a method; framework proxy assumed to intercept self-invocation.
