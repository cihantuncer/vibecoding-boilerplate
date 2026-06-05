---
purpose: Browser E2E and user-flow validation directive.
use_when: Work changes critical user journeys, routing, forms, responsive UI, auth flows, payments/admin surfaces, or behavior that unit tests cannot prove.
prefer_index: ./INDEX.md
---

# E2E Browser Directive

Test from the user's perspective. Prefer one focused flow that proves the changed behavior over broad brittle coverage. Use stable selectors, realistic inputs, and explicit waits for user-visible states.

Cover happy path plus the most relevant failure or edge path when risk warrants it. Avoid depending on arbitrary sleeps, implementation details, or fragile screenshots unless visual regression is the goal.

Validate in a production-like browser path when practical; for responsive work, include the affected viewport.
