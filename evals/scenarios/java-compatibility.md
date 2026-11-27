# Java Compatibility

## Task
A library method is renamed; all current source modules compile but older consumers have not been run.

## Expected routing
Route dev-quality-gates compatibility-gate and java-delivery compatibility.

## Expected evaluation
Distinguish source and binary compatibility; verify previous compiled consumer against new JAR; report required missing evidence UNKNOWN, unauthorized break FAIL.
