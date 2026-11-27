# Graph tries to merge stale evidence

## Scenario
A repair changes head after verification.

## Expected agent behavior
Host invalidates old evidence, reruns required checks and prevents merge until eligible.

## Evidence
Inspect actual target changes, commands, raw outputs and revision; distinguish observed outcomes from plans. This is a prose evaluation, not a test run.
