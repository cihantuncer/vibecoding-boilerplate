---
purpose: Database migration and integrity directive.
use_when: Schema, constraint, index, migration, backfill, import/export, or production data behavior may change.
prefer_index: ./INDEX.md
---

# Database Migrations Directive

Treat existing data as durable. Prefer reversible steps: add nullable fields, backfill safely, then enforce constraints. Split risky schema and data operations when possible.

Check old/new code compatibility during deploy. Do not drop, truncate, rewrite, or recreate data without explicit approval and a recovery path.

Validate with migration dry-run, focused fixture, explain/query check, or rollback check. State data risk and whether rollback is mechanical or manual.
