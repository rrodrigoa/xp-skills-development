# Python docstrings and comments

## Shared guidance
dev-implementation: comments-docstrings

## When to load
Document a public interface or non-obvious tradeoff.

## Language-specific decisions
Follow PEP 257 and project docstring style. Explain parameters, returns, units, exceptions, side effects, async/lifetime contracts and invariants; don't repeat obvious annotations.

## Verification and evidence
Review rendered API docs if configured, examples against public contract and comments against behavior.

## Avoid
Comments that excuse missing implementation or stale TODOs.
