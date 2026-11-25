# Composite

## Use when
Tree of objects needs uniform operations across leaves and groups.

## Avoid when
Flat collection or different leaf/group behavior.

## Implementation
Define common operation; composite delegates recursively to children; guard cycles and mutation as needed.

## Verification and review
Test empty, nested and leaf behavior; reject cycles if mutable.

## Refactoring recipe
**Trigger:** Recursive structures require type switches for leaves and groups.

**Migration:** Define common operation and ownership semantics; model leaf and container separately; migrate recursive traversal; validate cycles and sharing constraints.

**Acceptance:** Test empty, nested and leaf structures, ordering, cycle rejection and failure propagation.

**Tradeoff:** Do not force uniform operations that have no meaning for a leaf.
