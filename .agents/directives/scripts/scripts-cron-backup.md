---
purpose: Cron, backup, and destructive script guidance.
use_when: Scripts delete, move, sync, back up, run on cron, run remotely, or change deployment/state.
prefer_index: ./INDEX.md
---

# Cron/Backup Scripts Directive

Resolve target paths before recursive delete/move/sync. Provide dry-run or preview for destructive, remote, backup, and deploy behavior.

For cron/background jobs, use absolute paths, logging, locking, idempotency, and failure notification. For backups, define source, destination, exclusions, retention, and restore check.

Validate with syntax check and a small test target before real data.
