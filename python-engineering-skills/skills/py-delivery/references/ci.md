# Continuous integration

## Use when
Pull request verification and releases.

## Avoid when
CI that only runs trivial smoke test or broad token permissions.

## Implementation
Use matrix for supported versions/OS as needed, least privilege, cache keyed to dependency inputs; require checks through repo rules; separate untrusted PR from publishing.

## Verification and review
Verify workflows lint and actual CI status; no credentials on untrusted code.
