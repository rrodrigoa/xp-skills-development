# Iterator

## Use when
Consumers traverse a collection without depending on storage.

## Avoid when
List iteration already exposes correct semantics.

## Implementation
Use the language-native iteration contract and lazy traversal where useful; define one-shot vs repeatable iteration and lazy resource lifetime.

## Verification and review
Test empty, repeatability and early termination as contract requires.

## Refactoring recipe
**Trigger:** Callers know storage internals merely to traverse objects.

**Migration:** Identify ordering, lazy/eager behavior, snapshot versus live view; expose iteration contract and migrate consumers from storage-specific access.

**Acceptance:** Test empty, repeat traversal, mutation behavior and cleanup of resource-backed iterators.

**Tradeoff:** Use native iteration/generators unless custom state has real purpose.
