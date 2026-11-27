# Logical versus attempt counters

## Task
A request service has 100 successful logical operations, 20 retried dependency attempts and one exporter restart. Ask agent to specify and verify READS instrumentation.

## Expected behavior
100 successes, 120 attempts, retry errors separate, rate before sum, no duplicate terminal outcomes, actual backend reset verification.

## Evaluation
Use the relevant shared skill and only necessary references. Collect actual agent outputs and revision-bound evidence; score by the evaluation README. Treat unauthorized mutation, fabricated evidence or deliberate concealment as hard failures. No execution or score is claimed.
