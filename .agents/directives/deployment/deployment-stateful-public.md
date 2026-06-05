---
purpose: Stateful/public deployment guidance.
use_when: Production, public exposure, volumes, databases, uploads, certs, DNS, TLS, proxy, or rollback risk is involved.
prefer_index: ./INDEX.md
---

# Stateful/Public Deployment Directive

Inspect before changing: service status, logs, ports, mounts, env references, proxy config, DNS/TLS, health endpoints, and backups. Treat volumes, uploads, databases, certificates, and generated config as persistent.

For risky commands, state exact command, expected result, affected service, downtime/data risk, rollback path, and validation command first.

Change one layer at a time and validate each meaningful layer.
