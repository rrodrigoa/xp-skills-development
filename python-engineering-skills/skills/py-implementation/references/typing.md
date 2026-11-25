# Type annotations and generics

## Use when
Public API, complex collections or polymorphic boundaries.

## Avoid when
Using Any to suppress errors or over-generic framework code.

## Implementation
Annotate public functions and meaningful internal boundaries; use Protocol, TypeVar, narrow unions, Literal and NewType as appropriate. Use object plus narrowing for unknown values; check with configured type checker.

## Verification and review
Static type checker passes and negative boundary tests validate runtime data.
