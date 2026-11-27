# Python refactoring mechanics

## Shared guidance
dev-refactoring: characterization, procedural-to-objects; dev-migration: mechanical-migration

## When to load
Move or rename functions, types or packages.

## Language-specific decisions
Inventory imports, dynamic lookups, monkeypatch targets and public keyword contracts. Use syntax-aware CST or language tooling for mechanical moves; separate semantic change. Keep compatibility forwarding only with an approved removal plan.

## Verification and evidence
Compare behavior, import installed artifact, run type/tests and inspect dynamic consumers.

## Avoid
Regex-wide replacement or silently changing import side effects.
