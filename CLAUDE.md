# HoM - Claude Skills System

This project contains a curated library of Claude agent skills organized by domain.
All skills live in `.claude/.agent/skills/<skill-name>/SKILL.md`.

## How to Use

When asked to help with a task, identify the relevant category below, read that category's `SKILLS.md`, then read the specific `SKILL.md` files listed there. Only load categories needed for the current task.

> Example: User asks for UI design help → read `categories/design/SKILLS.md` → read the specific SKILL.md files listed there → apply that knowledge.

## Skill Categories

| Category | Folder | What it covers |
|---|---|---|
| Design & UI/UX | `categories/design/` | Visual design, frontend aesthetics, UX research, motion, brand |
| Engineering | `categories/engineering/` | Backend, frontend dev, DevOps, mobile, data engineering |
| Testing & QA | `categories/testing/` | TDD, accessibility audits, API testing, anti-patterns |
| Writing & Docs | `categories/writing/` | Technical writing, plans, clear communication, co-authoring |
| Marketing | `categories/marketing/` | Social media, growth, app store optimization, content |
| Product | `categories/product/` | Strategy, sprint prioritization, feedback synthesis |
| Project Management | `categories/project-management/` | Studio ops, project shepherding, experiment tracking |
| AI & Agents | `categories/ai-agents/` | AI engineering, agent orchestration, Claude API |
| Debugging | `categories/debugging/` | Systematic debugging, root cause tracing, verification |
| MCP & Plugins | `categories/mcp-plugins/` | MCP builders, hooks, plugin structure |
| Data & Documents | `categories/data-documents/` | xlsx, pdf, pptx, docx, data pipelines |
| XR & Spatial | `categories/xr-spatial/` | VisionOS, XR interfaces, spatial computing |
| Creative | `categories/creative/` | Brainstorming, ideation, algorithmic art, thinking tools |
| Communication | `categories/communication/` | Slack messaging, internal comms, GIFs |
| Workflow | `categories/workflow/` | Git, code review, skill management, productivity |
| Security | `categories/security/` | Security engineering, compliance, defense in depth |
| Support & Ops | `categories/support-ops/` | Customer support, finance, infrastructure, reporting |

## Navigation Rules

1. **Single-domain request** — load one category's `SKILLS.md`
2. **Multi-domain request** — load multiple category `SKILLS.md` files
3. **Unknown domain** — pick the closest category from the table above
4. **Skill variants** — skills with `--obra-superpowers-skills`, `--anthropics-skills`, etc. are enhanced versions of the base skill; prefer the variant that best matches context

## Skills Base Path

```
.claude/.agent/skills/<skill-name>/SKILL.md
```
