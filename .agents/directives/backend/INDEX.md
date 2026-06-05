# Backend Directives Index

Use for APIs, routes, services, middleware, server-side validation, and integrations.

- Identify the request boundary, caller, inputs, outputs, and existing contract.
- Preserve response shape, status codes, auth behavior, and error semantics unless asked.
- Validate inputs at the boundary; keep business logic in the existing local pattern.
- Check nearby tests or add focused validation when behavior changes.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| routine backend/API edit | none | this index is enough |
| new REST endpoint, resource naming, method semantics, filtering, sorting, versioning | `./rest-api-design.md` | REST API shape is being designed |
| response shape, status code, pagination, idempotency, public caller | `./backend-api-contract.md` | public contract may change |
| data writes, external service, auth side effect, unclear backend risk | `./backend.md` | risk is not covered by this index |

Open at most one backend directive unless the task clearly needs more.
