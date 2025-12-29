# Beacon UI/UX Design Report

**ID**: 161cbf3c | **Date**: 2024-12-28

## Summary

Designed complete UI/UX for Beacon - transparent status and roadmap platform. Deliverables include design plan, guidelines, and HTML wireframes for all 4 pages.

## Deliverables

| File | Path | Description |
|------|------|-------------|
| Design Plan | `plans/251228-0104-beacon-bootstrap/plan.md` | Overview + color/type system |
| Phase 1 | `plans/251228-0104-beacon-bootstrap/phase-1-design-system.md` | Tokens, components |
| Phase 2 | `plans/251228-0104-beacon-bootstrap/phase-2-public-pages.md` | Public page specs |
| Phase 3 | `plans/251228-0104-beacon-bootstrap/phase-3-admin-dashboard.md` | Admin interface specs |
| Guidelines | `docs/design-guidelines.md` | Complete design system doc |
| Status wireframe | `docs/wireframes/status.html` | Public status page |
| Roadmap wireframe | `docs/wireframes/roadmap.html` | Public roadmap page |
| Changelog wireframe | `docs/wireframes/changelog.html` | Public changelog page |
| Admin wireframe | `docs/wireframes/admin.html` | Admin dashboard |

## Design Decisions

### Style Direction
- **Primary**: Minimal & Direct + Swiss Modernism 2.0
- **Rationale**: Aligns with "No noise. Just clarity" philosophy
- **Performance**: Excellent (no heavy animations)
- **Accessibility**: WCAG AA compliant

### Typography
- **Font**: Plus Jakarta Sans (Geist fallback specified)
- **Rationale**: Modern, professional, excellent readability
- **Weights**: 400/500/600/700 for clear hierarchy

### Color System
- Status colors from requirements: Green (#22C55E), Yellow (#EAB308), Red (#EF4444)
- Neutral backgrounds: White (#FFFFFF), Surface (#FAFAFA)
- Accent blue (#3B82F6) for links and CTAs
- All pairs meet 4.5:1 contrast ratio

### Layout
- Max width 800px for public pages (optimal reading)
- Max width 1200px for roadmap (kanban needs space)
- Sidebar 240px for admin (standard pattern)
- 8px base grid, 8px border-radius on cards

### Components
- Status badge with pulse animation
- Service row with status dot + uptime %
- 90-day uptime bar graph
- Feature cards with vote button
- Timeline layout for changelog
- Data tables for admin CRUD

## Technical Notes

### shadcn/ui Integration
Wireframes use custom CSS matching shadcn/ui patterns:
- Same color token naming convention
- Same border-radius values
- Same shadow values
- Easy migration to actual components

### Responsive Strategy
- Mobile-first CSS in wireframes
- Breakpoints: 640px, 768px, 1024px, 1280px
- Kanban stacks to 2-col then 1-col on mobile
- Admin sidebar collapses on mobile (not shown in wireframe)

### Accessibility
- Focus states on all interactive elements
- Status communicated via text + color + icon
- Touch targets 44px minimum
- Reduced motion support via CSS

## Open Questions

1. **Geist font licensing**: Confirm Vercel font license allows use, else stick with Plus Jakarta Sans
2. **Dark mode priority**: Design tokens ready, implementation scope TBD
3. **Roadmap voting auth**: Anonymous or require sign-in?
4. **Mobile admin**: Full admin or simplified mobile view?
