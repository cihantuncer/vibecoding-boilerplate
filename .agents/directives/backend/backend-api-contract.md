---
purpose: Public API contract guidance.
use_when: Backend work changes response shape, status codes, pagination, auth behavior, idempotency, external integrations, or data-write side effects.
prefer_index: ./INDEX.md
---

# Backend API Contract Directive

Before editing, identify callers and the existing contract: route, method, status codes, response body, error format, pagination, auth, idempotency, and side effects.

Avoid silent contract drift. If the contract must change, update tests and nearby docs/examples. For external integrations, preserve timeout, retry, error mapping, and secret handling.

Validate with the smallest request-level check that exercises the changed path and one relevant failure path.
