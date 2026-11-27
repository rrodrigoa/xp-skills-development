# AI agent, LLM and tool instrumentation

## When to load
Implementing or debugging an agentic system.

## Procedure
Trace run/turn, workflow node, model request and tool execution with parent/link relationships and stable logical names. Track end-to-end task outcome, step/attempt counts, retries, model/provider/revision, tool name/outcome, queue/first-token/total duration, token usage and budget exhaustion. Use provider-reported counts when available; label estimates and unknowns, separate cached/reasoning tokens only when defined. Keep run/turn/tool-call IDs in safe trace/log fields rather than metric labels. Link eval verdict, scenario/cohort and evidence without leaking prompts or user content. Use pinned GenAI semantic conventions and document development-status fields. Instrument permission denials and cancellations without exposing credentials or raw arguments.

## Required evidence and acceptance
Known workflow with failed/retried tool, invalid response, denied action and budget stop; reconcile trace topology, usage, final outcome and independent quality evaluation.

## Guardrails
Do not treat successful tool transport or fluent answer as task success, or log hidden reasoning, prompts or raw tool outputs by default.
