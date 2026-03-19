---
name: design-system-patterns
description: Build scalable design systems with design tokens, theming infrastructure, and component architecture patterns. Use when creating design tokens, implementing theme switching, building component libraries, or establishing design system foundations.
---

# Design System Patterns

Build scalable design systems with design tokens, theming infrastructure, and component architecture.

Source: [wshobson/agents](https://github.com/wshobson/agents) — `plugins/ui-design/skills/design-system-patterns`

## When to Use This Skill

- Creating a design token system from scratch
- Implementing multi-theme support (light/dark/custom)
- Building a component library with consistent variants
- Setting up Style Dictionary for token pipeline
- Establishing design system governance

## Core Capabilities

### 1. Design Tokens
Semantic token layers that map raw values to purpose:

```ts
// tokens/colors.ts
export const colors = {
  // Primitives (raw values)
  slate: {
    50: '#f8fafc',
    900: '#0f172a',
  },
  // Semantic (purpose-mapped)
  semantic: {
    background: { DEFAULT: '{colors.slate.50}', dark: '{colors.slate.900}' },
    foreground: { DEFAULT: '{colors.slate.900}', dark: '{colors.slate.50}' },
  },
};
```

### 2. Theming Infrastructure

```tsx
// Theme switching with React Context
const ThemeContext = createContext<Theme>('light');

export function ThemeProvider({ children, defaultTheme = 'light' }) {
  const [theme, setTheme] = useState(defaultTheme);
  
  useEffect(() => {
    document.documentElement.setAttribute('data-theme', theme);
  }, [theme]);
  
  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      {children}
    </ThemeContext.Provider>
  );
}
```

### 3. Component Architecture with CVA

```tsx
import { cva, type VariantProps } from 'class-variance-authority';

const button = cva(
  'inline-flex items-center justify-center rounded-md font-medium transition-colors',
  {
    variants: {
      variant: {
        default: 'bg-primary text-primary-foreground hover:bg-primary/90',
        outline: 'border border-input bg-background hover:bg-accent',
        ghost: 'hover:bg-accent hover:text-accent-foreground',
      },
      size: {
        sm: 'h-9 px-3 text-sm',
        md: 'h-10 px-4',
        lg: 'h-11 px-8 text-lg',
      },
    },
    defaultVariants: {
      variant: 'default',
      size: 'md',
    },
  }
);

interface ButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement>,
    VariantProps<typeof button> {}

export function Button({ variant, size, className, ...props }: ButtonProps) {
  return <button className={button({ variant, size, className })} {...props} />;
}
```

### 4. Token Pipeline with Style Dictionary

```json
// style-dictionary.config.json
{
  "source": ["tokens/**/*.json"],
  "platforms": {
    "css": {
      "transformGroup": "css",
      "prefix": "ds",
      "buildPath": "dist/css/",
      "files": [{ "destination": "variables.css", "format": "css/variables" }]
    },
    "ts": {
      "transformGroup": "js",
      "buildPath": "dist/ts/",
      "files": [{ "destination": "tokens.ts", "format": "javascript/es6" }]
    }
  }
}
```

## Key Patterns

### Pattern 1: Token Hierarchy
```
Global tokens (raw values)
  └── Alias tokens (semantic meaning)
        └── Component tokens (component-specific)
```

### Pattern 2: Theme Switching
Use `data-theme` attribute on `:root` to switch CSS variable sets.

### Pattern 3: Variant System
Use CVA (class-variance-authority) for type-safe, composable component variants.

## Best Practices

1. **Single source of truth** — All design decisions originate from tokens
2. **Semantic naming** — Token names describe purpose, not value (`--color-primary` not `--color-blue-600`)
3. **Composable variants** — Components receive variant props, never raw class strings
4. **Dark mode by default** — Build both themes from the start, not as an afterthought
5. **Document everything** — Tokens and components need inline documentation

## Resources

- [Style Dictionary](https://amzn.github.io/style-dictionary/) - Token transformation pipeline
- [CVA](https://cva.style/) - Class variance authority for variant systems
- [Radix Colors](https://www.radix-ui.com/colors) - Accessible, perceptually-uniform color system
- [Tailwind CSS](https://tailwindcss.com/docs/theme) - Theme configuration
