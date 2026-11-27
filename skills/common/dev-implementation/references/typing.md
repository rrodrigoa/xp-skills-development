# Type contracts and generics

## Use when
Public API, complex collections or polymorphic boundaries.

## Avoid when
Using Any to suppress errors or over-generic framework code.

## Implementation
Declare public types and meaningful internal boundaries; use generics, interfaces, closed alternatives and domain-specific types where useful. Narrow unknown values before use; check with the configured compiler or type checker.

## Verification and review
Static type checker passes and negative boundary tests validate runtime data.
