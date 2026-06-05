---
purpose: Frontend accessibility and semantic UI directive.
use_when: UI work touches semantic structure, keyboard flow, focus, labels, ARIA, contrast, disabled states, or assistive-technology behavior.
prefer_index: ./INDEX.md
---

# Accessibility Directive

Preserve semantic HTML first; use ARIA only when native elements cannot express the interaction. Keep keyboard, focus order, focus-visible styling, labels, names, roles, and error announcements intact.

Do not hide actionable controls from keyboard or screen-reader users. Do not rely on color alone for state. Be careful with custom buttons, dialogs, menus, tabs, forms, and disabled/loading states.

Validate with keyboard traversal and at least one accessibility-oriented check: label/name inspection, contrast check, or relevant browser/devtool audit.
