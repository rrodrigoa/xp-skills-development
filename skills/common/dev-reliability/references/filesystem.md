# Safe filesystem operations

## Use when
Reading/writing user-controlled paths or archives.

## Avoid when
String prefix checks and unsafe extraction.

## Implementation
Resolve against permitted root, verify containment, reject symlinks or use safe OS-level operations where adversarial races matter; bound extraction; atomic replace for durable writes.

## Verification and review
Test traversal, symlink escape, partial failure and oversize archive.
