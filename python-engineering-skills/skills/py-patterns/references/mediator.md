# Mediator

## Use when
Components are tightly coupled through many peer interactions.

## Avoid when
A simple direct collaborator or small event list.

## Implementation
Route interactions through focused mediator/coordinator; prevent mediator becoming universal god object.

## Verification and review
Test interaction rules and absence of peer dependencies.

## Refactoring recipe
**Trigger:** Components reference each other through cyclic event coordination.

**Migration:** Map interactions and ownership; introduce coordinator for specific workflow, route one interaction at a time, remove peer links.

**Acceptance:** Test ordering, failure and no duplicate notification; verify reduced cycles.

**Tradeoff:** Avoid central god coordinator; direct communication may be simpler.
