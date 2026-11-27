# Java ProcessBuilder and filesystem safety

## Shared guidance
dev-reliability: subprocess, filesystem, security-boundaries

## When to load
Run subprocess or read/write paths.

## Language-specific decisions
Use ProcessBuilder with discrete arguments and controlled environment; drain stdout/stderr, bound output, wait with timeout and handle descendant cleanup where supported. Use NIO Path operations with authorized root, real-path and symlink checks appropriate to threat model.

## Verification and evidence
Test malicious arguments, symlink escapes, timeouts, process trees and disk failure.

## Avoid
Shell interpolation or assuming normalize alone blocks symlink traversal.
