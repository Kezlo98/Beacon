# Brainstorm: Soft Sage Design Unification

## Problem Statement
User chose V1 Soft Sage design for Beacon. Need to unify all public pages and admin to same organic biophilic aesthetic. Current design-guidelines.md uses Geist/zinc palette - requires complete replacement.

## Scope Confirmed
| Page | Action |
|------|--------|
| status.html | Redesign |
| changelog.html | Redesign |
| admin.html | Redesign |
| design-guidelines.md | Replace |
| roadmap variants (v2-v5) | Archive/keep as reference |

## Design System: Soft Sage

### Typography
```css
--font-heading: 'Varela Round', sans-serif;
--font-body: 'Nunito Sans', sans-serif;
```

### Color Palette
```css
/* Sage - Primary accent */
sage-50: #F6F9F4   sage-100: #E8F0E4   sage-200: #C9DBC0
sage-300: #9BBF8A  sage-400: #6B9C56   sage-500: #4A7C3B

/* Sand - Backgrounds */
sand-50: #FDFCFA   sand-100: #FAF7F2   sand-200: #F3EDE3
sand-300: #E8DFD0

/* Clay - Secondary accent */
clay-400: #B8977D  clay-500: #9C7A5C
```

### Organic Status Colors
| Status | Color | Hex | Notes |
|--------|-------|-----|-------|
| Operational | Sage | #6B9C56 | Calming growth |
| Degraded | Soft Amber | #D4A574 | Warm warning |
| Outage | Muted Rose | #C97878 | Not aggressive |
| Maintenance | Soft Blue | #7BA8C9 | Neutral info |

### Components
- Border radius: 16px (rounded-2xl)
- Shadows: Soft, minimal (shadow-sm)
- Animation: pulse-soft (3s ease-in-out infinite)
- Backgrounds: Organic gradient blobs

## Changes Summary

### 1. status.html
- Replace Plus Jakarta Sans → Varela Round + Nunito Sans
- Background: #FFFFFF → sand-50
- Status colors: Standard → Organic palette
- Cards: rounded-lg → rounded-2xl
- Add organic blob background gradients
- Update status badges to pill style with breathing dots

### 2. changelog.html
- Same font/color updates
- Timeline style: Keep vertical but soften edges
- Version badges: Use sage pills
- Release type tags: Sage (feature), Clay (fix), Soft blue (improvement)

### 3. admin.html
- Apply same visual system
- Keep functional layouts
- Softer form inputs with rounded-full
- Navigation matches public header style

### 4. design-guidelines.md
Replace entirely with:
- Philosophy: "Organic biophilic design - calm, natural, growth-focused"
- Typography: Varela Round + Nunito Sans specs
- Color system: Sage/Sand/Clay tokens
- Component specs: Soft Sage variants
- Status patterns: Organic colors with accessible contrast
- Animation: pulse-soft keyframes
- Accessibility: Maintain WCAG AA with softer palette

## Risks & Considerations

| Risk | Mitigation |
|------|------------|
| Softer status colors may reduce urgency perception | Pair with clear icons + text labels |
| Varela Round limited weights | Use for headings only, Nunito for body |
| Organic blobs may affect performance | Use CSS gradients, not images |
| Admin needs functional clarity | Keep layouts clear, just update surface styling |

## Implementation Order
1. Update design-guidelines.md first (single source of truth)
2. Status page (most critical user-facing)
3. Changelog page
4. Admin page

## Success Criteria
- Visual consistency across all pages
- WCAG AA contrast maintained
- Cohesive organic feel
- Clear status communication despite softer colors

## Next Steps
- [ ] Create implementation plan with file-by-file changes
- [ ] Generate screenshots of updated wireframes
- [ ] Review accessibility of organic status colors

---
*Report generated: 2025-12-29*
