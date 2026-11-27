# READS for queues, streams and batch jobs

## When to load
Work is accepted now and completed later.

## Procedure
Define ingress, durable acceptance, completion, acknowledgement and business result boundaries. R: arrival/completion rates and item counts. E: terminal processing failures, dead letters, retries and lost/duplicate outcomes separately. A: fraction completed correctly by deadline or freshness objective, including backlog still outstanding per approved cohort policy. D: queue wait, processing and end-to-end age, including time since oldest unprocessed item. S: partition lag, queue capacity, worker utilization, storage and quota headroom. Distinguish event time, ingestion time and processing time; account for late/out-of-order events, replay and backfill. Partition-level skew can hide behind aggregate throughput.

## Required evidence and acceptance
Load a known batch including retries, poison items, delayed events and a stopped consumer; reconcile durable outcomes and age/lag with queue state.

## Guardrails
Do not count acknowledgement as successful completion, or interpret backlog reduction caused by dropping work as recovery.
