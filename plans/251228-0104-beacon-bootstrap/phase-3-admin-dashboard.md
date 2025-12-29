# Phase 3: Admin Dashboard

## Layout Structure

```
+------------------------------------------+
| ☰ Beacon Admin              [User ▼]     |
+------+-----------------------------------+
|      |                                   |
| Nav  |  Page Content                     |
|      |                                   |
| ○ Dashboard                              |
| ○ Services                               |
| ○ Incidents                              |
| ○ Roadmap                                |
| ○ Changelog                              |
| ○ Settings                               |
|      |                                   |
+------+-----------------------------------+
```

## Sidebar Navigation
- Width: 240px (desktop), collapsed on mobile
- Active state: background highlight
- Icons + labels

## Dashboard (/admin)

Overview cards:
- Total services / operational count
- Active incidents
- Uptime % (30 days)
- Recent activity feed

## Services (/admin/services)

```
+-------------------------------------------+
| Services                    [+ Add Service]|
+-------------------------------------------+
| Name        | Status      | Uptime  | Act |
|-------------|-------------|---------|-----|
| API         | Operational | 99.9%   | ... |
| Web App     | Operational | 100%    | ... |
| Database    | Degraded    | 99.5%   | ... |
+-------------------------------------------+
```

Actions dropdown: Edit, Delete

## Incidents (/admin/incidents)

```
+-------------------------------------------+
| Incidents                 [+ New Incident] |
+-------------------------------------------+
| Service | Title          | Status   | Date |
|---------|----------------|----------|------|
| API     | Slow responses | Resolved | 2h   |
| DB      | Connection err | Active   | 1d   |
+-------------------------------------------+
```

Incident statuses: Investigating, Identified, Monitoring, Resolved

## Roadmap Items (/admin/roadmap)

```
+-------------------------------------------+
| Roadmap Items               [+ Add Item]   |
+-------------------------------------------+
| Title      | Status     | Votes | Category|
|------------|------------|-------|---------|
| Dark mode  | Shipped    | 142   | Feature |
| API v2     | In Progress| 89    | API     |
+-------------------------------------------+
```

Status: Exploring, Planned, In Progress, Shipped

## Changelog Entries (/admin/changelog)

```
+-------------------------------------------+
| Changelog                   [+ New Entry]  |
+-------------------------------------------+
| Version | Title          | Date           |
|---------|----------------|----------------|
| v1.2.0  | Feature Release| Dec 28, 2024   |
| v1.1.0  | Improvements   | Dec 15, 2024   |
+-------------------------------------------+
```

Editor: Markdown with preview

## Settings (/admin/settings)

Sections:
- **General**: Site name, description, logo
- **Appearance**: Theme, colors
- **Notifications**: Email, webhooks
- **API**: API keys, rate limits

## Modal Forms

Standard form layout:
- Max width: 500px
- Padding: 24px
- Label above input
- Validation inline
- Actions: Cancel (ghost), Save (primary)

## Data Tables

Using shadcn/ui table component:
- Sticky header
- Row hover state
- Pagination
- Bulk actions (optional)
