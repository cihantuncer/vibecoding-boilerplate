# Debugging Directives Index

Use for broken behavior, crashes, failing commands, failing tests, and unexpected results.

- Capture the exact symptom and reproduction path before patching.
- Inspect the narrowest likely path; avoid broad rewrites.
- Form a small hypothesis, test it against evidence, then patch minimally.
- Validate the original failure path.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| routine reproducible bug | none | this index is enough |
| flaky, machine-specific, config, timeout, order, cache | `./debugging-intermittent-config.md` | failure is not deterministic |
| unclear root cause, deployment/security-sensitive bug | `./debugging.md` | risk is not covered by this index |

Open at most one debugging directive unless the task clearly needs more.
