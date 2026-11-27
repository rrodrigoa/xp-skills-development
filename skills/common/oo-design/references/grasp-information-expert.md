# GRASP Information Expert and Creator

## When to load
Selecting a responsibility owner or deciding where construction belongs.

## Design procedure
Assign a behavior to the object that already owns the information and invariants required for it (Information Expert). Assign creation to a component that aggregates, contains, closely uses or knows the initialization data for the created object (Creator), provided that this does not introduce an unwanted dependency. For an external dependency or complex creation policy, use a composition root or factory. Separate invariant ownership from workflow coordination: an application service may coordinate several entities without owning their local rules.

## Verification
List information read and mutated, dependencies needed and the candidate owner. Test the behavior directly at that boundary. Verify that the chosen owner does not depend on presentation or infrastructure merely to obtain unrelated data.

## Avoid
Moving everything into a service that retrieves fields and mutates objects; conversely, forcing a domain entity to construct a database adapter because it has an identifier.
