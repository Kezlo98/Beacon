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
+----------------------------------------------------------+
| Logo             Status  Roadmap  Changelog              |
+----------------------------------------------------------+
|                                                          |
|  Product Roadmap                    [+ Submit Request]   |
|  [Filter: All ▼]  [Search... ⌘K]                         |
|                                                          |
|  Not Planned   Planned    In Progress   Shipped   Declined
|  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐
|  │▲ 42      │ │▲ 28      │ │▲ 15      │ │✓ Done    │ │✗ Closed  │
|  │Dark mode │ │API v2    │ │Webhooks  │ │SSO       │ │Feature X │
|  │#UI #UX   │ │#API      │ │#API      │ │#Auth     │ │#Scope    │
|  │💬 8  👁 12│ │💬 5  👁 8 │ │💬 3  👁 6 │ │💬 15     │ │💬 2      │
|  └──────────┘ └──────────┘ └──────────┘ └──────────┘ └──────────┘
|  ┌──────────┐ ┌──────────┐
|  │▲ 31      │ │▲ 22      │
|  │Export CSV│ │Mobile app│
|  └──────────┘ └──────────┘
|                                                          |
+----------------------------------------------------------+
```

### Columns (5)
| Column | Description | Color |
|--------|-------------|-------|
| Not Planned | User submissions, under consideration | Gray |
| Planned | Accepted, scheduled for development | Blue |
| In Progress | Currently being built | Yellow |
| Shipped | Completed and released | Green |
| Declined | Not moving forward (with reason) | Red muted |

### Request Submission Flow
1. User clicks "Submit Request" button
2. Modal form opens:
   - Title (required, max 100 chars)
   - Description (optional, max 500 chars)
   - Topics (select up to 3)
3. Request appears in "Not Planned" column
4. Users can upvote and comment
5. Admin moves to appropriate column

### Feature Card Layout
```
┌─────────────────────────────────┐
│  ▲  42    Dark mode support     │  ← Upvote button + count + title
│           #UI  #Enhancement     │  ← Topic tags (max 3)
│           💬 8   👁 12          │  ← Comments + followers
└─────────────────────────────────┘
```

### Components
- **RoadmapHeader**: Title + Submit button + filters
- **KanbanColumn**: Status column container (5 columns)
- **FeatureCard**: Vote count, title, tags, comments, followers
- **VoteButton**: Upvote only with count
- **TopicTag**: Color-coded pill with emoji
- **SubmitModal**: Form for new requests
- **FeatureDetailModal**: Full view with comments
- **SearchInput**: Quick search with ⌘K shortcut

### Interactions
- **Upvote**: Click to vote (toggle, 1 vote per user)
- **Follow**: Subscribe to status updates
- **Comment**: Add discussion on feature detail view
- **Filter**: By topic, status, or search term
- **Sort**: Most voted, newest, trending

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
