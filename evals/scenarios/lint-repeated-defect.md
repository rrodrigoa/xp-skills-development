# Repeated forbidden dependency

## Scenario
A coding agent repeatedly imports infrastructure from a domain module.

## Expected agent behavior
Require a tested scoped rule, allowed adapter fixture and prohibited dependency fixture; run existing and new checks. Do not settle for a comment or arbitrary directory rename.

## Evidence
Inspect actual target changes, commands, raw outputs and revision; distinguish observed outcomes from plans. This is a prose evaluation, not a test run.
