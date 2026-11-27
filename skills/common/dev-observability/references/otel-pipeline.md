# OpenTelemetry API, SDK, collector and export pipeline

## When to load
Designing or diagnosing the telemetry pipeline.

## Procedure
Inventory instrumentation API, SDK/provider, processors, exporter, collector receivers/processors/exporters and backend. Libraries depend on API and respect host configuration; applications own SDK lifecycle. Choose protocols, authentication, TLS, resource identity, batch/queue limits, timeouts, retry/drop policy, sampling and retention based on deployment. Do not block user work on best-effort diagnostics; separately design mandatory audit durability if required. Ensure shutdown flush is bounded and telemetry export cannot recursively instrument itself. Monitor collector queue pressure, refusals, export failures, drops and backend freshness. Validate version-specific component support and prevent double ingestion.

## Required evidence and acceptance
End-to-end sample from source to backend with identity/units; controlled collector/backend outage, restart and shutdown prove bounded failure and visible loss.

## Guardrails
Do not assume OTLP success proves final storage or an installed agent captures domain outcomes.
