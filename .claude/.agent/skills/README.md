# 🎨 Portfolio Skills

This folder contains all AI agent skills available to the portfolio project.
Skills are instruction sets that give the AI agent specialized knowledge and workflows for specific domains.

---

## ✅ Installed Skills

| Skill | Source | Description |
|-------|--------|-------------|
| `motion-designer` | `dylantarre/animation-principles` | Disney's 12 principles of animation for designing beautiful, meaningful motion |
| `get-shit-done-cc` | `gsd-build/get-shit-done` | Meta-prompting, context engineering & spec-driven development system. Solves context rot for complex builds |

---

## 📋 Planned Skills (from `skills.sh`)

These skills are listed in `skills.sh` for future installation via `npx skills add`:

| Skill | Source Repo | Description |
|-------|------------|-------------|
| `chat-ui` | `inference-sh-9/skills` | Premium chat UI patterns & components |
| `Frontend Responsive Design Standards` | `am-will/codex-skills` | Mobile-first, fluid layout standards |
| `frontend-design` | `anthropics/skills` | Anthropic-grade frontend design principles |
| `tools-ui` | `inference-sh-9/skills` | Tool invocation UI components |
| `agent-ui` | `inference-sh-9/skills` | Agentic interface design patterns |
| `shadcn-ui` | `giuseppe-trisciuoglio/developer-kit` | Shadcn/Radix design system skill |
| `fixing-accessibility` | `ibelick/ui-skills` | A11y auditing & remediation |
| `ui-design-system` | `samhvw8/dot-claude` | Centralized design token system |
| `superdesign` | `superdesigndev/superdesign-skill` | Super-premium visual design |
| `interface-design` | `dammyjay93/interface-design` | Premium interface design workflows |
| `tailwind-design-system` | `wshobson/agents` | TailwindCSS design system |

---

## 📁 Folder Structure

```
skills/
├── README.md                          ← This file
│
├── motion-designer/
│   └── SKILL.md                       ← Disney's 12 animation principles
│
└── get-shit-done-cc/
    └── SKILL.md                       ← GSD workflow system — `/gsd:` commands
```

---

## 🔧 How to Use Skills

### get-shit-done-cc — Start a new project workflow:
```
/gsd:new-project
```

### Add more skills:
```bash
npx skills add https://github.com/<owner>/<repo> --skill <skill-name>
```

Or install the full planning system:
```bash
npx get-shit-done-cc@latest
```
