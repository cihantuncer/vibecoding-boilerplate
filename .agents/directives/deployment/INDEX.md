# Deployment Directives Index

Use for Docker, servers, reverse proxies, DNS, TLS, cron, runtime config, migrations, and public exposure.

- Inspect config, logs, ports, mounts, env references, and persistence before changing anything.
- Treat production, volumes, databases, certs, and uploads as stateful.
- Prefer dry-runs, backups, one-layer changes, and explicit rollback.
- Validate with status, logs, health checks, curl, DNS, or TLS checks.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| local runtime/config inspection | none | this index is enough |
| production, public route, volumes, DB, DNS, TLS, proxy | `./deployment-stateful-public.md` | state or exposure may change |
| deployment risk not otherwise covered | `./deployment.md` | rollback/validation needs detail |

Open at most one deployment directive unless the task clearly needs more.
