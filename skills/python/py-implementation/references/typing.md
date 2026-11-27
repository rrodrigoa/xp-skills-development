# Python type contracts

## Shared guidance
dev-implementation: typing; oo-design: protocols-abcs

## When to load
Public APIs and dynamic boundaries.

## Language-specific decisions
Use annotations, Protocol, TypeVar, Literal, NewType and narrow unions as needed; respect minimum Python version for newer syntax. Narrow object values before use. Avoid unchecked Any and broad casts; use TypedDict for dict-shaped boundary contracts.

## Verification and evidence
Run configured mypy or Pyright on relevant roots and inspect new ignores.

## Avoid
Annotations treated as runtime validation; gratuitous generics.
