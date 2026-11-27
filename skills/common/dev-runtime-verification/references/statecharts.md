# User-visible statecharts and transition tables

## When to load
Workflow, UI, cancellation or asynchronous feature.

## Implementation in the target project
Define states, initial state, events, guards, side effects, transition target and observable outcome; include invalid transitions, timeout, failure, recovery and terminal states. Distinguish user-visible state from internal implementation. Review ambiguous transitions with owner; map approved states/edges to tests and where useful formal properties. Update feature map and trace labels.

## Required evidence and acceptance
Reachable states and critical transitions exercised, invalid events rejected, terminal paths bounded. Reviewer can compare statechart to real artifacts.

## Guardrails
Diagram is a specification aid, not execution or proof; avoid generating it solely from implementation if checking intent.
