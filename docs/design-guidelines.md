# Beacon Design Guidelines

> No Jira. No noise. Just clarity.

## Design Philosophy

Beacon's design embodies **transparency through simplicity**. Every visual element serves a clear purpose. We prioritize clarity over decoration, function over flourish.

---

## Typography

### Font Family
```css
--font-sans: 'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'Geist Mono', 'SF Mono', 'Fira Code', monospace;
```

**Fallback**: Plus Jakarta Sans if Geist unavailable.

### Type Scale

| Name | Size | Line Height | Weight | Usage |
|------|------|-------------|--------|-------|
| `text-xs` | 12px | 1.5 | 400-500 | Labels, captions |
| `text-sm` | 14px | 1.5 | 400-500 | Body small, table cells |
| `text-base` | 16px | 1.5 | 400 | Body text |
| `text-lg` | 18px | 1.4 | 500 | Lead paragraphs |
| `text-xl` | 20px | 1.3 | 600 | Section headers |
| `text-2xl` | 24px | 1.25 | 600 | Page titles |
| `text-3xl` | 32px | 1.2 | 700 | Hero headlines |
| `text-4xl` | 40px | 1.1 | 700 | Large display |

---

## Color System

### Semantic Colors

```css
/* Backgrounds */
--background: #FFFFFF;        /* Page background */
--surface: #FAFAFA;           /* Cards, panels */
--surface-hover: #F4F4F5;     /* Hover states */

/* Text */
--text-primary: #09090B;      /* Headings, important */
--text-secondary: #3F3F46;    /* Body text */
--text-muted: #71717A;        /* Secondary info */
--text-placeholder: #A1A1AA;  /* Input placeholders */

/* Borders */
--border: #E4E4E7;            /* Default borders */
--border-strong: #D4D4D8;     /* Emphasized borders */

/* Interactive */
--accent: #3B82F6;            /* Links, primary actions */
--accent-hover: #2563EB;      /* Hover state */
--ring: #93C5FD;              /* Focus rings */
```

### Status Colors

| Status | Color | Hex | Usage |
|--------|-------|-----|-------|
| Operational | Green | `#22C55E` | All systems working |
| Degraded | Yellow | `#EAB308` | Partial outage |
| Outage | Red | `#EF4444` | System down |
| Maintenance | Blue | `#3B82F6` | Scheduled maintenance |

### Status with Backgrounds

```css
/* Operational */
--status-op-bg: #DCFCE7;
--status-op-text: #166534;
--status-op-dot: #22C55E;

/* Degraded */
--status-deg-bg: #FEF9C3;
--status-deg-text: #854D0E;
--status-deg-dot: #EAB308;

/* Outage */
--status-out-bg: #FEE2E2;
--status-out-text: #991B1B;
--status-out-dot: #EF4444;
```

---

## Spacing

Base unit: 4px. Use multiples for consistency.

| Token | Value | Common Use |
|-------|-------|------------|
| `space-1` | 4px | Tight gaps |
| `space-2` | 8px | Icon spacing, inline gaps |
| `space-3` | 12px | Button padding |
| `space-4` | 16px | Card padding, section gaps |
| `space-6` | 24px | Content sections |
| `space-8` | 32px | Major sections |
| `space-12` | 48px | Page sections |
| `space-16` | 64px | Page margins |

---

## Layout

### Grid
- Max content width: 1200px
- Padding: 16px (mobile), 24px (tablet), 32px (desktop)
- 12-column grid for complex layouts

### Breakpoints
```css
--breakpoint-sm: 640px;
--breakpoint-md: 768px;
--breakpoint-lg: 1024px;
--breakpoint-xl: 1280px;
```

---

## Components

### Cards
```css
.card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 16px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
}
```

### Buttons

| Variant | Background | Text | Border |
|---------|------------|------|--------|
| Primary | `#09090B` | `#FAFAFA` | none |
| Secondary | `#FAFAFA` | `#09090B` | `#E4E4E7` |
| Ghost | transparent | `#3F3F46` | none |
| Destructive | `#EF4444` | `#FFFFFF` | none |

Button sizes:
- Small: h-8, px-3, text-xs
- Default: h-10, px-4, text-sm
- Large: h-12, px-6, text-base

Border-radius: 6px

### Status Badge
```css
.status-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 4px 10px;
  border-radius: 9999px;
  font-size: 12px;
  font-weight: 500;
}

.status-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  animation: pulse 2s infinite;
}
```

### Service Row
```css
.service-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 16px;
  border-bottom: 1px solid var(--border);
}
```

### Uptime Bar
- 90 bars representing days
- Height: 32px
- Width: 3px per bar
- Gap: 2px
- Green for 100%, yellow for degraded, red for outage
- Gray for no data

### Feature Card (Roadmap)
```css
.feature-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 12px;
}

.feature-title {
  font-size: 14px;
  font-weight: 500;
  margin-bottom: 4px;
}

.feature-description {
  font-size: 13px;
  color: var(--text-muted);
  display: -webkit-box;
  -webkit-line-clamp: 2;
  overflow: hidden;
}
```

---

## Shadows

```css
--shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
--shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
--shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
--shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
```

---

## Animation

### Timing
```css
--duration-fast: 150ms;
--duration-base: 200ms;
--duration-slow: 300ms;
--easing: cubic-bezier(0.4, 0, 0.2, 1);
```

### Status Pulse
```css
@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}
```

### Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## Accessibility

### Color Contrast
- All text meets WCAG 2.1 AA (4.5:1 minimum)
- Status colors paired with icons/text, never color alone
- Focus states visible (2px ring)

### Interactive Elements
- Minimum touch target: 44x44px
- Focus indicators on all interactive elements
- Skip links for keyboard navigation

### Status Communication
Always pair colors with:
- Text labels ("Operational", "Outage")
- Icons (checkmark, warning, x)

---

## Icons

Use Lucide icons for consistency with shadcn/ui.

Common icons:
- `check-circle` - Operational
- `alert-triangle` - Degraded
- `x-circle` - Outage
- `clock` - Maintenance
- `chevron-up` - Vote
- `plus` - Add
- `pencil` - Edit
- `trash-2` - Delete

Size: 16px (inline), 20px (buttons), 24px (standalone)

---

## Dark Mode (Future)

Swap color tokens:
```css
[data-theme="dark"] {
  --background: #09090B;
  --surface: #18181B;
  --text-primary: #FAFAFA;
  --text-secondary: #D4D4D8;
  --text-muted: #A1A1AA;
  --border: #27272A;
}
```

---

## Component Library

Use shadcn/ui components:
- Button, Input, Textarea, Select
- Card, Badge, Avatar
- Table, Dialog, Sheet
- Dropdown Menu, Tabs
- Toast, Alert

Customize with CSS variables above.

---

*Last updated: 2024-12-28*
