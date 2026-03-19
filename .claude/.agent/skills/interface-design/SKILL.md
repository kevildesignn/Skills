---
name: interface-design
description: This skill is for interface design — dashboards, admin panels, apps, tools, and interactive products. NOT for marketing design (landing pages, marketing sites, campaigns). Design engineering for Claude Code. Build interfaces with craft, memory, and consistency. Maintains design decisions across sessions.
---

# Interface Design

**Design engineering for dashboards, admin panels, apps, and interactive products.**

Source: [Dammyjay93/interface-design](https://github.com/Dammyjay93/interface-design)

## Scope

This skill applies to:
- Dashboards and data-heavy UIs
- Admin panels and management interfaces
- SaaS product interfaces
- Tools and productivity apps
- Interactive applications

NOT for: landing pages, marketing sites, campaigns.

## The Problem

Most AI-generated interfaces suffer from:
- **Sameness** — Every component looks like every other
- **Generic defaults** — White backgrounds, blue buttons, gray text
- **No system** — Design decisions aren't consistent or intentional

## Intent First

Every design choice must be intentional. Before implementing:

### Every Choice Must Be A Choice
- Typography: What feeling? What hierarchy?
- Color: What emotion? What brand?
- Spacing: What rhythm? What breathing room?
- Motion: What does it reveal about the product?

### Sameness Is Failure
If the design could belong to any product, it belongs to none.

### Intent Must Be Systemic
One intentional token propagated everywhere > many ad-hoc decisions.

## Design Principles

### Token Architecture
Use CSS variables for all design decisions:

```css
:root {
  /* Semantic tokens */
  --surface-base: hsl(var(--background));
  --surface-raised: hsl(var(--card));
  --surface-overlay: hsl(var(--popover));
  
  /* Text hierarchy */
  --text-primary: hsl(var(--foreground));
  --text-secondary: hsl(var(--muted-foreground));
  --text-disabled: hsl(var(--muted-foreground) / 0.5);
  
  /* Control tokens */
  --control-height-sm: 2rem;
  --control-height-md: 2.5rem;
  --control-height-lg: 3rem;
}
```

### Subtle Layering
Use layered surfaces to create depth without shadows:

```css
/* Surface elevation through lightness */
.surface-base    { background: hsl(220 14% 11%); }
.surface-raised  { background: hsl(220 14% 14%); }
.surface-overlay { background: hsl(220 14% 17%); }
```

### Card Layouts
- Consistent padding (16px or 24px)
- Clear header/content/footer separation
- Status indicators at card edge or top

### Controls
- Height consistency across form elements
- Clear focus states (not just outline)
- Disabled states that communicate unavailability

### Animation
- Entrance: `fade-in` + `slide-up` (100-200ms, ease-out)
- Exit: `fade-out` (80-150ms, ease-in)
- State changes: 150ms maximum
- Respect `prefers-reduced-motion`

## Workflow

### Before Starting
1. Check for `system.md` in project root — read it if it exists
2. Understand the product domain and user mental model
3. Commit to an aesthetic direction

### After Completing a Task
1. Update `system.md` with new design decisions
2. Document: colors used, spacing choices, component patterns
3. Note any deviations from existing system and why

## Avoid

- Generic blue primary colors without intention
- Box shadows as the only depth mechanism  
- Lorem ipsum placeholder text
- Inconsistent spacing (mixing 12px, 14px, 16px randomly)
- Components that don't relate to each other visually
- Forgetting dark mode considerations
