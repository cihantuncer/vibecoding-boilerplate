---
purpose: Web application security directive.
use_when: Web work touches rendering untrusted data, forms, cookies, sessions, CSRF, redirects, CSP, auth UI, browser storage, or client/server trust boundaries.
prefer_index: ./INDEX.md
---

# Web Security Directive

Treat browser input, URL params, stored content, headers, and third-party data as untrusted. Preserve output encoding, safe templating, CSRF protection, secure cookie settings, redirect allowlists, and auth/session boundaries.

Do not move authorization decisions into client-only checks. Avoid unsafe HTML injection, token storage in risky browser locations, leaking secrets to bundles/logs, or weakening CSP/security headers.

Validate at least one abuse case when security behavior changes: XSS-like content, forbidden action, invalid CSRF/session, unsafe redirect, or unauthorized resource access.
