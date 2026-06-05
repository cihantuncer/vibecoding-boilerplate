---
purpose: Database/schema/data procedure.
use_when: Migrations, integrity, production data, indexes, transactions, imports, exports, or query performance.
prefer_index: ./INDEX.md
---

# Database Directive

Identify affected tables/models, constraints, indexes, read paths, write paths, and ownership before editing. Treat existing data as valuable; do not drop, truncate, rewrite, or recreate data without explicit approval.

For migrations, prefer reversible steps: add nullable/backfilled fields before enforcing constraints, split risky schema and data operations, and define rollback or recovery. Check whether old and new code can run during deploy.

Use parameterized queries and existing data-access patterns. For transactions, keep the transaction boundary small and handle partial failure explicitly.

Validate with migration dry-run, focused tests, explain/query checks, or a small fixture. State data and rollback risk.
