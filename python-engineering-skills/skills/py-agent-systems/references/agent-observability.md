# Agent tracing and cost budgets

## Use when
Agent execution spans multiple LLMs/tools.

## Avoid when
Logging full prompts or assuming provider usage is always present.

## Implementation
Trace run/node/tool/provider IDs, model version, timings, outcome and token usage when available; redact content; impose step/time/cost limits and capture termination reason.

## Verification and review
Test budget exhaustion, missing usage and correlation across tools.
