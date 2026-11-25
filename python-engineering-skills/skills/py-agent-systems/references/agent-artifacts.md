# Agent-generated code and artifact integrity

## Use when
Agent writes code, patches or packages.

## Avoid when
Claiming tests passed, inventing files, or rewriting unrelated code.

## Implementation
Track actual commands and changes, inspect generated diff, run checks, validate artifact contents and hashes, report blockers and unverified claims; require approval for external publishing.

## Verification and review
Verify exact files and reproducibility; fail if artifact missing.
