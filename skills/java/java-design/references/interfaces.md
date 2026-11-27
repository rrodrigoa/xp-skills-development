# Java interfaces, abstract classes and sealed hierarchies

## Shared guidance
oo-design: protocols-abcs, solid-isp, solid-lsp

## When to load
Design variation and API boundaries.

## Language-specific decisions
Use interfaces for consumer-owned contracts and composition; use abstract classes for genuine shared lifecycle or template. Functional interfaces support single-operation strategies. Sealed types (where supported) express deliberately closed sets, not general plugin extension points. Default methods may affect compatibility and dispatch; review conflicts.

## Verification and evidence
Compile consumers and run shared behavioral contract tests; test invalid variants and extension compatibility.

## Avoid
Interface per implementation, deep inheritance or sealing an intended public extension API.
