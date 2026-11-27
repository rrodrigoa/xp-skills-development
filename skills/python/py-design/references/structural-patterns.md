# Python structural pattern mapping

## Shared guidance
oo-patterns: adapter, bridge, composite, decorator, facade, flyweight, proxy

## When to load
Adapt or compose abstractions.

## Language-specific decisions
Use structural protocols and explicit delegation. Function decorators are suitable for callable contracts; preserve metadata/signature as appropriate. Object decorators preserve the wrapped behavioral contract. Keep proxy authorization at actual trust boundaries; cache immutable flyweight state only.

## Verification and evidence
Test delegation, decorator ordering, error propagation and lifetime, including async callables when supported.

## Avoid
Dynamic forwarding that hides ownership or masks unsupported operations.
