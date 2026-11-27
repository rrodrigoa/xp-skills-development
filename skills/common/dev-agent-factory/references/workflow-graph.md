# Deterministic development workflow graph

## When to load
Building an agent orchestration workflow.

## Implementation in the target project
Define typed state with task, approved requirements, scope, base/head, policy, budgets, selected skills, artifacts and evidence. Specify allowed nodes: intake, inspect, plan, acceptance, implement, fast checks, runtime/formal checks when applicable, independent gate, human approval if required, completion. Make transition predicates host-owned and machine-evaluated; LLM can propose action, not set gate status. Include failure, hold, cancel, timeout and terminal paths; invalidate evidence on revision change.

## Required evidence and acceptance
Transition table and negative tests show forbidden transitions, stale evidence, cancellation, retries and exhausted budget cannot reach eligible state.

## Guardrails
A graph with prompt-only conditional edges is not deterministic enforcement. No runtime graph is provided here.
