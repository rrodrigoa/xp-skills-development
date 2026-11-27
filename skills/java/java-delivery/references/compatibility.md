# Java binary, source and behavioral compatibility

## Shared guidance
oo-design: public-api; dev-quality-gates: compatibility-gate

## When to load
Change published Java API.

## Language-specific decisions
Distinguish source, binary, behavior, serialization and module compatibility. Review method signatures, visibility, generic bounds, constructors, default interface methods, checked exceptions and published constants. Use japicmp or Revapi when approved; compile new consumers and run previously compiled representative consumers against new artifact.

## Verification and evidence
Compare artifacts and exact baseline version; test previous binaries, source clients and wire behavior; record authorized breaks.

## Avoid
Assuming recompiling all sources proves binary compatibility.
