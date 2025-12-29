# Beacon Tech Stack

> No Jira. No noise. Just clarity.

## Core Stack

| Layer | Choice | Rationale |
|-------|--------|-----------|
| **Framework** | Next.js 15 (App Router) | SSR/SSG for SEO, React Server Components, TypeScript |
| **Database** | SQLite + Drizzle ORM | Zero config, single file, easy backup, self-host friendly |
| **Styling** | Tailwind CSS + shadcn/ui | Utility-first, copy-paste components, no runtime |
| **Auth** | Better Auth | Simple, self-hosted, supports multiple providers |
| **Deployment** | Docker | Single container, works anywhere |

## Why This Stack

### SQLite over Postgres
- Single file = trivial backup (`cp beacon.db backup.db`)
- No separate database server
- Sufficient for 99% of status page traffic
- Drizzle makes migration to Postgres easy if needed

### Next.js 15 App Router
- Server Components reduce client JS bundle
- Built-in API routes (no separate backend)
- Static generation for public pages (fast, SEO)
- Server Actions for mutations

### Better Auth over NextAuth
- Simpler API, better DX
- Built-in admin/user roles
- Easy credential-based auth for single-admin setups

## Project Structure

```
beacon/
├── src/
│   ├── app/              # Next.js App Router
│   │   ├── (public)/     # Public status pages (SSG)
│   │   ├── (admin)/      # Admin dashboard (protected)
│   │   └── api/          # API routes
│   ├── components/       # UI components (shadcn/ui)
│   ├── db/               # Drizzle schema + migrations
│   └── lib/              # Utilities, auth config
├── public/               # Static assets
├── drizzle.config.ts
├── docker-compose.yml
└── Dockerfile
```

## Key Dependencies

```json
{
  "next": "^15.0.0",
  "react": "^19.0.0",
  "drizzle-orm": "^0.38.0",
  "better-sqlite3": "^11.0.0",
  "better-auth": "^1.0.0",
  "tailwindcss": "^4.0.0"
}
```

## Deployment Options

1. **Docker (recommended)**: Single container, volume for SQLite
2. **Vercel**: Works but needs external DB (Turso for SQLite-compat)
3. **VPS**: Node.js + PM2, simplest self-host

## Real-time Strategy

- **Polling** for MVP (simple, works everywhere)
- **Server-Sent Events** for v2 (native browser support, no WebSocket overhead)

## Design Decisions

| Decision | Choice | Alternative Considered |
|----------|--------|----------------------|
| ORM | Drizzle | Prisma (heavier, slower cold starts) |
| Components | shadcn/ui | Radix directly (more work) |
| State | React Server Components | Redux/Zustand (unnecessary complexity) |
| Forms | React Hook Form + Zod | Native forms (less validation) |

## Scaling Path

SQLite handles ~100k daily visitors easily. When needed:
1. Switch to Turso (distributed SQLite) - minimal code changes
2. Or migrate to Postgres via Drizzle - schema stays same

---

*Stack optimized for: solo developers, small teams, self-hosters*
