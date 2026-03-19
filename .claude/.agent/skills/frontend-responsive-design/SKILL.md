---
name: frontend-responsive-design
description: "Frontend Responsive Design Standards. Mobile-first, fluid layout standards for building responsive web interfaces. Covers breakpoints, fluid grids, flexible images, and responsive typography. Use when building or auditing responsive layouts."
---

# Frontend Responsive Design Standards

Mobile-first, fluid layout standards from [am-will/codex-skills](https://github.com/am-will/codex-skills).

## Core Principles

### Mobile-First Approach
- Start with mobile layout and progressively enhance for larger screens
- Use `min-width` media queries to add complexity as screen grows
- Default styles should be optimized for mobile

### Fluid Grids
- Use relative units (`%`, `vw`, `rem`) instead of fixed pixels for layouts
- CSS Grid and Flexbox for responsive layouts
- Prefer `fr` units in CSS Grid for proportional columns

### Flexible Images
```css
img {
  max-width: 100%;
  height: auto;
}
```

### Responsive Typography
```css
/* Fluid type scale */
:root {
  --step-0: clamp(1rem, 0.9rem + 0.5vw, 1.25rem);
  --step-1: clamp(1.25rem, 1.1rem + 0.75vw, 1.563rem);
  --step-2: clamp(1.563rem, 1.35rem + 1.06vw, 1.953rem);
}
```

## Standard Breakpoints

| Name | Width | Use Case |
|------|-------|----------|
| `sm` | 640px | Small phones |
| `md` | 768px | Tablets |
| `lg` | 1024px | Laptops |
| `xl` | 1280px | Desktops |
| `2xl` | 1536px | Large screens |

## Best Practices

1. **Test across viewports**: Always test at mobile, tablet, and desktop sizes
2. **Touch targets**: Minimum 44×44px for interactive elements
3. **Content priority**: Ensure most important content is visible first on mobile
4. **Performance**: Use responsive images with `srcset` and `sizes`
5. **Avoid horizontal scroll**: Content should never overflow viewport width

## Common Patterns

### Responsive Navigation
- Use hamburger/drawer menu on mobile
- Full nav visible on desktop

### Responsive Cards Grid
```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(300px, 100%), 1fr));
  gap: 1rem;
}
```

### Stack to Row Pattern
```css
.container {
  display: flex;
  flex-direction: column; /* stack on mobile */
}

@media (min-width: 768px) {
  .container {
    flex-direction: row; /* row on tablet+ */
  }
}
```
