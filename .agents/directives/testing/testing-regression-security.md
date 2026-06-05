---
purpose: Regression and security validation guidance.
use_when: Tests must prove a bug fix, permission boundary, denied path, migration safety, or broad refactor behavior.
prefer_index: ./INDEX.md
---

# Regression/Security Testing Directive

Define the failure or risk before choosing a test. For bugs, reproduce the old failure when practical. For security, include a denied/abuse path, not only the allowed path.

Use the lowest test level that proves the behavior reliably. Avoid brittle timing, broad snapshots, and over-mocking.

Run the narrowest relevant command first and report skipped broader checks.
