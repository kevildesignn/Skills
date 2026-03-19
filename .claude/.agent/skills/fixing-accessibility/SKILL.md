---
name: fixing-accessibility
description: Audit and fix HTML accessibility issues including ARIA labels, keyboard navigation, focus management, color contrast, and form errors. Use when adding interactive controls, forms, dialogs, or reviewing WCAG compliance.
---

# fixing-accessibility

## how to use
- `/fixing-accessibility`
  Apply these constraints to any UI work in this conversation.

- `/fixing-accessibility <file>`
  Review the file against all rules below and report:
  - violations (quote the exact line or snippet)
  - why it matters (one short sentence)
  - a concrete fix (code-level suggestion)

Do not rewrite large parts of the UI. Prefer minimal, targeted fixes.

## when to apply
Reference these guidelines when:
- adding or changing buttons, links, inputs, menus, dialogs, tabs, dropdowns
- building forms, validation, error states, helper text
- implementing keyboard shortcuts or custom interactions
- working on focus states, focus trapping, or modal behavior
- rendering icon-only controls
- adding hover-only interactions or hidden content

## rule categories by priority

| priority | category | impact |
|----------|----------|--------|
| 1 | accessible names | critical |
| 2 | keyboard access | critical |
| 3 | focus and dialogs | critical |
| 4 | semantics | high |
| 5 | forms and errors | high |
| 6 | announcements | medium-high |
| 7 | contrast and states | medium |
| 8 | media and motion | low-medium |
| 9 | tool boundaries | critical |

## quick reference

### 1. accessible names (critical)
- Every interactive element must have an accessible name
- Icon-only buttons: use `aria-label` or `<span class="sr-only">`
- Images: use meaningful `alt` or `alt=""` for decorative images
- Form inputs: always associate with `<label>` via `for`/`id` or `aria-label`

### 2. keyboard access (critical)
- All interactive elements must be keyboard reachable
- Custom components: implement full keyboard patterns (arrow keys, Enter, Space, Escape)
- Never remove `outline` without providing a visible alternative
- Tab order must follow visual/logical reading order

### 3. focus and dialogs (critical)
- Modals: trap focus inside when open, restore focus on close
- New content: move focus to the newly opened region
- Skip links: provide "Skip to main content" as first focusable element

### 4. semantics (high)
- Use semantic HTML over `<div>` for interactive elements
- Landmark regions: `<main>`, `<nav>`, `<header>`, `<footer>`, `<aside>`
- Heading hierarchy must not skip levels (h1 → h2 → h3)

### 5. forms and errors (high)
- Inline errors: associate with `aria-describedby`
- Required fields: use `aria-required="true"` or native `required`
- Group related inputs with `<fieldset>` + `<legend>`

### 6. announcements (medium-high)
- Dynamic changes: use `aria-live` regions for status updates
- Loading states: announce with `aria-busy` or live region
- Form submission results must be announced

### 7. contrast and states (medium)
- Text contrast: minimum 4.5:1 (AA) for normal text, 3:1 for large text
- Focus indicators: minimum 3:1 contrast against adjacent color
- Always indicate disabled, selected, and expanded states visually

### 8. media and motion (low-medium)
- Videos: provide captions and transcripts
- Auto-playing media: provide pause/stop control
- Animations: respect `prefers-reduced-motion`

## common fixes

```tsx
// ❌ Bad
<button><SearchIcon /></button>

// ✅ Good
<button aria-label="Search"><SearchIcon /></button>
```

```tsx
// ❌ Bad
<div onClick={handleClick}>Click me</div>

// ✅ Good
<button onClick={handleClick}>Click me</button>
```

```css
/* ❌ Bad */
:focus { outline: none; }

/* ✅ Good */
:focus-visible { outline: 2px solid var(--color-focus); outline-offset: 2px; }
```
