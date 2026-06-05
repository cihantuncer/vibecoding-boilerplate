# Vibe Coding Agent Environment Boilerplate

Author: Cihan Tuncer  
License: CC0 1.0 Universal (`CC0-1.0`)

Token-friendly, on-demand agent configuration boilerplate. Designed for Codex, Gemini, Claude, and other agentic IDEs.

This boilerplate structures how AI agents read rules, plans, roadmaps, and directives—preventing token waste by keeping context loading strictly on-demand.

---

## Philosophy

* **On-Demand & Modular:** Load only what is needed. Avoid massive system prompts.
* **Separation of Concerns:**
  * **Rules:** Invariants (always on).
  * **Directives:** General best practices (loaded per task).
  * **Project Directives:** Local overrides.
  * **Plans/Roadmaps:** Project trajectory (loaded only for project start, resume, handoff, or roadmap execution tasks).
* **Truth in Code:** Memory is a hint; the actual workspace files are the ultimate source of truth.

---

## Context Reading Flow

To save tokens, the agent loads context in a strict hierarchy:

1. **Bootstrap & Router:** `ROUTER.md` directs the agent to the right topic.
2. **Topic Index:** The agent loads **exactly one** topic `INDEX.md` (e.g., `.agents/directives/frontend/INDEX.md`).
3. **Specific Directive:** Only if needed, it opens a detailed file (e.g., `react-state.md`).
4. **Project Lifecycle:** Large plan/roadmap files are **only** read during bootstrap/continuation phases, not for localized code edits.

---

## Quick Start (How to Use)

Follow these simple steps to integrate this template into your project:

### 1. Copy the Structure
Copy the `.agents/` and `docs/` directories directly into your project root.

```text
your-project/
├── .agents/
│   ├── ROUTER.md
│   ├── rules/
│   ├── directives/
│   └── project-directives/
└── docs/
    ├── plan/
    └── roadmap/
```

### 2. Configure Your Agent Rules
* **Global Agent Bootstrap:** Rename `_AGENTS.override._md` in the project root to `AGENTS.override.md` (or copy its contents to your IDE's global system instructions/rules configuration) so the agent knows how to interact with the router, MCPs, and directives.
* **Project-specific Rules:** (Optional) Rename `.agents/rules/_common._md` to `.agents/rules/common.md` to define project-specific, always-on constraints.

### 3. Initialize the Workspace (Project Bootstrap)
When you are ready to start, give your agent a prompt to initialize (e.g., *"Read the boilerplate and initialize the workspace to build X"*):
* The agent will trigger the bootstrap and continuation workflow (`.agents/directives/reasoning/project-continuation.md`).
* **Environment Verification:** It can help verify and configure the recommended MCP servers and starter skills listed in this `README.md`.
* **Roadmap & Plan:**
  * **If a plan exists (`docs/plan/`):** It will scan the plan to understand the goals and automatically create `docs/roadmap/STATUS.md` to start tracking progress.
  * **If no plan exists yet:** It will offer to discuss your requirements and generate an implementation plan in `docs/plan/` first before creating the roadmap.

---

## Recommended Stack

### 1. Prerequisite CLI Tools
Ensure these tools are installed on your machine or project before starting:

* **[Ripgrep (rg)](https://github.com/BurntSushi/ripgrep):** Required for fast code search (used by agents for text and file discovery).
* **[Node.js](https://nodejs.org/):** Runtime for running skills, utilities, and helper tools.
* **[Git](https://git-scm.com/):** For version control and workspace state checking.

Optional tools:

* **[Playwright](https://playwright.dev/):** Required only if you use browser/E2E testing skills (`npm install -D @playwright/test` and `npx playwright install`).

### 2. MCP Servers
Install only what you need. Click the links to learn more about each server:

* **[Context7](https://github.com/upstash/context7):** Web documentation queries for libraries and APIs.
* **[Cavemem](https://github.com/JuliusBrussee/cavemem):** Local, cross-agent persistent memory.
* **[Serena](https://github.com/oraios/serena):** IDE-like symbol-level code navigation and editing capabilities.
* **[Chrome DevTools](https://github.com/ChromeDevTools/chrome-devtools-mcp):** Browser automation, UI debugging, and console logging.
* **[Toolbox for Databases](https://github.com/googleapis/mcp-toolbox):** Developer database inspection.

### 3. Recommended Skills
Enable skills selectively. Do not load large catalogs by default.

* **[skill-security-auditor](https://github.com/alirezarezvani/claude-skills/tree/main/engineering/skills/skill-security-auditor)** (Pre-install safety check)
* **[dependency-auditor](https://github.com/alirezarezvani/claude-skills/tree/main/engineering/skills/dependency-auditor)** (Vulnerability & upgrade paths)
* **[log-summarizer](https://github.com/proflead/codex-skills-library/tree/master/skills/foundation/log-summarizer)** (Log triaging)
* **[ci-failure-triage](https://github.com/proflead/codex-skills-library/tree/master/skills/infra/ci-failure-triage)** (Pipeline stabilizer)
* **[integration-testing](https://github.com/kid-sid/codex-spellbook/tree/main/skills/integration-testing)** (E2E/automated testing)
* **[playwright-pro](https://github.com/alirezarezvani/claude-skills/tree/main/engineering-team/playwright-pro)** (Playwright testing toolkit)

## Support

[![Buy Me a Coffee](https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png)](https://buymeacoffee.com/cihantr)
