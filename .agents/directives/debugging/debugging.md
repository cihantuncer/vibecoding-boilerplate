---
purpose: Debugging procedure.
use_when: Unclear root cause, intermittent failure, config/environment issue, deployment failure, or security-sensitive bug.
prefer_index: ./INDEX.md
---

# Debugging Directive

Start from the observed symptom: exact command, input, output, stack trace, status code, or user flow. Reproduce when practical; otherwise locate the closest failing path through logs, tests, or code.

Narrow scope before patching. Compare expected vs actual behavior, identify the first wrong state, and avoid changing multiple layers at once. Prefer one small hypothesis at a time.

Patch the root cause, not just the symptom. Preserve unrelated behavior and avoid broad cleanup during the fix.

Validate the original failure path and at least one nearby non-failing path when risk justifies it. If not reproduced, say what evidence supported the fix.
