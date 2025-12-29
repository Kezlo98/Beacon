# Phase 4: Admin Page

## Context
- **Parent Plan:** [plan.md](./plan.md)
- **Reference:** `docs/wireframes/roadmap-v1-soft-sage.html`
- **Depends on:** Phases 1-3

## Overview

| Field | Value |
|-------|-------|
| Date | 2025-12-29 |
| Priority | P2 |
| Impl Status | pending |
| Review Status | pending |

Redesign `docs/wireframes/admin.html` with Soft Sage organic biophilic design while maintaining functional clarity.

## Key Changes

| Element | Current | New |
|---------|---------|-----|
| Font | Plus Jakarta Sans | Varela Round + Nunito Sans |
| Sidebar bg | #FFFFFF | #FAF7F2 (sand-100) |
| Main bg | #FAFAFA | #FDFCFA (sand-50) |
| Accent | #3B82F6 (blue) | #6B9C56 (sage-400) |
| Nav radius | 6px | 12px (rounded-xl) |
| Card radius | 8px | 16px (rounded-2xl) |

## Requirements

1. Apply Soft Sage base styles
2. Update sidebar:
   - Sand-100 background
   - Rounded-xl nav items
   - Sage active states
3. Keep functional layouts clear
4. Softer form inputs (rounded-full where appropriate)
5. Update buttons to Soft Sage style
6. Status indicators use organic colors

## Architecture

### Sidebar Nav Item Pattern
```html
<a class="nav-item active">
  <!-- Sand bg, sage text when active -->
  <span class="font-heading">Services</span>
</a>
```

### Form Input Pattern
```html
<input class="w-full bg-white border border-sand-300 rounded-xl px-4 py-2
             focus:outline-none focus:ring-2 focus:ring-sage-200" />
```

### Button Pattern
```html
<!-- Primary -->
<button class="bg-sage-400 hover:bg-sage-500 text-white rounded-full px-5 py-2">
  Save
</button>
<!-- Secondary -->
<button class="bg-sand-200 hover:bg-sand-300 text-clay-500 rounded-full px-5 py-2">
  Cancel
</button>
```

## Related Files

| File | Action |
|------|--------|
| `docs/wireframes/admin.html` | Full redesign |

## Implementation Steps

1. [ ] Read current admin.html completely
2. [ ] Update `<head>` same as other pages
3. [ ] Update sidebar:
   - Sand-100 background
   - Rounded-xl nav items
   - Sage accents
4. [ ] Update main content area:
   - Sand-50 background
   - Rounded-2xl cards
5. [ ] Update form elements:
   - Rounded inputs
   - Sage focus rings
6. [ ] Update buttons to Soft Sage style
7. [ ] Update status indicators
8. [ ] Update tables/data displays
9. [ ] Take screenshot

## Success Criteria

- [ ] Consistent with public pages
- [ ] Functional clarity maintained
- [ ] Forms clearly visible
- [ ] Actions easy to identify
- [ ] Screenshot generated

## Risk Assessment

| Risk | Impact | Mitigation |
|------|--------|------------|
| Admin clarity reduced | Medium | Keep layouts functional, only update surfaces |
| Form inputs too soft | Low | Ensure good border contrast |

## Security Considerations

None - static HTML wireframe.

## Completion

After this phase:
- All wireframes unified
- Design guidelines documented
- Screenshots for all pages
