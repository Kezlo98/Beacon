# Phase 2: Status Page

## Context
- **Parent Plan:** [plan.md](./plan.md)
- **Reference:** `docs/wireframes/roadmap-v1-soft-sage.html`
- **Depends on:** Phase 1 (design guidelines)

## Overview

| Field | Value |
|-------|-------|
| Date | 2025-12-29 |
| Priority | P1 |
| Impl Status | pending |
| Review Status | pending |

Redesign `docs/wireframes/status.html` with Soft Sage organic biophilic design.

## Key Changes

| Element | Current | New |
|---------|---------|-----|
| Font | Plus Jakarta Sans | Varela Round + Nunito Sans |
| Background | #FFFFFF | #FDFCFA (sand-50) |
| Surface | #FAFAFA | #FAF7F2 (sand-100) |
| Accent | #3B82F6 (blue) | #6B9C56 (sage-400) |
| Borders | #E4E4E7 | #E8DFD0 (sand-300) |
| Card radius | 8px | 16px (rounded-2xl) |
| Operational | #22C55E | #6B9C56 (sage) |
| Degraded | #EAB308 | #D4A574 (soft amber) |
| Outage | #EF4444 | #C97878 (muted rose) |

## Requirements

1. Update Google Fonts import to Varela Round + Nunito Sans
2. Replace :root CSS variables with Soft Sage tokens
3. Update header to match V1 roadmap style
4. Apply rounded-2xl to all cards
5. Add organic blob background gradients
6. Update status badges with breathing dots animation
7. Apply soft shadows

## Architecture

### Header Structure (from V1 roadmap)
```html
<header class="sticky top-0 z-50 bg-sand-50/90 backdrop-blur-sm border-b border-sand-200">
  <div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
    <div class="font-heading text-xl">Beacon</div>
    <nav>Status | Roadmap | Changelog</nav>
  </div>
</header>
```

### Status Badge Pattern
```html
<span class="status-badge operational">
  <span class="w-2.5 h-2.5 rounded-full bg-sage-400 pulse-soft"></span>
  All Systems Operational
</span>
```

## Related Files

| File | Action |
|------|--------|
| `docs/wireframes/status.html` | Full redesign |

## Implementation Steps

1. [ ] Read current status.html completely
2. [ ] Update `<head>`:
   - Change font imports to Varela Round + Nunito Sans
   - Update CSS variables to Soft Sage palette
   - Add pulse-soft keyframes
   - Add organic-blob background styles
3. [ ] Update `<body>` class to use sand-50 bg
4. [ ] Redesign header to match V1 roadmap
5. [ ] Update status hero section:
   - Rounded-2xl container
   - Soft shadows
   - Breathing status dot
6. [ ] Update service rows:
   - Sand backgrounds
   - Sage borders
   - Organic status colors
7. [ ] Update uptime bars colors
8. [ ] Update footer style
9. [ ] Take screenshot

## Success Criteria

- [ ] Visual consistency with V1 roadmap
- [ ] Status colors clearly distinguishable
- [ ] Breathing animation on status dots
- [ ] Organic blob backgrounds visible
- [ ] Screenshot generated

## Risk Assessment

| Risk | Impact | Mitigation |
|------|--------|------------|
| Soft status colors unclear | Medium | Use icons + text labels always |

## Security Considerations

None - static HTML wireframe.

## Next Phase

→ [Phase 3: Changelog Page](./phase-03-changelog-page.md)
