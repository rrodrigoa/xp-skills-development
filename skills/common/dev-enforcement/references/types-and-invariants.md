# Type and compiler constraints

## When to load
Invalid states, wrong units or unchecked variants.

## Implementation in the target project
Use meaningful types, explicit sums/enums, value objects and constructors to constrain representations; validate external data at boundaries. Make required transitions and capabilities explicit. Enable approved compiler/type rules in scope; test negative compile/type fixtures and runtime rejection of untyped input. Check serialization and version compatibility.

## Required evidence and acceptance
Invalid representation is rejected through supported entry points; valid variants compile and execute; unchecked or dynamic escapes documented.

## Guardrails
Type annotations without checking do not enforce behavior. Type safety does not establish authorization or distributed invariants.
