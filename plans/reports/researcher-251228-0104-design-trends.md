# Design Research: Status Page & Roadmap Trends 2024-2025

## 1. Visual Design Trends
- **High-Density Minimalism**: Moving away from card-heavy layouts to "borderless" or subtle-border designs (e.g., Linear, Vercel). Focus on information hierarchy through whitespace rather than boxes.
- **Glassmorphism & Depth**: Subtle use of backdrop blurs on sticky navigation and notification banners.
- **Micro-interactivity**: Hover states that reveal metadata or provide smooth transitions (Spring animations > Linear transitions).

## 2. Typography & Color
### Typography Alternatives (Avoiding Inter/Poppins)
- **Geist (Vercel)**: Ultra-modern, mono-spaced influences, optimized for legibility in technical UIs. Highly recommended for Beacon.
- **Plus Jakarta Sans**: Grotesque style with a friendly, modern feel. Great for roadmaps.
- **Satoshi**: Geometric sans with variable weights, very clean and "premium" tech feel.
- **Commit Mono**: For technical status details or incident logs to provide a "system" feel.

### Color Systems (Achromatic + Semantic)
- **Backgrounds**: Deep charcoal (`#0A0A0A`) or soft gray (`#FAFAFA`) instead of pure black/white.
- **Operational (Green)**: Emerald/Teal shifts (`#10B981` / `#059669`). Pulsing "Live" indicator.
- **Degraded (Yellow)**: Amber/Gold (`#F59E0B`). Avoid neon yellows.
- **Outage (Red)**: Rose/Crimson (`#E11D48`). Softening the red to be less "alarming" but clearly critical.

## 3. UI Element Patterns
### Status Indicators
- **The "Blinking Dot"**: Small 8px dot with a subtle outer glow (box-shadow) to indicate live status.
- **Component Grids**: Minimal list items with a "sparkline" showing 90-day uptime instead of just a current status badge.

### Timeline & Changelog (Linear-style)
- **Vertical Line Trace**: A thin (`1px`) vertical line connecting dated entries.
- **Date Sticky Headers**: Dates that stick to the top left as the user scrolls.
- **Media Integration**: Large-radius rounded corners (`12px-16px`) for screenshots/videos within changelogs.

### Roadmap Cards
- **Status Tags**: Small, pill-shaped badges (e.g., "Planned", "In Progress", "Completed") with low-opacity backgrounds.
- **Priority Pips**: Subtle indicators (dots or bars) for item importance.
- **Quarterly Grouping**: Layouts organized by "Q1", "Q2" rather than specific dates to manage expectations.

## 4. Specific Recommendations for Beacon
- **Primary Font**: Geist Sans for UI, Geist Mono for incident IDs/logs.
- **Spacing Scale**: 4px base (8, 12, 16, 24, 32, 48, 64) for consistent rhythm.
- **Radii**: 8px for small elements (badges, buttons), 12px for cards/modals.
- **Contrast**: Use text-secondary (`#666666`) for timestamps and metadata to reduce visual noise.

## 5. Inspiration References
- **Linear Changelog**: For the vertical timeline and clean typography.
- **Vercel Status**: For the "system-wide" overview grid and Geist integration.
- **Stripe Status**: For high-clarity incident reporting and professional color palette.
- **GitHub Status**: For simple, no-nonsense incident history.

## Unresolved Questions
- Should the roadmap include user voting/reactions (like Canny) or remain read-only?
- Will the status page support "Dark Mode" by default or follow system preferences?
