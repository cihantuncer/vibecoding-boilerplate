---
purpose: Form UX and validation directive.
use_when: Work changes forms, inputs, validation, errors, submit behavior, dirty state, disabled/loading state, or client/server validation boundaries.
prefer_index: ./INDEX.md
---

# Forms Validation Directive

Preserve the full form lifecycle: initial values, typing, validation timing, submit, loading, success, failure, reset, and retry. Keep client validation helpful but never treat it as the only enforcement boundary.

Error messages should be field-specific, stable, and accessible. Preserve labels, autocomplete, input modes, keyboard behavior, focus after submit/failure, and disabled state semantics.

Validate at least one success path and one failure path. For server-backed forms, check that server errors map cleanly back to the UI.
