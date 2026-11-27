# Silences, mute timings and maintenance windows

## When to load
Suppressing known planned notifications under authorization.

## Procedure
Identify exact rule/label scope, owner, incident/change ticket, start/end, timezone and reason. Use the approved alert manager mechanism; differentiate notification suppression from stopping evaluation. Prefer narrow, expiring silence or scheduled mute timing with visible record; do not change thresholds or delete rule to avoid a notification. Maintain independent coverage for unrelated incidents and high-risk failures. Verify planned maintenance SLO exclusion separately with policy; a silence does not remove bad events. Preview matcher scope and rollback; review expiry and recovery notifications.

## Required evidence and acceptance
Before/after matched alerts, approved scope and expiry, unaffected routes and confirmed restoration; no permanent or unauthorized suppression.

## Guardrails
Never auto-silence a production alert from an agent diagnosis without approval or use wildcard global silence casually.
