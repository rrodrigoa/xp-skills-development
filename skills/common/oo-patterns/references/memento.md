# Memento

## Use when
Snapshot/restore internal state for undo or checkpoint.

## Avoid when
Simple immutable value replacement already suffices.

## Implementation
Capture explicit snapshot of relevant state; keep snapshot immutable and versioned if persistent; restore via owner and validate.

## Verification and review
Test restoration, snapshot independence and invalid snapshot handling.

## Refactoring recipe
**Trigger:** Undo/checkpoint logic exposes private fields or copies live resources.

**Migration:** Define immutable snapshot contract, schema/version and authorized restore; let owner capture/restore, migrate callers to history store.

**Acceptance:** Test round trip, invalid snapshot, version mismatch, aliasing and retention.

**Tradeoff:** External effects cannot be undone by restoring memory; do not snapshot secrets unnecessarily.
