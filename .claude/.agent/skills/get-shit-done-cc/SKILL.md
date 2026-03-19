---
name: get-shit-done-cc
description: Use when planning, executing, or managing complex development tasks. A meta-prompting, context engineering and spec-driven development system that solves context rot — the quality degradation that happens as the AI fills its context window. Use for: initializing new projects, planning milestones, executing phases, debugging systematically, managing tasks across sessions. Trigger on: 'build this', 'plan this feature', 'create a new project', 'execute this task', 'debug this issue', 'gsd:', '/gsd'.
---

# GET SHIT DONE (GSD)

A light-weight and powerful meta-prompting, context engineering and spec-driven development system.

**Solves context rot** — the quality degradation that happens as the AI fills its context window.

---

## How It Works

GSD structures every development task through a 6-phase workflow:

### 1. Initialize Project (`/gsd:new-project`)
Runs a structured discussion to extract:
- What you're building and why
- Tech stack and architecture decisions
- Scope of v1 vs future versions
- Success criteria and constraints

Creates: `PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`

### 2. Discuss Phase (`/gsd:discuss-phase [N]`)
Before planning any phase, clarifies:
- Implementation approach
- External dependencies
- Potential blockers
- Assumptions to validate

### 3. Plan Phase (`/gsd:plan-phase [N]`)
Spawns parallel research agents to investigate:
- Stack-specific patterns and pitfalls
- Feature implementation details
- Architecture decisions
- External API/library choices

Creates atomic XML-structured `PLAN.md` tasks with built-in verification steps.

### 4. Execute Phase (`/gsd:execute-phase <N>`)
Spawns parallel executor agents — each with fresh context — to implement tasks in waves. Each task gets its own atomic git commit immediately after completion.

### 5. Verify Work (`/gsd:verify-work [N]`)
Verifier agent checks the codebase against goals. Debugger agents diagnose failures.

### 6. Repeat → Complete → Next Milestone
Archive milestone, tag release, start next version.

---

## Core Commands

### Core Workflow
| Command | What it does |
|---------|--------------|
| `/gsd:new-project [--auto]` | Full initialization: questions → research → requirements → roadmap |
| `/gsd:discuss-phase [N] [--auto]` | Capture implementation decisions before planning |
| `/gsd:plan-phase [N] [--auto]` | Research + plan + verify for a phase |
| `/gsd:execute-phase <N>` | Execute all plans in parallel waves, verify when complete |
| `/gsd:verify-work [N]` | Manual user acceptance testing |
| `/gsd:audit-milestone` | Verify milestone achieved its definition of done |
| `/gsd:complete-milestone` | Archive milestone, tag release |
| `/gsd:new-milestone [name]` | Start next version |

### Navigation
| Command | What it does |
|---------|--------------|
| `/gsd:progress` | Where am I? What's next? |
| `/gsd:help` | Show all commands and usage guide |
| `/gsd:update` | Update GSD with changelog preview |

### Brownfield (Existing Codebases)
| Command | What it does |
|---------|--------------|
| `/gsd:map-codebase` | Analyze existing codebase before new-project — spawns parallel agents to map stack, architecture, conventions, and concerns |

### Phase Management
| Command | What it does |
|---------|--------------|
| `/gsd:add-phase` | Append phase to roadmap |
| `/gsd:insert-phase [N]` | Insert urgent work between phases |
| `/gsd:remove-phase [N]` | Remove future phase, renumber |
| `/gsd:list-phase-assumptions [N]` | See intended approach before planning |
| `/gsd:plan-milestone-gaps` | Create phases to close gaps from audit |

### Session Management
| Command | What it does |
|---------|--------------|
| `/gsd:pause-work` | Create handoff when stopping mid-phase |
| `/gsd:resume-work` | Restore from last session |

### Utilities
| Command | What it does |
|---------|--------------|
| `/gsd:settings` | Configure model profile and workflow agents |
| `/gsd:set-profile <profile>` | Switch model profile (quality/balanced/budget) |
| `/gsd:add-todo [desc]` | Capture idea for later |
| `/gsd:check-todos` | List pending todos |
| `/gsd:debug [desc]` | Systematic debugging with persistent state |
| `/gsd:quick [--full] [--discuss]` | Execute ad-hoc task with GSD guarantees |
| `/gsd:health [--repair]` | Validate `.planning/` directory integrity |

---

## Context Engineering Files

| File | What it does |
|------|--------------|
| `PROJECT.md` | Project vision, always loaded |
| `research/` | Ecosystem knowledge (stack, features, architecture, pitfalls) |
| `REQUIREMENTS.md` | Scoped v1/v2 requirements with phase traceability |
| `ROADMAP.md` | Where you're going, what's done |
| `STATE.md` | Decisions, blockers, position — memory across sessions |
| `PLAN.md` | Atomic task with XML structure, verification steps |
| `SUMMARY.md` | What happened, what changed, committed to history |
| `todos/` | Captured ideas and tasks for later work |

---

## Why It Works

### Multi-Agent Orchestration
Every stage uses a thin orchestrator that spawns specialized agents:

| Stage | Orchestrator does | Agents do |
|-------|------------------|-----------|
| Research | Coordinates, presents findings | 4 parallel researchers investigate stack, features, architecture, pitfalls |
| Planning | Validates, manages iteration | Planner creates plans, checker verifies, loop until pass |
| Execution | Groups into waves, tracks progress | Executors implement in parallel, each with fresh 200k context |
| Verification | Presents results, routes next | Verifier checks codebase against goals, debuggers diagnose failures |

**Result:** You can run an entire phase and your main context window stays at 30-40%. The work happens in fresh subagent contexts.

### Atomic Git Commits
Each task gets its own commit immediately after completion:
```bash
abc123f docs(08-02): complete user registration plan
def456g feat(08-02): add email confirmation flow
hij789k feat(08-02): implement password hashing
lmn012o feat(08-02): create registration endpoint
```

### XML Plan Format
Every plan is structured XML optimized for AI consumption:
```xml
<task type="auto">
  <name>Create login endpoint</name>
  <files>src/app/api/auth/login/route.ts</files>
  <action>
    Use jose for JWT (not jsonwebtoken - CommonJS issues).
    Validate credentials against users table.
    Return httpOnly cookie on success.
  </action>
  <verify>curl -X POST localhost:3000/api/auth/login returns 200 + Set-Cookie</verify>
  <done>Valid credentials return cookie, invalid return 401</done>
</task>
```

---

## Quick Mode

For ad-hoc tasks without full project setup:

```
/gsd:quick Build a contact form with email sending
/gsd:quick --full Add OAuth login with GitHub
/gsd:quick --discuss Refactor the payment service
```

- Default: Executes immediately with GSD guarantees
- `--full`: Adds plan-checking and verification steps  
- `--discuss`: Gathers context before executing

---

## Installation

To install GSD properly in this project, run:

```bash
npx get-shit-done-cc@latest
```

The installer prompts you to choose:
1. **Runtime** — Claude Code, OpenCode, Gemini, Codex, or all
2. **Location** — Global (all projects) or local (current project only)

Verify with: `/gsd:help`

---

## Source
- GitHub: [gsd-build/get-shit-done](https://github.com/gsd-build/get-shit-done)
- npm: [get-shit-done-cc](https://www.npmjs.com/package/get-shit-done-cc)
- By: TÂCHES
