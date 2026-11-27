# Java plugin discovery and lifecycle

## Shared guidance
dev-implementation: cli-plugins; dev-migration: blueprint-plugin

## When to load
Discover optional provider implementations.

## Language-specific decisions
Prefer explicit registry initially. Use ServiceLoader for approved SPI discovery with provider declarations appropriate to classpath or module path; validate capabilities and versions and handle ServiceConfigurationError explicitly. Scope class loaders and cleanup; discovery is not sandboxing.

## Verification and evidence
Test missing/duplicate provider, bad provider declaration, incompatible version, loading and shutdown; inspect packaged service resources.

## Avoid
Loading untrusted JARs into privileged process or relying on discovery ordering.
