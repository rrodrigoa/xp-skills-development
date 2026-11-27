# Remove contagious workarounds and obsolete patterns

## When to load
Timer hacks, retries, global state or temporary shims proliferate.

## Implementation in the target project
Trace the symptom to ownership, lifecycle, scheduling or contract mismatch. Record a reproducible failure and measure impact. Add characterization tests; introduce a principled replacement and migrate a small cohort; prohibit new instances with a scoped check; retire old ones after compatibility and rollback review. Preserve rationale for necessary exceptions with expiry and owner.

## Required evidence and acceptance
Regression fails before fix and passes after; profiling or telemetry confirms claimed impact; no new prohibited usage; legitimate low-level uses remain possible.

## Guardrails
A ban on all timers, comments or static functions is not universal. Protect justified framework-level use.
