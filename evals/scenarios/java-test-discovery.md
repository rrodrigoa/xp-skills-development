# Java Test Discovery

## Task
A Gradle test task reports success with zero relevant tests because the configured engine does not discover them.

## Expected routing
Route dev-quality-gates test-execution-gate, java-testing junit and java-delivery gradle.

## Expected evaluation
Do not report PASS; inspect discovery and exact module scope, record failure or missing evidence under approved policy. No changing gate thresholds.
