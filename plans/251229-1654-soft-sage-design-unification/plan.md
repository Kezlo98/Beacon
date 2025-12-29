---
title: "Soft Sage Design Unification"
description: "Unify all Beacon wireframes to V1 Soft Sage organic biophilic design"
status: pending
priority: P2
effort: 3h
branch: master
tags: [design, wireframes, ui]
created: 2025-12-29
---

# Soft Sage Design Unification

## Overview

Unify all Beacon wireframes (status, changelog, admin) and design guidelines to the V1 Soft Sage organic biophilic design system.

**Reference Design:** `docs/wireframes/roadmap-v1-soft-sage.html`
**Brainstorm Report:** `plans/reports/brainstorm-251229-1654-soft-sage-design-unification.md`

## Design System Summary

| Element | Value |
|---------|-------|
| Font Heading | Varela Round |
| Font Body | Nunito Sans |
| Primary Accent | Sage (#6B9C56) |
| Backgrounds | Sand (#FDFCFA, #FAF7F2) |
| Secondary | Clay (#B8977D) |
| Border Radius | 16px (rounded-2xl) |
| Animation | pulse-soft 3s |

## Phases

| # | Phase | Status | File |
|---|-------|--------|------|
| 1 | Design Guidelines | pending | [phase-01-design-guidelines.md](./phase-01-design-guidelines.md) |
| 2 | Status Page | pending | [phase-02-status-page.md](./phase-02-status-page.md) |
| 3 | Changelog Page | pending | [phase-03-changelog-page.md](./phase-03-changelog-page.md) |
| 4 | Admin Page | pending | [phase-04-admin-page.md](./phase-04-admin-page.md) |

## Files to Modify

```
docs/
├── design-guidelines.md          # Complete rewrite
└── wireframes/
    ├── status.html               # Redesign
    ├── changelog.html            # Redesign
    └── admin.html                # Redesign
```

## Success Criteria

- [ ] Visual consistency across all pages
- [ ] WCAG AA contrast maintained
- [ ] Cohesive organic feel
- [ ] Clear status communication with soft colors
- [ ] Screenshots generated for all updated pages

## Dependencies

- None (wireframes are standalone HTML files)

---
*Plan created: 2025-12-29*
