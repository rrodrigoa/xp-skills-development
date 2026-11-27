# Severity, ownership and notification routing

## When to load
Defining alert recipients and escalation.

## Procedure
Classify severity from user impact, urgency and time-to-harm; map to a named service owner and on-call route with fallback. Use stable routing labels such as team, service, environment and severity; keep changing numeric values in annotations, not identity labels. Define page/ticket/info policy, escalation and acknowledgement expectations. Verify notification policy match order, grouping, receiver access and fallback for unmatched labels. Separate production from test routes; test actual delivery using approved test channels and synthetic notifications. Avoid sensitive content in messages and contact credentials in rules.

## Required evidence and acceptance
Route test proves expected owner, fallback, escalation and no unauthorized recipient; record timestamps and delivery/ack status.

## Guardrails
Do not infer a notification was delivered merely because the rule fired.
