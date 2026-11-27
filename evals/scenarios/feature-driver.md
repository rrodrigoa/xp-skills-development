# Stale app instance

## Scenario
Agent tests a feature against a previously launched build.

## Expected agent behavior
Require candidate identity, reset/readiness, observable assertions and cleanup. Stale evidence cannot pass.

## Evidence
Inspect actual target changes, commands, raw outputs and revision; distinguish observed outcomes from plans. This is a prose evaluation, not a test run.
