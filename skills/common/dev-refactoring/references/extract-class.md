# Extract class

## Use when
One class owns multiple distinct lifecycles or policies.

## Avoid when
Splitting by line count only.

## Implementation
Group fields and behavior that change together; create collaborator with narrow contract; delegate, migrate tests and remove redundant state.

## Verification and review
New class has independent responsibility and tests.
