# Prototype

## Use when
Create independent objects from configured exemplars.

## Avoid when
Ordinary construction or immutable value copying suffices.

## Implementation
Define explicit clone semantics for owned vs borrowed state; use copy or replace only when safe; do not copy live connections.

## Verification and review
Mutate clone and verify original unaffected where independence promised.

## Refactoring recipe
**Trigger:** Callers repeatedly reconstruct a configured object or mutate shared defaults.

**Migration:** Identify what is immutable, copied, shared or external; define explicit clone semantics, wrap existing creation, migrate callers that need independent variants.

**Acceptance:** Test nested mutable isolation, identity rules and resources that must not be duplicated.

**Tradeoff:** Use immutable replacement or explicit constructor when clearer; never blindly deepcopy locks or connections.
