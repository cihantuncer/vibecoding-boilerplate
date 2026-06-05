---
purpose: Frontend/UI procedure.
use_when: Complex state, critical workflows, accessibility risk, auth/admin UI, or broad layout/interaction changes.
prefer_index: ./INDEX.md
---

# Frontend Directive

Inspect nearby components, routes, state ownership, CSS conventions, design tokens, and existing accessibility patterns. Keep the first changed screen usable, not merely visually plausible.

Preserve interaction contracts: loading, empty, error, disabled, focus, keyboard, responsive, and permission states. Avoid duplicating derived state and keep effects/events scoped.

For CSS/layout, use stable dimensions and responsive constraints. Check text overflow, overlap, viewport behavior, and component density.

Validate with focused tests, browser smoke checks, screenshots, or manual steps appropriate to the change. State any viewport or interaction path not checked.
