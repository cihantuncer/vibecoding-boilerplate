---
purpose: Project continuation and roadmap execution workflow.
use_when: User asks to start, continue, resume, find current status, pick the next task, or work from plan/roadmap.
prefer_index: ./INDEX.md
---

# Project Continuation Directive

Use the smallest lifecycle context that explains where the project stands. First check `.agents/CONTINUITY.md` only if it exists; it overrides roadmap because it records active unfinished work.

Then read `docs/roadmap/STATUS.md` if it exists, followed by `docs/roadmap/README.md` only when needed. If roadmap files are missing, read `docs/plan/README.md`. If a plan exists, propose it to the user for discussion. Once the plan is agreed upon, create `docs/roadmap/README.md` and `docs/roadmap/STATUS.md` automatically without asking. If no plan exists either, ask the user to describe the project.

Structure the plan as `docs/plan/README.md` (index with reading order) linking to numbered topic files (e.g. `01-product-concept.md`, `02-architecture.md`). Keep each file focused on one topic.

Report current state, last completed work, blocker, and the smallest next action. Ask before inventing roadmap scope when product decisions are still open.

When completing roadmap work, update `docs/roadmap/STATUS.md` and the relevant roadmap checkbox. Do not use this directive for small localized fixes unless the user ties them to roadmap progress.

## Project Bootstrap

When starting a new project (first task or explicit "start project" signal), perform these one-time setup steps:

- **CONTINUITY.md**: Does not exist by default. Create `.agents/CONTINUITY.md` after the first meaningful progress to record active unfinished work, blockers, and next step. Keep it concise.
- **MCP & Skill Verification**: Review the recommended MCPs and starter skills in `README.md`. Check which ones are already configured in the environment. Help the user configure the missing ones. **Crucial:** Always perform a quick test call to verify that you can successfully see and invoke the tools of each configured MCP server or skill.
- **Serena configuration**: Set `languages:` in `.serena/project.yml` to match the project stack (e.g. `[typescript]`, `[python]`). Then run Serena onboarding to discover build/test commands.
- **Directive pruning**: Review `.agents/directives/` topics against the project stack. List any topics that do not apply (e.g. `php/` for a Node project) and remove them.
- **Skill deactivation list**: Review installed skills and list the ones that are irrelevant to the project stack. Present this list to the user once so they can deactivate via skill-manager. Do not attempt to deactivate skills yourself or check again later.
