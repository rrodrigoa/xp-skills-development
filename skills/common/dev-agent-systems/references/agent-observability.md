# Agent tracing and cost budgets

## Use when
Agent execution spans multiple LLMs/tools.

## Avoid when
Logging full prompts or assuming provider usage is always present.

## Implementation
Trace run/node/tool/provider IDs, model version, timings, outcome and token usage when available; redact content; impose step/time/cost limits and capture termination reason.

## Verification and review
Test budget exhaustion, missing usage and correlation across tools.

## Deep guidance
Load dev-reads agent-reads for agent health and quality semantics, dev-observability agent-telemetry for execution spans and token/cost signals, and monitoring-agent-tools for bounded evidence tools. Use dev-alerting for actionable response, not model self-diagnosis. Track provider-reported versus estimated usage and independent eval verdicts; unknown quality must not count as success.
