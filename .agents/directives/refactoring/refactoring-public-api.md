---
purpose: Public API or module movement refactoring guidance.
use_when: Refactor moves exported symbols, public files, imports, config, routes, dependency boundaries, or shared modules.
prefer_index: ./INDEX.md
---

# Public API Refactoring Directive

Identify all callers and public entry points before moving code. Separate mechanical moves from behavior changes. Preserve imports, filenames, route names, config keys, and side effects unless intentionally changed.

Use adapters or temporary compatibility paths when direct movement would break callers.

Validate with existing tests, type checks, import checks, or a focused smoke path. State any caller coverage gap.
