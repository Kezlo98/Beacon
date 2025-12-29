# Beacon UI/UX Design Plan

> No Jira. No noise. Just clarity.

## Design Philosophy

**Core Principle**: Transparency through simplicity. Every element serves a purpose.

## Style Direction

- **Primary Style**: Minimal & Direct + Swiss Modernism 2.0
- **Secondary**: Bento Grid for dashboard layouts
- **Framework**: Tailwind CSS + shadcn/ui components

## Typography

| Element | Font | Weight | Size |
|---------|------|--------|------|
| Headings | Geist Sans | 600-700 | 24-48px |
| Body | Geist Sans | 400 | 14-16px |
| Mono | Geist Mono | 400 | 13px |
| Labels | Geist Sans | 500 | 12px |

## Color System

| Role | Light Mode | Dark Mode | Usage |
|------|------------|-----------|-------|
| Background | #FFFFFF | #09090B | Page bg |
| Surface | #FAFAFA | #18181B | Cards |
| Border | #E4E4E7 | #27272A | Dividers |
| Text Primary | #09090B | #FAFAFA | Headings |
| Text Muted | #71717A | #A1A1AA | Secondary |
| **Operational** | #22C55E | #22C55E | All good |
| **Degraded** | #EAB308 | #EAB308 | Issues |
| **Outage** | #EF4444 | #EF4444 | Down |
| **Accent** | #3B82F6 | #60A5FA | Links, CTAs |

## Spacing & Grid

- Base unit: 4px
- Common: 8px, 12px, 16px, 24px, 32px, 48px
- Max content width: 1200px
- Card radius: 8px
- Button radius: 6px

## Pages Overview

### 1. Public Status (/)
- Sticky header: Logo + status badge
- Service list with status dots + uptime %
- Incident timeline (current + recent)
- 90-day uptime bars (gray/green)

### 2. Roadmap (/roadmap)
- 5-column kanban: Not Planned > Planned > In Progress > Shipped > Declined
- User submissions land in "Not Planned" column
- Feature cards: upvote, title, topic tags (max 3), comments, followers
- Submit Request button + modal form
- Filter by topic + search (⌘K)
- Sort by: most voted, newest, trending

### 3. Changelog (/changelog)
- Vertical timeline layout
- Version badge + date
- Markdown content area

### 4. Admin Dashboard (/admin)
- Sidebar nav (compact)
- Data tables for CRUD
- Modal forms
- Settings page

## Phase Files

- `phase-1-design-system.md` - Tokens, components
- `phase-2-public-pages.md` - Status, Roadmap, Changelog
- `phase-3-admin-dashboard.md` - Admin CRUD interfaces

## Deliverables

1. Design guidelines: `docs/design-guidelines.md`
2. HTML wireframes: `docs/wireframes/*.html`
3. Component specs integrated with shadcn/ui

## Accessibility

- WCAG 2.1 AA minimum
- Focus indicators on all interactive elements
- Status communicated via text, not color alone
- Keyboard navigation support
