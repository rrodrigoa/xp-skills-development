# Formatting, linting and type quality gate

## When to load
Configured static checks apply to changed code.

## Procedure
Identify the approved format, lint and type-check configurations, language and runtime targets, and exclusions. Verify all required checks ran on the reviewed revision; inspect any new ignores, casts, untyped escape hatches or changes to diagnostic severity. Distinguish preexisting findings from new or worsened ones according to policy. Review dynamic boundaries that a type checker cannot prove.

## Required evidence and acceptance
Exact configuration and tool identity, trusted check results and locations of new violations. Approved baseline and policy must determine whether legacy findings block.

## Guardrails
Do not weaken configuration or add unjustified suppressions to obtain a pass. A clean static check is not evidence of behavioral correctness.
