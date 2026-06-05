---
purpose: Refactoring procedure.
use_when: Broad/shared behavior, weak tests, public API movement, dependency changes, modernization, or large file/module movement.
prefer_index: ./INDEX.md
---

# Refactoring Directive

Define the unchanged behavior and the exact scope. Inspect current tests and callers before moving code. If safety is weak, add or run a focused check before broad edits.

Keep changes incremental and reviewable. Separate mechanical movement from behavior changes. Preserve public APIs, imports, filenames, config, and side effects unless intentionally changed.

Prefer existing abstractions. Add a new abstraction only when it removes real duplication or complexity and has a clear owner.

Validate the old behavior through tests, type checks, or targeted smoke checks. State any behavior that was assumed rather than proven.
