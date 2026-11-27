# Tell, do not ask and Law of Demeter

## When to load
Callers navigate another object's internals or retrieve state to enforce its invariants externally.

## Design procedure
Move decisions that protect a local invariant to its owner. Prefer intention-revealing operations over exposing mutable fields and long navigation chains. A component should depend on its immediate collaborators and stable public contracts, not their internal graph. Queries, immutable projections and DTOs are legitimate: do not replace every getter with a command. Avoid chains that expose ownership, not ordinary fluent composition over stable values.

## Verification
Identify invariant writers and prove clients cannot bypass them through supported APIs. Test behavior without relying on private representation. Review whether a change to nested representation affects unrelated consumers.

## Avoid
Blindly banning getters, fluent APIs or read models; creating forwarding methods that only conceal the same coupling.
