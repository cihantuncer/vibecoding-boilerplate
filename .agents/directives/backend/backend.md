---
purpose: Backend/API procedure.
use_when: Public contract, auth, data writes, external services, or unclear server behavior.
prefer_index: ./INDEX.md
---

# Backend Directive

Before changing backend behavior, identify the boundary: route, controller, service, middleware, job, or integration. Note caller, inputs, outputs, auth state, persistence, and side effects.

Preserve contracts unless explicitly changing them: status codes, response shape, pagination, error format, idempotency, and permission behavior. Validate input at the boundary and keep business rules in the existing local layer.

For data writes, check transaction expectations and failure behavior. For external calls, preserve timeout, retry, error mapping, and secret handling.

Validate with focused tests, a direct request, or the smallest command that exercises the changed path. Mention any unverified contract or integration risk.
