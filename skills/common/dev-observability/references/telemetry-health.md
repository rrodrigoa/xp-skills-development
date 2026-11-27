# Monitoring the monitoring pipeline

## When to load
Signals go missing or observability reliability matters.

## Procedure
Measure expected targets/emitters versus observed, scrape or receive health, last successful export, queue length, refused/dropped items, ingest lag, storage/query availability, evaluation delays and notification delivery. Separate source idle from collection failure and query error. Establish independent synthetic heartbeat or dead-man check for the monitoring chain; avoid relying solely on the broken system to report its own outage. Define ownership and capacity budgets for collectors and storage, failure modes and recovery criteria.

## Required evidence and acceptance
Inject source failure, collector outage, backend delay and notification failure; verify distinct status, routing and recovery without false healthy signal.

## Guardrails
Do not use the application error rate as sole proof that monitoring itself is working.
