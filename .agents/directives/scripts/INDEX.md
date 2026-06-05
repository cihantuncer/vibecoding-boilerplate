# Scripts Directives Index

Use for Bash, PowerShell, cron, rsync, backup, maintenance, and automation.

- Identify OS, shell, working directory, permissions, and target paths.
- Use safe quoting and explicit paths; avoid string-built destructive commands.
- Add dry-run or preview behavior for risky file, remote, or state changes.
- Validate with a small local run or syntax check.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| small local script edit | none | this index is enough |
| delete, move, sync, backup, cron, remote, deploy | `./scripts-cron-backup.md` | state or schedule may change |
| permissions, background jobs, unclear shell risk | `./scripts.md` | risk is not covered by this index |

Open at most one scripts directive unless the task clearly needs more.
