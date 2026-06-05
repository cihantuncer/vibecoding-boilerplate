---
purpose: Caching and freshness guidance.
use_when: Performance work uses caching, memoization, batching, debounce/throttle, lazy loading, or stale data tradeoffs.
prefer_index: ./INDEX.md
---

# Performance Caching Directive

Start with the bottleneck and freshness requirement. Define cache key, scope, invalidation, lifetime, error behavior, and user-visible staleness.

Caching must preserve authorization, ordering, and correctness. Avoid hiding slow or broken behavior behind stale data unless that tradeoff is intentional.

Validate with the original metric and a freshness/invalidation check. State the correctness tradeoff, if any.
