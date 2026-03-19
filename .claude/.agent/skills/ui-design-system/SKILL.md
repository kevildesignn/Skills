---
name: ui-design-system
description: "React UI component systems with TailwindCSS + Radix + shadcn/ui. Stack: TailwindCSS (styling), Radix UI (primitives), shadcn/ui (components), React/Next.js. Capabilities: design system architecture, accessible components, responsive layouts, theming, dark mode, component composition. Actions: review, design, build, improve, refactor UI components. Keywords: TailwindCSS, Radix UI, shadcn/ui, design system, component library, accessibility, ARIA, responsive, dark mode, theming, CSS variables, component architecture, atomic design, design tokens, variant, slot, composition. Use when: building component libraries, implementing shadcn/ui, creating accessible UIs, setting up design systems, adding dark mode/theming, reviewing UI component architecture."
license: MIT
version: 2.0.0
---

# UI/UX Design & Development Expert

**Comprehensive UI/UX design, review, and improvement for modern web applications.**

Production-ready implementations with **TailwindCSS + Radix UI + shadcn/ui** and modern React patterns.

## Stack Architecture

### The Three Pillars
1. **TailwindCSS** — Utility-first styling, design tokens via CSS variables
2. **Radix UI** — Headless accessible primitives (dialogs, dropdowns, etc.)
3. **shadcn/ui** — Pre-built components combining Radix + Tailwind

### Architecture Hierarchy
```
TailwindCSS (utilities/tokens)
    └── Radix UI (accessibility + behavior)
        └── shadcn/ui (pre-built components)
            └── Your custom components
```

## Core Capabilities

### UI/UX Review & Audit
- Identify accessibility violations (ARIA, keyboard, contrast)
- Spot design inconsistencies (spacing, color, typography)
- Review component API design

### UI/UX Design
- Build new component systems
- Design tokens and theming
- Responsive layout architecture

### UI/UX Improvement
- Refactor existing components
- Improve performance and accessibility
- Modernize legacy UI patterns

## When to Use Each Layer

### Use TailwindCSS Directly When:
- Simple, one-off styling needs
- Responsive adjustments
- Animation and transition utilities

### Use Radix UI Primitives When:
- Need full control over markup
- Building custom component variants
- Complex accessibility requirements

### Use shadcn/ui Components When:
- Need a quick, production-ready solution
- Standard UI patterns (buttons, inputs, cards)
- Consistent with existing design system

## Critical Design Principles

### 1. Progressive Enhancement
Start with semantic HTML, enhance with CSS, then JS behaviors.

### 2. Composition Over Complexity
Small, focused components composed together over large monolithic ones.

### 3. Accessibility First
Every component must be keyboard navigable and screen-reader friendly.

### 4. Design Token Consistency
Use CSS variables for all design decisions, never hardcode values.

### 5. Mobile-First Responsive
Build for mobile first, enhance for larger screens.

## Design Token Architecture

```css
:root {
  /* Colors */
  --background: 0 0% 100%;
  --foreground: 222.2 84% 4.9%;
  --primary: 222.2 47.4% 11.2%;
  --primary-foreground: 210 40% 98%;
  
  /* Spacing scale */
  --spacing-1: 0.25rem;
  --spacing-2: 0.5rem;
  --spacing-4: 1rem;
  --spacing-8: 2rem;
  
  /* Typography */
  --font-sans: 'Inter', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
  
  /* Radius */
  --radius: 0.5rem;
}
```

## Accessibility Standards

### WCAG Requirements
- **AA**: 4.5:1 contrast for text, 3:1 for large text/UI components
- **AAA**: 7:1 contrast for text (aim for where possible)

### Radix UI Built-In Guarantees
- ARIA attributes automatically managed
- Keyboard navigation patterns per WAI-ARIA spec
- Focus management in dialogs, menus, sheets

## Resources

- [TailwindCSS Docs](https://tailwindcss.com/docs)
- [Radix UI Primitives](https://www.radix-ui.com/primitives)
- [shadcn/ui Components](https://ui.shadcn.com)
- [WAI-ARIA Patterns](https://www.w3.org/WAI/ARIA/apg/patterns/)
