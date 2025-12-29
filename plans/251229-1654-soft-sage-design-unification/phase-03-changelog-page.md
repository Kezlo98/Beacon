# Phase 3: Changelog Page

## Context
- **Parent Plan:** [plan.md](./plan.md)
- **Reference:** `docs/wireframes/roadmap-v1-soft-sage.html`
- **Depends on:** Phase 1, Phase 2

## Overview

| Field | Value |
|-------|-------|
| Date | 2025-12-29 |
| Priority | P2 |
| Impl Status | pending |
| Review Status | pending |

Redesign `docs/wireframes/changelog.html` with Soft Sage organic biophilic design.

## Key Changes

| Element | Current | New |
|---------|---------|-----|
| Font | Plus Jakarta Sans | Varela Round + Nunito Sans |
| Background | #FFFFFF | #FDFCFA (sand-50) |
| Accent | #3B82F6 (blue) | #6B9C56 (sage-400) |
| Borders | #E4E4E7 | #E8DFD0 (sand-300) |
| Version badges | Blue pills | Sage pills |
| Timeline dots | Standard | Breathing sage dots |

## Requirements

1. Apply same base styles as status page
2. Update version badges to sage pills
3. Release type tags:
   - Feature → sage-100/sage-500
   - Fix → clay-100/clay-500
   - Improvement → soft blue
4. Timeline with organic dots
5. Entry cards with rounded-2xl

## Architecture

### Version Badge Pattern
```html
<span class="text-xs bg-sage-100 text-sage-500 px-2 py-0.5 rounded-full font-medium">
  v2.1.0
</span>
```

### Release Type Tags
```html
<!-- Feature -->
<span class="text-xs bg-sage-100 text-sage-500 px-2 py-0.5 rounded-full">Feature</span>
<!-- Fix -->
<span class="text-xs bg-sand-200 text-clay-500 px-2 py-0.5 rounded-full">Fix</span>
```

## Related Files

| File | Action |
|------|--------|
| `docs/wireframes/changelog.html` | Full redesign |

## Implementation Steps

1. [ ] Read current changelog.html completely
2. [ ] Update `<head>` same as status page
3. [ ] Update body/header styling
4. [ ] Redesign changelog entries:
   - Rounded-2xl cards
   - Sage version badges
   - Organic release type tags
   - Timeline with breathing dots
5. [ ] Update footer
6. [ ] Take screenshot

## Success Criteria

- [ ] Matches Soft Sage system
- [ ] Version badges clearly visible
- [ ] Release types distinguishable
- [ ] Timeline has organic feel
- [ ] Screenshot generated

## Risk Assessment

| Risk | Impact | Mitigation |
|------|--------|------------|
| Timeline dates unclear | Low | Keep clear date formatting |

## Security Considerations

None - static HTML wireframe.

## Next Phase

→ [Phase 4: Admin Page](./phase-04-admin-page.md)
