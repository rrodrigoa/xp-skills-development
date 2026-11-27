# Abstract Factory

## Use when
A family of compatible products must vary together.

## Avoid when
One independent product or simple constructor.

## Implementation
Define family interface returning related products; inject concrete factory at bootstrap; keep product compatibility explicit.

## Verification and review
Test each family for compatible products; client remains unchanged.

## Refactoring recipe
**Trigger:** A client independently chooses storage, serializer and transport variants that must be compatible.

**Migration:** Characterize supported combinations and invalid mixtures; introduce a family contract, wrap the old constructors as one concrete factory, migrate composition root and add a second family only when needed.

**Acceptance:** Verify each family produces mutually compatible products, unknown selection fails and no client branches on family.

**Tradeoff:** Keep independent constructor choices if no family invariant exists.
