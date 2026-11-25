# Value objects and entities

## Use when
Primitive values carry units, validation or identity.

## Avoid when
Wrapping every string or integer without domain meaning.

## Implementation
Use frozen dataclasses for value semantics; enforce invariants in __post_init__. Entities have explicit identity and controlled mutation. Frozen is shallow; choose immutable fields.

## Verification and review
Test equality, hashing where supported, invalid values and entity identity.
