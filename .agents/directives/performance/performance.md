---
purpose: Performance procedure.
use_when: Weak measurement, caching, hot paths, memory/CPU pressure, query cost, bundle size, or cross-layer optimization.
prefer_index: ./INDEX.md
---

# Performance Directive

Define the performance problem with evidence: metric, trace, slow query, bundle output, memory profile, repeated render, or observed latency. Avoid optimizing without a baseline.

Find the hot path and reduce work there: fewer queries, smaller payloads, less allocation, fewer renders, less blocking I/O, better indexes, or narrower cache invalidation.

Preserve correctness. Be careful with caching, batching, debounce/throttle, lazy loading, and memoization because they can change freshness, ordering, or error behavior.

Validate against the original metric or a targeted proxy. State measurement limits and any tradeoff introduced.
