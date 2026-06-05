# Reasoning Directives Index

Use for planning, architecture, tradeoffs, uncertainty, risky multi-step work, or broad decisions.

- State the goal, constraints, evidence needed, and smallest useful next step.
- Separate known facts from assumptions.
- Prefer reversible decisions and local evidence.
- Avoid expanding scope unless it materially reduces risk.
- If Sequential Thinking MCP is available, use it for multi-step reasoning chains where intermediate decisions depend on earlier analysis results.

## Route Map

| Signal | Directive | Open when |
|---|---|---|
| small planning/tradeoff question | none | this index is enough |
| start project, continue, resume, roadmap, next task, project status, where left off | `./project-continuation.md` | project lifecycle context is needed |
| sequencing, rollback, migration steps, irreversible choice | `./reasoning-staged-plan.md` | staged plan is needed |
| high-impact architecture or many unknowns | `./reasoning.md` | risk is not covered by this index |

Open at most one reasoning directive unless the task clearly needs more.
