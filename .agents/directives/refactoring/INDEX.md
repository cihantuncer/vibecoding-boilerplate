# Refactoring Directives Index

Use for cleanup, splitting, reorganizing, and improving structure without intended behavior changes.

- Define the behavior that must remain unchanged.
- Prefer small, mechanical, reviewable changes in one responsibility area.
- Follow existing local abstractions and naming.
- Keep or add a focused safety check before larger movement.
- After completing changes, review your own diff: check for unnecessary changes, broken contracts, or missing edge cases.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| small local cleanup | none | this index is enough |
| exported symbols, imports, routes, config, shared modules | `./refactoring-public-api.md` | callers may break |
| broad refactor, weak tests, dependency/modernization work | `./refactoring.md` | risk is not covered by this index |

Open at most one refactoring directive unless the task clearly needs more.
