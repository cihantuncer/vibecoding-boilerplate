# Frontend Directives Index

Use for UI, CSS, DOM, browser behavior, React, accessibility, and client state.

- Inspect nearby components, styles, state flow, and design conventions.
- Preserve interaction behavior and layout at relevant viewport sizes.
- Keep state ownership clear; avoid duplicating derived state.
- Validate with targeted tests, screenshots, or browser checks when visual/interactive behavior changes.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| routine component/UI edit | none | this index is enough |
| semantic HTML, keyboard, focus, ARIA, labels, contrast, disabled states | `./accessibility.md` | accessibility behavior may change |
| forms, inputs, validation, errors, submit, loading, dirty state | `./forms-validation.md` | form lifecycle or validation changes |
| CSS, responsive, mobile, viewport, overflow, wrapping, spacing, Grid/Flexbox, fluid sizing | `./modern-css-responsive-design.md` | layout behavior is central |
| complex state, critical workflow, accessibility, auth/admin UI | `./frontend.md` | risk is not covered by this index |

Open at most one frontend directive unless the task clearly needs more.
