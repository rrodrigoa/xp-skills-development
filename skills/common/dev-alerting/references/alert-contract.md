# Alert design contract and actionability

## When to load
Proposing a new alert or reviewing existing ones.

## Procedure
Start from a user-impact symptom, reliability objective or imminent preventable risk. Define affected population, condition, data source/query, evaluation interval/window, sustained duration, recovery semantics, labels, severity, owner, route, expected action, runbook and evidence link. State what happens if no data, query error or partial coverage. Decide page versus ticket versus dashboard-only according to urgency and actionability. Prefer symptom alerts for paging; use cause signals to guide diagnosis or page only if they demand timely preventive action. Explicitly identify duplicates and expected responders.

## Required evidence and acceptance
An independent responder can explain impact, verify condition and perform a safe next action; replay healthy, breach, transient, recovery and missing-data cases.

## Guardrails
Do not page on every log error, arbitrary CPU threshold or a signal with no owner/action.
