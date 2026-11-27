# Inspectable runtime evidence bundles

## When to load
Reviewing actual changes rather than only diffs.

## Implementation in the target project
Capture preconditions, actions, assertions, actual outputs, screenshots/video if useful, trace IDs, logs, timings and failure artifacts. Bind all to candidate and test run; record platform, data fixtures and capture tool. Redact secrets and personal data; store with access control. Show before/after when behavior changed and retain negative evidence.

## Required evidence and acceptance
Reviewer can independently follow sequence and verify observed assertions; artifacts are authentic, revision-bound and complete enough for claimed scope.

## Guardrails
A screenshot is supporting evidence, not proof of authorization, hidden state or all transitions. Do not cherry-pick successful runs.
