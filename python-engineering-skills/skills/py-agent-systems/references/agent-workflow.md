# Agent workflow state and orchestration

## Use when
Multi-step graph, tools and resumable runs.

## Avoid when
One unbounded model loop with hidden state.

## Implementation
Define typed state, node contracts, explicit transitions, termination and budgets; isolate deterministic policies from LLM choices; checkpoint versioned state.

## Verification and review
Test success, failure, resume, loop bounds and invalid transitions.
