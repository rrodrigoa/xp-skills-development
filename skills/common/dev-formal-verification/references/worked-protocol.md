# Worked formal model: retry and duplicate delivery

## When to load
A workflow performs a durable operation and may retry after a timeout or crash. Combine concurrency-protocols, tla-model and model-correspondence.

## Example property and abstraction
Model two logical requests, a small bounded number of attempts, durable operation identity, an atomic committed-effect record, response delivery and a crashed/recovered worker. Include retry before and after commit, dropped responses, duplicate messages and recovery. Separate at-most-one committed effect per logical identity from eventual completion under stated delivery and availability assumptions. Do not assume successful response implies durable commit unless that contract is established.

## Procedure
Write initial state and legal actions independently of implementation; make request identity and attempt identity separate. Check the safety invariant for all explored reachable states and appropriate liveness only with explicit fairness/availability assumptions. Use a bounded TLC configuration with multiple workers and small identity sets; vary counts where affordable. Introduce a broken variant that forgets the committed identity after a lost response; verify the model checker finds a duplicate-effect counterexample. Restore the intended model and run again, retaining exact property list, constants, config, state counts and diagnostics.

## Implementation correspondence
Map logical identity to request idempotency key, committed-effect record to atomic durable write, response loss to injected transport failure, crash to controlled process restart and retry to application scheduler. Implement an integration test that commits an operation, loses the response, restarts the worker and retries; independently assert durable effect count and terminal result. Include concurrent duplicate deliveries and expiration of idempotency storage as separate cases. Instrument logical terminal outcome separately from dependency attempts using dev-reads.

## Acceptance and limits
Report bounded model result, counterexample for broken version, concrete regression and source mapping. If transaction boundaries differ from the model, the claim cannot cover the implementation until reconciled. The model does not prove arbitrary request volumes, real databases or all failure schedules. Do not claim exactly-once transport delivery; the intended property is at-most-one durable effect under the documented contract.
