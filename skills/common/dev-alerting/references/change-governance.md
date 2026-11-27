# Alert configuration change control and rollback

## When to load
An agent edits alert rules or notification policy.

## Procedure
Inspect live and declared state, exact organization/folder/rule identifiers, owner and approved source of truth. Prepare scoped diff including old/new semantics, routing, affected alerts, coverage gap, evaluation and rollback. Obtain explicit permission before production writes or silence, enforce least privilege, avoid secret disclosure and use conflict/version checks. Apply to staging or shadow first; validate actual backend state and delivery. Coordinate cutover so old/new rules do not create gaps or duplicate pages. Record author, independent review, revision and deployment evidence; do not modify gates or policy to obtain a pass.

## Required evidence and acceptance
Approved change ticket, candidate/live diff, tests, scoped deployment result, rollback and independent review.

## Guardrails
No blind bulk updates, unauthorized production mutation or automatic threshold changes to quiet an incident.
