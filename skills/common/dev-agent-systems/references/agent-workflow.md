# Agent workflow state and orchestration

## Use when
Multi-step graph, tools and resumable runs.

## Avoid when
One unbounded model loop with hidden state.

## Implementation
Define typed state, node contracts, explicit transitions, termination and budgets; isolate deterministic policies from LLM choices; checkpoint versioned state.

## Verification and review
Test success, failure, resume, loop bounds and invalid transitions.

For deterministic coding orchestration, load dev-agent-factory workflow-graph and node-contracts. Host-controlled transition guards must validate typed outputs and independent evidence; model confidence cannot authorize merge, bypass verification or extend its own budget. Use repair-loop and self-improvement for bounded, independently reviewed evolution.
