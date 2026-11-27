# Auto versus manual instrumentation

## When to load
Introducing instrumentation in an existing application.

## Procedure
Inventory framework agents, libraries, exporters, interceptors and existing metric/span ownership. Use supported auto instrumentation for conventional transport, database and runtime signals; add manual signals for domain outcomes, retry semantics, queues, business latency and resource ownership gaps. Establish one instrumentation owner per measurement and layer. Preserve parent context rather than creating a second root. Verify exporter configuration, semantic convention version and labels against actual output. Disable duplicates only with explicit scope and evidence; document coverage gaps and unsupported libraries.

## Required evidence and acceptance
Compare before/after signal inventory and known request trace; verify one terminal domain metric and expected transport spans, with no double counts or conflicting providers.

## Guardrails
Never assume auto instrumentation is sufficient for READS or add a second SDK without checking current configuration.
