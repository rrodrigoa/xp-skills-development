# Python behavioral pattern mapping

## Shared guidance
oo-patterns: strategy, command, observer, iterator, visitor, state, interpreter, mediator, memento, template-method, chain-of-responsibility

## When to load
Dispatch, iterate, compose workflows or vary policies.

## Language-specific decisions
Use callables for simple strategies/commands and objects for stateful ones. Native __iter__, generators and async iteration handle traversal; specify one-shot and resource lifetime. For closed variants consider match or singledispatch where supported; use visitor for stable hierarchies with evolving operations. Use explicit unsubscribe and bounded delivery for observers.

## Verification and evidence
Test each variant, cancellation, exhaustion, invalid transitions and subscriber failures.

## Avoid
Java-style boilerplate for simple callables; dynamic dispatch with no unsupported-case handling.
