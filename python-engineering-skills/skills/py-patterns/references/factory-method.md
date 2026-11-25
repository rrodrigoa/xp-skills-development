# Factory Method

## Use when
A base workflow needs a customizable product creation hook.

## Avoid when
Plain constructor or explicit factory callable is enough.

## Implementation
Define stable workflow and overridable create method; subclass only creation variation. Prefer injected callable when inheritance is not otherwise needed.

## Verification and review
Test workflow with alternate product and failure during construction.

## Refactoring recipe
**Trigger:** A reusable workflow repeatedly branches to create a specialized object.

**Migration:** Isolate creation seam while retaining existing algorithm; define product contract, preserve default creation, introduce override or injected factory and migrate variants.

**Acceptance:** Test workflow with each product, creation failures and stable lifecycle.

**Tradeoff:** Prefer an injected callable over inheritance unless workflow subclasses have independent reason to exist.
