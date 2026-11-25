# Library and HTTP API design

## Use when
External consumers call stable interfaces.

## Avoid when
Exposing internal domain mutation or ORM schemas directly.

## Implementation
Specify typed requests/results, errors, pagination, timeouts and versioning as applicable. Keep transport adapters thin and validate inputs; avoid breaking defaults.

## Verification and review
Contract tests cover success, validation, auth and compatibility.
