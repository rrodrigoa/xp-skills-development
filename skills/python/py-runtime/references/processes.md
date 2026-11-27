# Python subprocess and filesystem safety

## Shared guidance
dev-reliability: subprocess, filesystem, security-boundaries

## When to load
Launch tools or access files.

## Language-specific decisions
Pass argument lists instead of shell interpolation, use explicit working directory/environment, bounded output/timeouts and process cleanup; account for Windows versus POSIX process behavior. Resolve paths within authorized root and handle symlink/race risks.

## Verification and evidence
Test hostile arguments, path traversal, timeouts, process trees and redacted output.

## Avoid
shell=True with untrusted strings or relying on lexical prefix checks alone.
