---
purpose: Script/automation procedure.
use_when: Deletion, moves, backups, cron, remote commands, deployment automation, permissions, background jobs, or stateful scripts.
prefer_index: ./INDEX.md
---

# Scripts Directive

Identify shell, OS, working directory, permissions, environment, target paths, and whether the script runs locally, remotely, in cron, or in CI. Make paths explicit and quote carefully.

For file operations, validate resolved paths before delete/move/copy, especially recursive operations. Provide dry-run or preview for destructive, remote, backup, or sync behavior.

For cron/background jobs, handle logging, locking, idempotency, failure notification, and relative paths. For backups, define source, destination, retention, restore check, and exclusion rules.

Validate with syntax checks, dry-runs, or small test directories before real targets.
