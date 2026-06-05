---
purpose: Testing/validation procedure.
use_when: Flaky tests, broad refactors, security-sensitive behavior, complicated mocks, unclear validation strategy, or test design work.
prefer_index: ./INDEX.md
---

# Testing Directive

Define what risk must be proven: regression, contract, security, migration, rendering, integration, or performance. Use the lowest test level that proves it reliably.

Follow existing test tools, fixtures, naming, and assertions. For bug fixes, add or run a case that fails for the old behavior when practical. Avoid brittle timing, snapshots, and over-mocking.

For refactors, prove unchanged behavior. For security, include at least one denied/abuse path. For deployment/scripts, prefer dry-run and smoke validation.

Run the narrowest relevant command first. Broaden only when shared behavior changed. Report commands run and any skipped checks.
