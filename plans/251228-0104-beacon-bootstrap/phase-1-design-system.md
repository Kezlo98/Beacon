# Phase 1: Design System

## Typography Tokens

```css
--font-sans: 'Geist', system-ui, sans-serif;
--font-mono: 'Geist Mono', monospace;

--text-xs: 0.75rem;    /* 12px */
--text-sm: 0.875rem;   /* 14px */
--text-base: 1rem;     /* 16px */
--text-lg: 1.125rem;   /* 18px */
--text-xl: 1.25rem;    /* 20px */
--text-2xl: 1.5rem;    /* 24px */
--text-3xl: 2rem;      /* 32px */
--text-4xl: 2.5rem;    /* 40px */

--leading-tight: 1.25;
--leading-normal: 1.5;
--leading-relaxed: 1.625;
```

## Color Tokens

```css
/* Light Mode */
--background: 0 0% 100%;
--foreground: 240 10% 3.9%;
--card: 0 0% 98%;
--card-foreground: 240 10% 3.9%;
--muted: 240 4.8% 95.9%;
--muted-foreground: 240 3.8% 46.1%;
--border: 240 5.9% 90%;
--ring: 240 5% 64.9%;

/* Status Colors */
--status-operational: 142 71% 45%;
--status-degraded: 48 96% 47%;
--status-outage: 0 84% 60%;

/* Accent */
--accent: 217 91% 60%;
```

## Spacing Scale

```css
--space-1: 0.25rem;  /* 4px */
--space-2: 0.5rem;   /* 8px */
--space-3: 0.75rem;  /* 12px */
--space-4: 1rem;     /* 16px */
--space-5: 1.25rem;  /* 20px */
--space-6: 1.5rem;   /* 24px */
--space-8: 2rem;     /* 32px */
--space-10: 2.5rem;  /* 40px */
--space-12: 3rem;    /* 48px */
--space-16: 4rem;    /* 64px */
```

## Component Specs

### Status Badge
- Height: 24px
- Padding: 4px 8px
- Border-radius: 9999px (pill)
- Dot size: 8px with pulse animation
- Text: 12px semibold uppercase

### Service Card
- Background: var(--card)
- Padding: 16px
- Border-radius: 8px
- Border: 1px solid var(--border)
- Shadow: 0 1px 2px rgba(0,0,0,0.05)

### Uptime Bar
- Height: 32px per day segment
- Width: calculated (90 bars)
- Gap: 2px
- Border-radius: 2px
- Tooltip on hover

### Feature Card (Roadmap)
- Width: 100% of column
- Padding: 12px
- Title: 14px medium
- Description: 13px muted (2 lines max)
- Vote button: icon + count

### Timeline Item (Changelog)
- Left: date badge + connecting line
- Right: version tag + content
- Content max-width: 720px

## Shadows

```css
--shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
--shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1);
--shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1);
```

## Transitions

```css
--transition-fast: 150ms ease;
--transition-base: 200ms ease;
--transition-slow: 300ms ease;
```
