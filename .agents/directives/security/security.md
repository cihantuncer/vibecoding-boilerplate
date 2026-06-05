---
purpose: Security-sensitive procedure.
use_when: Real auth, authorization, secrets, tokens, uploads, downloads, file access, permissions, or trust boundaries.
prefer_index: ./INDEX.md
---

# Security Directive

Identify protected asset, actor, trust boundary, authorization rule, and impact of failure. Enforce permission checks server-side at the resource boundary.

Treat all user-controlled input as untrusted before database, shell, filesystem, template, redirect, or network use. Normalize paths and ensure resolved paths stay inside allowed roots.

Handle tokens and secrets carefully: do not log, expose, weaken, hardcode, or print them. Preserve expiry, audience, scope, rotation, and storage expectations.

For uploads/downloads, check ownership, size, type, path traversal, direct access, and content disposition. Validate with focused abuse cases, not only the happy path.
