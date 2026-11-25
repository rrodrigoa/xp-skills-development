# Module and package boundaries

## Use when
Large package has circular imports or incoherent utils modules.

## Avoid when
One file per trivial class by default.

## Implementation
Group by cohesive capability or feature. Expose curated public API; private submodules use underscore only when useful. Break cycles via dependency direction, not local imports as a blanket fix.

## Verification and review
Import installed package in clean process; test public exports and dependency rules.
