# Interface segregation

## Use when
Consumers depend on unrelated operations or mocks implement many unused methods.

## Avoid when
Creating a protocol for every single internal helper.

## Implementation
Define narrow client-owned protocols by capability; split read/write only when consumers differ.

## Verification and review
A read-only adapter should need no write stubs.
