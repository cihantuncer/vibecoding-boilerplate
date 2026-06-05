# Testing Directives Index

Use for tests, coverage, mocks, regression checks, and validation strategy.

- Identify the behavior or risk that must be proven.
- Prefer the existing test style and the smallest useful test level.
- For bug fixes, reproduce the failure when practical.
- Run the narrowest relevant command first, then broaden only if needed.
- After code changes, run the project's defined lint, type-check, or test commands. Discover commands from Serena onboarding memory or project config (package.json, Makefile, etc.).

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| routine local test/check | none | this index is enough |
| E2E, browser flow, Playwright, Cypress, responsive smoke, critical journey | `./e2e-browser.md` | user flow must be proven in browser |
| bug regression, denied path, migration safety, broad refactor | `./testing-regression-security.md` | test must prove a specific risk |
| flaky tests, mocks, unclear validation strategy | `./testing.md` | risk is not covered by this index |

Open at most one testing directive unless the task clearly needs more.
