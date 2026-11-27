# Value objects and entities

## Use when
Primitive values carry units, validation or identity.

## Avoid when
Wrapping every string or integer without domain meaning.

## Implementation
Use immutable value types with validated construction and value equality. Entities have explicit identity and controlled mutation. Immutability may be shallow; use immutable members or defensive copies.

## Verification and review
Test equality, hashing where supported, invalid values and entity identity.
