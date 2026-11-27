# Worked rule lifecycle: forbidden dependency

## When to load
A repository needs its first enforceable architecture rule.

## Example contract
Illustrative ID ARCH-01/domain-no-infrastructure, only after approval. Domain code must not import concrete persistence or transport implementations; infrastructure can implement domain/application-owned contracts. Composition root may wire adapters. Scope source roots explicitly; generated files and fixtures are excluded only by approved paths. Type-only references are considered according to the actual dependency contract, not automatically excluded.

## Implementation sequence
1. Inspect existing direct imports, aliases, re-exports, dynamic loader and build/module relationships. Record inherited violations and whether analysis can resolve each relationship.
2. Introduce or reuse the correct port in the owning layer and migrate one call site with characterization tests. Make canonical valid usage visible.
3. Implement a syntax-aware or compiler/architecture-tool rule on the relevant edges. Give diagnostic contract ID, source location, offending target, permitted alternative and documentation pointer. Ensure analyzer failures and unresolvable required inputs produce explicit error, not success.
4. Create isolated fixture cases for forbidden direct import, alias, forbidden re-export/transitive edge if in scope, permitted adapter, composition root, harmless string/comment, excluded generated path and malformed input. For dynamic registration use a separate runtime wiring test if static analysis cannot resolve it.
5. Execute the rule on valid and invalid fixtures. A deliberately invalid dependency must produce the expected diagnostic, not merely fail due to unrelated missing dependency. Run on base and candidate; baseline only authorized inherited violations, then verify no-new regression using the same configuration.
6. Integrate the existing local verify entry point and CI context with tool version and fixture execution. Ask independent owner to review rule semantics, scope, false positives and bypass risk before requiring it. Record residual dynamic risk and migration schedule.

## Acceptance
Expected behavior survives the refactor; rule rejects actual prohibited change and accepts valid architecture; CI uses same checker contract and failures are propagated. Reviewer verifies base/head evidence and changed controls. If host CI or dynamic analysis is unavailable, report exact gap; do not claim full enforcement.

## Guardrails
This example is not a universal layer structure. Use actual project architecture and approved scope. No executable checker implementation belongs in the skills repository.
