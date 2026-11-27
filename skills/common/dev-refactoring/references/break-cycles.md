# Break cyclic dependencies

## Use when
Imports fail or layers mutually depend.

## Avoid when
Hiding cycles via deferred imports alone.

## Implementation
Identify dependency direction; move consumer-owned protocol or shared domain value; compose at root; remove module import side effects.

## Verification and review
Cold imports and import graph pass.
