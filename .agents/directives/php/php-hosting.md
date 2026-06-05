---
purpose: PHP/shared-hosting procedure.
use_when: cPanel, shared hosting, public PHP, `.htaccess`, tokenized downloads, mail, database config, or file permissions.
prefer_index: ./INDEX.md
---

# PHP Hosting Directive

Assume constrained hosting: limited shell access, older PHP, no long-running processes, Apache/LiteSpeed behavior, and a risky public web root. Keep deployment simple and portable.

Protect config, logs, uploads, private keys, and generated files from direct web access. Prefer storing private files outside public root; if impossible, enforce deny rules and application checks.

For tokenized downloads, validate token, expiry, ownership, path normalization, content type, and logging. Never trust a requested path directly.

Validate with PHP syntax checks, local smoke tests, and host-compatible requests. State host assumptions and manual deployment steps.
