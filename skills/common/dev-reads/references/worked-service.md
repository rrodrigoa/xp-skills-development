# Worked READS contract for a request service

## When to load
An agent needs a concrete example of measurement design.

## Procedure
Illustrative checkout operation: eligible demand is 1,000 distinct eligible logical requests accepted at the service boundary in ten minutes, 990 complete, 10 remain in flight. Of completed requests, 980 deliver the agreed result, 10 fail; 970 of the 980 successes meet a 300 ms deadline. R is about 1.67 accepted requests per second, completion rate 1.65/s, E is 10/990 terminal errors (about 1.01%). A for the terminal-event population is 980/990 (about 98.99%); a deadline-based cohort SLI may classify outstanding requests differently once due. D deadline-good fraction for eligible completed operations is 970/990 (about 97.98%) if both correctness and latency are required; compute actual duration percentiles from a histogram. S: 45 occupied of 50 worker slots is 90% occupancy; a growing queue and wait distribution establish pressure. A failed payment provider attempt followed by successful retry counts as an attempt error, not a terminal failure. External synthetic checks cover ingress failure, when no eligible requests reach the service. Never merge these example populations without explicit semantics.

## Required evidence and acceptance
Given a fixed workload, reproduce each number, identify denominator and in-flight classification, compare probe and passive signals, and map the required instruments to owners.

## Guardrails
Illustrative values are not production thresholds. Do not claim final cohort success before outstanding work reaches its deadline.
