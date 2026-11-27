# Java memory model and shared state

## Shared guidance
oo-design: object-model; dev-reliability: async, data-integrity

## When to load
Concurrently access mutable objects or caches.

## Language-specific decisions
Define ownership and safe publication using immutability, locks, volatile/atomic primitives or concurrent collections as appropriate. Volatile does not make compound updates atomic; concurrent collection operations may not make multi-step invariants atomic. Avoid escaping this during construction.

## Verification and evidence
Inspect happens-before reasoning, test compound invariants and contention; use stress tests where appropriate.

## Avoid
Relying on timing, unsynchronized lazy initialization or shared mutable static fields.
