# Agent permissions and prompt injection

## Use when
Agent handles external content or performs actions.

## Avoid when
Relying on prompt instructions as sole authorization.

## Implementation
Treat retrieved text as data; allowlist tools and operation scope; validate args, require approval for consequential actions as policy dictates; isolate execution and secrets; audit decisions.

## Verification and review
Adversarial scenario tries tool escalation, data exfiltration and hidden instructions; assert no side effect.
