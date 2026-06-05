---
purpose: PHP tokenized file/download guidance.
use_when: Shared-hosting PHP handles private files, tokenized downloads, uploads, paths, or public web-root protection.
prefer_index: ./INDEX.md
---

# PHP Tokenized Downloads Directive

Never trust a requested path directly. Validate token, expiry, ownership, path normalization, content type, and allowed root. Prefer private files outside public web root.

If files must live under public root, deny direct access and serve through application checks. Avoid leaking full paths or token values in logs/errors.

Validate happy path, expired token, wrong owner, and path traversal.
