# Phase 2: Public Pages

## Status Page (/)

### Layout Structure
```
+------------------------------------------+
| Logo          [All Systems Operational]  |
+------------------------------------------+
|                                          |
|  Current Incidents                       |
|  ┌────────────────────────────────────┐  |
|  │ [!] API degraded performance       │  |
|  │     Started 2h ago - Investigating │  |
|  └────────────────────────────────────┘  |
|                                          |
|  Services                                |
|  ┌────────────────────────────────────┐  |
|  │ ● API             Operational 99.9%│  |
|  │ ● Web App         Operational 100% │  |
|  │ ● Database        Operational 99.8%│  |
|  │ ● CDN             Operational 100% │  |
|  └────────────────────────────────────┘  |
|                                          |
|  Uptime - Last 90 Days                   |
|  ▓▓▓▓▓▓▓▓▓▓░▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓  |
|  Jan 1                            Today  |
|                                          |
+------------------------------------------+
|  Powered by Beacon                       |
+------------------------------------------+
```

### Components
- **StatusHeader**: Logo + overall status badge
- **IncidentBanner**: Active incidents (collapsible)
- **ServiceList**: Services with status + uptime %
- **UptimeGraph**: 90-day bar chart
- **Footer**: Minimal branding

## Roadmap Page (/roadmap)

### Layout Structure
```
+------------------------------------------+
| Logo          Status  Roadmap  Changelog |
+------------------------------------------+
|                                          |
|  Product Roadmap                         |
|  [Filter: All ▼]  [Search...]            |
|                                          |
|  Exploring    Planned    In Progress  Shipped
|  ┌────────┐  ┌────────┐  ┌────────┐  ┌────────┐
|  │Feature │  │Feature │  │Feature │  │Feature │
|  │ desc   │  │ desc   │  │ desc   │  │ desc   │
|  │▲ 42    │  │▲ 28    │  │▲ 15    │  │✓ Done  │
|  └────────┘  └────────┘  └────────┘  └────────┘
|  ┌────────┐  ┌────────┐  ┌────────┐  ┌────────┐
|  │Feature │  │Feature │  │        │  │Feature │
|  └────────┘  └────────┘  │        │  └────────┘
|                                          |
+------------------------------------------+
```

### Components
- **RoadmapHeader**: Title + filters
- **KanbanColumn**: Status column container
- **FeatureCard**: Title, description, votes, category
- **VoteButton**: Upvote with count
- **CategoryTag**: Color-coded pill

## Changelog Page (/changelog)

### Layout Structure
```
+------------------------------------------+
| Logo          Status  Roadmap  Changelog |
+------------------------------------------+
|                                          |
|  Changelog                               |
|                                          |
|  ┌─ Dec 28, 2024 ──────────────────────┐ |
|  │                                      │ |
|  │  v1.2.0 - Feature Release            │ |
|  │  ─────────────────────────────────   │ |
|  │  ### New Features                    │ |
|  │  - Added dark mode support           │ |
|  │  - New API endpoints for webhooks    │ |
|  │                                      │ |
|  │  ### Bug Fixes                       │ |
|  │  - Fixed timezone display issue      │ |
|  │                                      │ |
|  └──────────────────────────────────────┘ |
|           │                               |
|  ┌─ Dec 15, 2024 ──────────────────────┐ |
|  │  v1.1.0 - Improvements               │ |
|  └──────────────────────────────────────┘ |
|                                          |
+------------------------------------------+
```

### Components
- **ChangelogHeader**: Title
- **TimelineEntry**: Date + version + content
- **VersionBadge**: Semver badge
- **MarkdownContent**: Rendered markdown
