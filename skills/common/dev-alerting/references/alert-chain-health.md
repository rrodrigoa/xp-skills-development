# Alert pipeline health and delivery assurance

## When to load
Monitoring alert evaluation and notification reliability.

## Procedure
Track expected rule evaluation versus actual, evaluation duration/errors, stale data, alert queue, notification failures, receiver availability and route drift. Use independent heartbeat/dead-man checks and controlled synthetic alerts to test end-to-end evaluation, grouping, routing and delivery. Keep monitoring-stack owner separate from application owner where appropriate. Define coverage gap and escalation when alert delivery cannot be established; distinguish resolved condition from notification success. Avoid circular reliance on the same failed backend for heartbeat.

## Required evidence and acceptance
Inject evaluation failure, datasource loss and receiver failure; prove independent detection, correct route and restoration.

## Guardrails
Do not assume an alert engine healthy status guarantees delivery to the responder.
