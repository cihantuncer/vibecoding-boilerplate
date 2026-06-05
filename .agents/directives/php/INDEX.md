# PHP Hosting Directives Index

Use for PHP on shared hosting, cPanel, LiteSpeed, Apache, `.htaccess`, and constrained servers.

- Assume limited shell access, limited process control, and public web-root risk.
- Keep structure simple and compatible with host PHP/version limits.
- Protect configs, uploads, tokens, and non-public files from direct access.
- Validate with local PHP checks or hosting-compatible smoke tests.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| routine PHP/shared-hosting edit | none | this index is enough |
| private files, uploads, tokenized downloads, path handling | `./php-tokenized-downloads.md` | file access must be protected |
| `.htaccess`, mail, DB config, permissions, hosting limits | `./php-hosting.md` | risk is not covered by this index |

Open at most one PHP directive unless the task clearly needs more.
