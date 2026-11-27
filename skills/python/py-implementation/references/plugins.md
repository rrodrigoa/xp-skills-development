# Python plugin discovery

## Shared guidance
dev-implementation: cli-plugins; dev-migration: blueprint-plugin

## When to load
Discover external providers.

## Language-specific decisions
Use explicit registry before dynamic discovery. Use importlib.metadata entry points for installed providers; validate names, capabilities, compatibility and trust before loading. Importing a plugin executes code; isolate untrusted extensions.

## Verification and evidence
Test duplicate registrations, missing plugin, unsupported API version and cleanup after partial load.

## Avoid
Arbitrary module names from untrusted input or global import-time registration.
