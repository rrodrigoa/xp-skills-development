# Custom rule false positive

## Scenario
A checker flags a forbidden name in a string and misses an import alias.

## Expected agent behavior
Require syntax-aware matching, allowed fixture and alias violation fixture. Mark unreliable enforcement incomplete.

## Evidence
Inspect actual target changes, commands, raw outputs and revision; distinguish observed outcomes from plans. This is a prose evaluation, not a test run.
