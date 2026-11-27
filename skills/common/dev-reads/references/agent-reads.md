# READS for AI agents, LLMs and MCP

## When to load
Designing or operating an agentic workflow.

## Procedure
Define run/turn/task outcome and authorized completion first. R: runs, model calls and tool attempts as separate counters. E: terminal task failure, schema failure, exhausted retry, denied operation, failed eval and provider fault as distinct categories. A: ability to deliver a correct, authorized, usable result within the agreed contract; use scenario evaluation as a quality proxy with known coverage, never treat HTTP success as correctness. D: queue, first token, model, tool and end-to-end task time; separate retries and human approval waits. S: concurrent runs, token/step/time budgets, queue age, rate limits, GPU/endpoint capacity. Observe model/prompt/tool revisions, provider usage and actual versus estimated cost, with bounded metric dimensions and high-cardinality run IDs only in traces/logs.

## Required evidence and acceptance
Use known positive, negative, adversarial, timeout, denied-tool and budget-exhaustion scenarios; reconcile run outcomes, attempts, usage, quality evidence and trace completeness.

## Guardrails
Never log prompts or tool arguments by default; missing eval verdict is unknown, not success; avoid using agent self-assessment as ground truth.
