# Security Directives Index

Use for auth, authorization, secrets, tokens, permissions, uploads, downloads, file paths, and trust boundaries.

- Identify protected asset, actor, trust boundary, and failure impact.
- Enforce authorization server-side; never rely only on UI checks.
- Validate and normalize untrusted input before file, DB, shell, or network use.
- Do not print or weaken secrets, tokens, cookies, private keys, or env dumps.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| small permission/input-safety check | none | this index is enough |
| XSS, CSRF, cookies, sessions, redirects, CSP, browser storage, untrusted rendering | `./web-security.md` | browser/web trust boundary may change |
| tokens, secrets, uploads, downloads, private files, path joins | `./security-token-file-transfer.md` | secret/file transfer risk exists |
| auth model, authorization, trust boundary, unclear security risk | `./security.md` | risk is not covered by this index |

Open at most one security directive unless the task clearly needs more.
