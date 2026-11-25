# Open/closed principle

## Use when
New variants repeatedly require edits to stable dispatch logic.

## Avoid when
One stable conditional with no expected variants.

## Implementation
Extract the actual varying policy behind a protocol or callable; choose implementations at construction. Retain explicit dispatch where the variant set is intentionally closed.

## Verification and review
Add one variant without changing existing policy implementations.
