# READS for CLI tools and libraries

## When to load
Instrumenting non-server software.

## Procedure
For a CLI, measure invocation, terminal exit/result classification, duration and local resource/queue limits where relevant; define availability as ability to complete supported operations only if there is a meaningful population or synthetic check. Keep stdout output contract intact and use approved diagnostics on stderr or a separate sink. For a library define meaningful caller-observed operations, leave provider/export configuration to the host, and avoid hidden network or global side effects. Offline tools may use local counters or summaries and opt-in export; document when dimensions are not applicable. Distinguish local failures from remote dependency errors and interrupted execution.

## Required evidence and acceptance
Verify successful/failed exits, interruption, no telemetry backend, library reuse and machine-readable output; justify unavailable dimensions.

## Guardrails
Do not mandate remote telemetry, server uptime or background threads for every library or local tool.
