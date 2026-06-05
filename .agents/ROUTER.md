# Agent Router

Use the smallest useful instruction set.

Directive indexes live at `.agents/directives/<topic>/INDEX.md`.
Detailed directives live under the same topic folder.

Default: this router + 1 topic index. Topic indexes act as mini-routers for detailed directives. Open a detailed directive only when the selected index points to it.

If `.agents/PROJECT_ROUTER.md` exists, scan it after this router for project-specific overlays or project-only topics.

## Escalation

- Start with the selected topic index; do not open detailed directives by default.
- Before reading code, scan that topic index route map.
- Open one detailed directive only when a route signal matches or the task has high risk: production, data loss, auth/security, migration, public exposure, broad refactor, or unclear multi-step work.
- Add one support topic index only for clear cross-domain risk; otherwise do not.
- Keep specialized detailed directives out of this router; add them to the relevant topic `INDEX.md` route map.
- Open at most one project directive index from `.agents/project-directives/` when `.agents/PROJECT_ROUTER.md` matches the task or a matching topic overlay exists.
- Read `.agents/CONTINUITY.md` only when it exists and prior decisions matter.

## Route Map

| Situation | Topic | Detailed when |
|---|---|---|
| bug, crash, failing command | debugging | unclear root cause, risky fix, intermittent |
| planning, architecture, tradeoff | reasoning | high impact or many unknowns |
| start project, continue, resume, roadmap, next task, project status | reasoning | project lifecycle context is needed |
| refactor, cleanup, reorganize | refactoring | broad/shared behavior or weak tests |
| tests, coverage, mocks | testing | flaky, broad, or security-sensitive |
| auth, token, secret, permission, upload, download, file path | security | real trust boundary or secret |
| Docker, deploy, server, proxy, DNS, TLS, migration | deployment | production, stateful, or public |
| frontend, UI, CSS, DOM, React, accessibility, mobile, layout, overflow | frontend | critical flow, complex state, auth/admin UI, responsive/visual risk |
| backend, API, route, service, middleware | backend | public contract, auth, external service, data risk |
| PHP, cPanel, shared hosting, `.htaccess` | php | public hosting, tokenized files, server config |
| Bash, PowerShell, cron, rsync, backup, automation | scripts | destructive, scheduled, remote, backup, deploy |
| database, SQL, schema, index | database | migration, integrity, performance, prod data |
| slow, memory, CPU, latency, bundle size | performance | behavior might change |
| README, docs, comments, examples, roadmap | documentation | durable architecture/product docs |

## Support Topics

Use at most one support topic index, only when the task clearly crosses domains:

- `security`: auth, tokens, secrets, permissions, uploads, downloads, file paths, public exposure.
- `testing`: new/changed validation strategy, regression coverage, critical user flow.
- `deployment`: runtime, cron, server, Docker, migration, public service behavior.
- `database`: schema, migration, transaction, query, or production data impact.

## Project Docs

Use `docs/plan/README.md` or `docs/roadmap/README.md` only for product, architecture, roadmap, or durable context.

Do not read project docs for localized fixes such as UI layout, CSS, bugs, tests, scripts, or small backend changes unless the task explicitly asks for product or architecture context.

Do not load all plan, roadmap, topic, or directive files.

## Folder Policy

Keep instructions task-based by default. Add stack folders such as `web-js/` only when many reusable stack-specific rules exist; otherwise inspect nearby code.
