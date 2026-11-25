# Visitor

## Use when
New operations frequently target a stable set of node types.

## Avoid when
Node types change frequently or simple singledispatch suffices.

## Implementation
Use visitor protocol and accept for double dispatch; keep operations outside node model; consider match/singledispatch for closed sets.

## Verification and review
Test every node/operation combination and missing handler behavior.

## Refactoring recipe
**Trigger:** New operations frequently add type checks across stable node types.

**Migration:** Inventory node types and operations, establish explicit dispatch contract, migrate one operation, verify handling for all nodes.

**Acceptance:** Test every supported type, unknown extension behavior and result equivalence.

**Tradeoff:** Use polymorphism when adding new node types is more common; consider singledispatch for simple cases.
