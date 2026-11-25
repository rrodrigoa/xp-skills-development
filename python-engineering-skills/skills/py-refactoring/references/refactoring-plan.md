# Refactoring plan and risk control

## Use when
Multi-file restructuring with external consumers.

## Avoid when
Combining unrelated feature changes into refactor.

## Implementation
Inventory dependencies and contracts; select seams, define baseline, incremental milestones, migration and rollback; separate mechanical moves from behavior changes.

## Verification and review
Each milestone has executable checks; final diff reviewed for public changes.
