---
purpose: Modern CSS and responsive layout guidance.
use_when: CSS/layout work needs responsive behavior, fluid sizing, grid/flex decisions, container queries, or motion/accessibility checks.
prefer_index: ./INDEX.md
---

# Modern CSS Responsive Design Directive

Use mobile-first CSS. Prefer Grid for two-dimensional layout, Flexbox for one-dimensional alignment, and `gap` over margin choreography. Use logical properties, `aspect-ratio`, `clamp()`, `min()`, `max()`, and container queries when they simplify responsive behavior.

Keep styling consistent with existing tokens, custom properties, naming, and component structure. Add new utility classes sparingly and avoid `!important` unless overriding an external constraint.

Protect usability across sizes: check text wrapping, overflow, touch targets, focus-visible states, contrast, reduced motion, and high-contrast behavior. Use transforms for motion, keep `will-change` rare, and avoid expensive selectors.

Validate with relevant viewport checks or screenshots when layout behavior changes.
