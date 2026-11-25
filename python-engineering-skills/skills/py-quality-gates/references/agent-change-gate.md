# Agent, prompt and MCP quality gate

## When to load
Model, tool schema, prompts, routing, orchestration or policies change.

## Procedure
Identify altered capabilities and tool permissions. Use versioned scenario evidence for positive, negative, adversarial and multi-turn cases as relevant. Compare equivalent model/config and budget; inspect actual tool calls, outputs, side effects, refusals and hallucinations. Require independent authorization boundaries.

## Required evidence and acceptance
Scenario IDs, expected/observed results, model/config, sample size, failures and quality/cost deltas; approved threshold or UNKNOWN.

## Guardrails
No harness is provided here. Do not trust self-grading, fluent answers, or a single happy path. Confirm denied actions never happened.
