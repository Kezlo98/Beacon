# Research Report: Modern Tech Stack for Status Page Application

## Executive Summary
This report evaluates modern web frameworks and tools for building **Beacon**, an open-source, self-hostable status page and roadmap platform. The goal is to select a stack that balances developer velocity, performance (SEO/SSG), and ease of self-hosting.

**Recommendation**: **Next.js 15 (App Router)** + **Tailwind CSS/shadcn/ui** + **SQLite** + **Drizzle ORM**.

## Research Methodology
- **Sources consulted**: GitHub (OpenStatus, Kener, StatusNook), Official Docs (Next.js, Astro, Prisma, Drizzle), Benchmarks.
- **Date range**: late 2024 to late 2025.
- **Key search terms**: Next.js 15 vs Astro 5, self-hosted status page stack, SQLite ORM comparison 2025.

## Key Findings

### 1. Frontend Frameworks
- **Next.js 15**: Strongest ecosystem. Server Components (RSC) reduce client-side JS. Excellent for full-stack apps with built-in API routes.
- **Astro**: Best for pure speed and static sites. Excellent for the public status page, but slightly more complex for the admin dashboard compared to Next.js.
- **SvelteKit**: High developer satisfaction and performance. Used by `kener`.
- **Remix**: Strong focus on web standards and SSR. Now largely integrated into React Router 7.

### 2. Full-Stack Considerations
- **SSR/SSG**: Critical for status pages. Public pages should be SSG with Incremental Static Regeneration (ISR) or fast SSR. Next.js excels here.
- **Real-time**: Can be achieved via Server-Sent Events (SSE) or simple polling for status updates. Websockets are often overkill for status pages.
- **Self-Hosting**: Docker is the standard. Next.js `output: 'standalone'` is efficient for self-hosting.

### 3. Styling Options
- **Tailwind CSS**: Industry standard.
- **shadcn/ui**: Built on **Radix UI**. Provides accessible, copy-pasteable components. Perfect for rapid development of both public pages and admin dashboards.

### 4. Database & ORM
- **SQLite**: Best for self-hosting. One file, no separate DB server required. High performance for status page workloads (high read/write ratio).
- **Postgres**: Better for large-scale multi-tenant SaaS, but adds complexity for self-hosters.
- **Drizzle ORM**: Leaner, faster, and "closer to SQL" than Prisma. Superior support for SQLite/Bun and smaller bundle sizes.
- **Prisma**: Easier DX for beginners but heavier runtime/engine.

## Comparative Analysis

| Feature | Next.js 15 | Astro | SvelteKit |
|---------|------------|-------|-----------|
| **SSG/SSR** | Excellent | Best | Excellent |
| **Admin UI** | Native | Islands | Native |
| **Ecosystem**| Massive | Growing | Moderate |
| **Learning** | Moderate | Easy | Easy |

## Implementation Recommendations

### Recommended Stack: "The Simple Powerhouse"
- **Framework**: Next.js 15 (App Router, React 19)
- **Language**: TypeScript
- **Styling**: Tailwind CSS + shadcn/ui (Radix UI)
- **Database**: SQLite (via `better-sqlite3` or `libsql`)
- **ORM**: Drizzle ORM
- **Auth**: NextAuth.js (Auth.js v5) or Better Auth
- **Deployment**: Docker (Standalone mode)

### Code Example (Drizzle + SQLite Schema)
```typescript
import { sqliteTable, text, integer } from "drizzle-orm/sqlite-core";

export const services = sqliteTable("services", {
  id: text("id").primaryKey(),
  name: text("name").notNull(),
  status: text("status", { enum: ["operational", "degraded", "outage"] }).default("operational"),
  updatedAt: integer("updated_at", { mode: "timestamp" }),
});
```

## Common Pitfalls
- **Over-engineering**: Avoid Microservices or heavy Message Brokers.
- **Cold Starts**: If self-hosting on low-spec VPS, avoid heavy Docker images. Use Alpine-based builds.
- **Database Locking**: SQLite handles concurrent reads well but writes can block. Ensure WAL (Write-Ahead Logging) mode is enabled.

## Unresolved Questions
1. Should we support Postgres as an optional backend from day one?
2. Is Bun a viable runtime for the target self-hosting audience?
