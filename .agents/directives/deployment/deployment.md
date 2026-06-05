---
purpose: Deployment/operations procedure.
use_when: Production, stateful services, public exposure, Docker, proxy, DNS, TLS, migration, cron, or rollback-sensitive work.
prefer_index: ./INDEX.md
---

# Deployment Directive

Before changing operations, identify environment, runtime, container/host boundary, public/private route, reverse proxy, persistence, and backup state. Inspect configs, logs, ports, mounts, env references, health endpoints, DNS, and TLS before applying changes.

Treat volumes, databases, uploads, certificates, and generated config as persistent. Do not prune, recreate, delete, or overwrite state without explicit approval.

For risky commands, show the exact command, expected outcome, affected service, downtime/data risk, rollback path, and validation command first.

Change one layer at a time: app config, service/container, proxy, DNS/TLS, firewall, migration. Validate after each meaningful layer.
