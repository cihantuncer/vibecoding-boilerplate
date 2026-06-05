---
purpose: Intermittent and environment/config debugging guidance.
use_when: Failure is flaky, machine-specific, config-driven, time/order dependent, or not locally reproducible.
prefer_index: ./INDEX.md
---

# Intermittent/Config Debugging Directive

Separate symptom from environment. Capture command, inputs, timestamps, versions, env references without secrets, logs, and frequency. Look for ordering, race, timeout, path, permissions, clock, cache, and config differences.

Avoid speculative rewrites. Add narrow logging or assertions only where they prove the failing state.

If not reproduced, explain the evidence chain and validate the closest deterministic path.
