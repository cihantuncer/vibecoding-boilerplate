# Performance Directives Index

Use for slowness, memory, CPU, latency, query cost, bundle size, and resource use.

- Identify the measured or observable bottleneck first.
- Optimize the hot path only; preserve correctness and public behavior.
- Prefer simple reductions in work, data, renders, queries, or allocation.
- Validate with the same metric or a targeted proxy check.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| obvious small hot-path cleanup | none | this index is enough |
| LCP, CLS, INP, images, fonts, hydration, bundle, main thread, perceived load | `./web-vitals.md` | user-visible web performance may change |
| cache, memoization, batching, debounce, stale data | `./performance-caching.md` | freshness/correctness may change |
| weak measurement or cross-layer optimization | `./performance.md` | risk is not covered by this index |

Open at most one performance directive unless the task clearly needs more.
