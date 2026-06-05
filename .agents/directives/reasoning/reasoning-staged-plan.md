---
purpose: Staged plan and irreversible decision guidance.
use_when: Work needs sequencing, rollback points, migration steps, security-sensitive design, or a decision with hard-to-reverse effects.
prefer_index: ./INDEX.md
---

# Staged Plan Directive

State goal, constraints, non-goals, known facts, assumptions, and what evidence could change the plan. Prefer reversible steps and early validation.

For each stage, define dependency, expected result, rollback point, and validation. Keep open questions few and tied to decisions that cannot be safely inferred.

End with the smallest useful next action, not a broad wish list.
