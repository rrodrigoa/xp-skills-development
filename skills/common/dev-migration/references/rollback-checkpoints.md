# Migration checkpoints and rollback

## When to load
Planning multi-step changes or risky refactors.

## Procedure
Record starting revision and working-tree state; identify independently verifiable slices, checkpoint criteria, data compatibility and reversibility. Verify each slice and stop if contract breaks or evidence is missing. Define rollback or forward recovery with owner approval for destructive steps.

## Required evidence and acceptance
Checkpoint record with touched paths, tests, migration state and exact remaining scope; recovery verified where feasible.

## Guardrails
Do not reset or discard unrelated work. Code rollback does not necessarily reverse data changes or external side effects.
