---
purpose: REST API design and resource semantics directive.
use_when: Backend work adds or changes REST endpoints, resource naming, methods, status codes, filtering, pagination, idempotency, or error semantics.
prefer_index: ./INDEX.md
---

# REST API Design Directive

Model endpoints around resources and existing project conventions. Preserve method semantics: safe reads, idempotent updates where expected, explicit creation, and predictable deletion behavior.

Keep status codes, error shape, pagination, filtering, sorting, and versioning consistent with nearby APIs. Avoid leaking internal persistence names or adding one-off response formats.

Validate with request-level checks for success, validation failure, and authorization or not-found behavior when relevant.
