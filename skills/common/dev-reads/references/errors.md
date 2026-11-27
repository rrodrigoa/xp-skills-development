# E — Error semantics and classification

## When to load
Defining errors or diagnosing rising failure rates.

## Procedure
Define terminal user-visible failure from the consumer contract, including timeouts, partial results, stale results and incorrect business outcomes. Keep attempt-level dependency failures separate from final failures; count a logical request once at its terminal boundary. Use bounded categories such as invalid input, authorization denial, throttling, dependency failure, deadline, cancellation and internal fault, with explicit eligibility rules. Treat HTTP status or an exception as evidence, not a universal definition: a transport success can contain a business failure; expected validation may be excluded from a specific SLI. Record cause and outcome separately. Derive error ratio from the failed eligible events divided by all eligible terminal events for matching scope/window.

## Required evidence and acceptance
Exercise successful retry, exhausted retry, business failure with transport success, cancellation and partial success; compare emitted counters to expected outcome table.

## Guardrails
Never hide errors by catching exceptions, excluding failures post hoc, or counting every exception as a separate user failure.
