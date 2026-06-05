---
purpose: Token, secret, upload, download, and file-path security guidance.
use_when: Work handles tokens, secrets, cookies, uploads, downloads, private files, path joins, or direct file access.
prefer_index: ./INDEX.md
---

# Token/File Transfer Security Directive

Do not log, expose, hardcode, weaken, or print secrets/tokens. Preserve expiry, audience, scope, rotation, storage, and revocation expectations.

For files, normalize paths and verify resolved paths stay inside allowed roots. Check ownership, size, type, path traversal, direct access, and content disposition.

Validate happy path plus at least one denied or abuse case.
