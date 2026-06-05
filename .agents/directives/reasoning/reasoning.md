---
purpose: Planning/reasoning procedure.
use_when: High-impact architecture, many unknowns, irreversible choices, migrations, security-sensitive design, or staged work.
prefer_index: ./INDEX.md
---

# Reasoning Directive

Start with goal, constraints, stakeholders, non-goals, and evidence needed. Separate facts from assumptions and name what would change the decision.

Prefer small reversible steps. If multiple approaches exist, compare them by risk, implementation cost, maintenance cost, user impact, and validation path.

For staged work, define sequence, dependencies, rollback points, and what can be verified after each stage. Avoid turning analysis into implementation unless the user asked for action.

End with a concrete recommendation or next action. Keep open questions few and only for decisions that cannot be safely inferred.
