# End-to-end and CLI tests

## Use when
Installed application or full workflow behavior.

## Avoid when
Large brittle suites for simple policies.

## Implementation
Invoke installed command or service through real boundary, assert exit/result/state, isolate environment, enforce deadlines and cleanup.

## Verification and review
Test clean environment, success and representative failures.
