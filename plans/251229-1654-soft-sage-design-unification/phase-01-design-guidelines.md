# Phase 1: Design Guidelines

## Context
- **Parent Plan:** [plan.md](./plan.md)
- **Reference:** `docs/wireframes/roadmap-v1-soft-sage.html`

## Overview

| Field | Value |
|-------|-------|
| Date | 2025-12-29 |
| Priority | P1 (first) |
| Impl Status | pending |
| Review Status | pending |

Complete replacement of `docs/design-guidelines.md` with Soft Sage organic biophilic design system.

## Key Changes

Replace Geist/zinc palette with organic system:
- Typography: Varela Round + Nunito Sans
- Colors: Sage/Sand/Clay palette
- Components: Rounded-2xl, soft shadows
- Status: Organic colors (sage/amber/rose)
- Philosophy: "Organic biophilic - calm, natural, growth-focused"

## Requirements

1. Document typography specs (fonts, sizes, weights)
2. Define color tokens with CSS variables
3. Specify component patterns (cards, buttons, badges)
4. Detail status color system with accessibility notes
5. Include animation specs (pulse-soft)
6. Add dark mode tokens (future consideration)

## Architecture

### Color Tokens Structure
```css
:root {
  /* Sage - Primary */
  --sage-50: #F6F9F4;  --sage-100: #E8F0E4;  --sage-200: #C9DBC0;
  --sage-300: #9BBF8A; --sage-400: #6B9C56;  --sage-500: #4A7C3B;

  /* Sand - Backgrounds */
  --sand-50: #FDFCFA;  --sand-100: #FAF7F2;
  --sand-200: #F3EDE3; --sand-300: #E8DFD0;

  /* Clay - Secondary */
  --clay-400: #B8977D; --clay-500: #9C7A5C;

  /* Status - Organic */
  --status-op: #6B9C56;      --status-op-bg: #E8F0E4;
  --status-deg: #D4A574;     --status-deg-bg: #FEF3E3;
  --status-out: #C97878;     --status-out-bg: #FCE8E8;
  --status-maint: #7BA8C9;   --status-maint-bg: #E3F0F8;
}
```

## Related Files

| File | Action |
|------|--------|
| `docs/design-guidelines.md` | Complete rewrite |

## Implementation Steps

1. [ ] Read current design-guidelines.md structure
2. [ ] Write new file with Soft Sage system:
   - Design Philosophy section
   - Typography section (fonts, scale)
   - Color System section (all tokens)
   - Spacing section (keep base-4px)
   - Components section (updated specs)
   - Status Colors section (organic + accessibility)
   - Animation section (pulse-soft keyframes)
   - Dark Mode section (future tokens)
3. [ ] Verify WCAG AA contrast ratios documented

## Success Criteria

- [ ] All color tokens defined with hex values
- [ ] Typography specs complete
- [ ] Component patterns documented
- [ ] Status colors have accessibility notes
- [ ] File structure maintained for reference

## Risk Assessment

| Risk | Impact | Mitigation |
|------|--------|------------|
| Missing tokens | Medium | Cross-reference with V1 roadmap HTML |

## Security Considerations

None - documentation file only.

## Next Phase

→ [Phase 2: Status Page](./phase-02-status-page.md)
