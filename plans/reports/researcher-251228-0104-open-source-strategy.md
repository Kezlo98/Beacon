# Research Report: Open Source Status Platform Strategy
Date: 251228
Author: Researcher Agent

## 1. Open Source Strategy

### Licensing Options
- **MIT/Apache 2.0**: Preferred for maximum adoption (e.g., **Upptime**, **Gatus**). High permissiveness encourages corporate integration but risks "open core" commercialization by others without upstreaming.
- **AGPL-3.0**: Common for self-hosted SaaS competitors (e.g., **Uptime Kuma** uses MIT, but many newer self-hosted tools pivot to AGPL). Protects against cloud providers "wrapping" the tool as a service without contributing back.
- **Decision Matrix**:
    - *MIT*: For building a foundational library or widely adopted utility.
    - *AGPL*: For a standalone application where protecting the "service" aspect is critical.

### Community Building
- **GitHub Discussions**: Essential for off-loading issues from bug tracking to user support.
- **Hacktoberfest**: Successful pattern for status pages (e.g., Cachet) to gain initial UI/localization contributions.
- **Sponsorships**: Visible "Sponsor" buttons and Open Collective integration for sustainability.

## 2. Self-Hosting Requirements

### Deployment Simplicity
- **Docker/Compose**: Non-negotiable standard. One-click deployments via templates (CapRover, Umbrel) drive adoption.
- **Statelessness**: Favoring architectures that store config in yaml/env and persistent data in a single volume.

### Database Strategy
- **SQLite**: Best for "Minimal dependencies philosophy" and low-traffic sites.
- **Postgres/MySQL**: Required for high-availability or multi-node scaling.
- **Pattern**: Support SQLite by default (file-based) with an easy ENV switch for Postgres (e.g., **Gatus**, **Cachet**).

### Repository-as-Database (Experimental)
- **Upptime**: Uses GitHub Actions + GitHub Pages + Git repo as the database. Zero hosting cost, high resilience, but locked to GitHub ecosystem.

## 3. Extensibility

### Plugin/Integration Architecture
- **Hook-based System**: Uptime Kuma's "Notification Providers" pattern is the gold standard (90+ services).
- **Embedded Webview/Custom CSS**: Crucial for status pages to match corporate branding.

### API-First Design
- **REST vs WebSocket**: REST API is essential for external monitoring agents. WebSockets (Uptime Kuma) provide superior real-time dashboards but can be harder to integrate with external CLI tools.
- **Swagger/OpenAPI**: Auto-generated docs are expected for "API-first" claims.

### Webhook Patterns
- **Inbound**: To receive heartbeats from "dead man switches" (cron jobs).
- **Outbound**: To trigger external automation (incident response, CI/CD rollbacks).

## Sources
- [Uptime Kuma GitHub](https://github.com/louislam/uptime-kuma)
- [Gatus GitHub](https://github.com/TwiN/gatus)
- [Upptime GitHub](https://github.com/upptime/upptime)
- [Cachet GitHub](https://github.com/CachetHQ/Cachet)

## Unresolved Questions
1. How to handle multi-region status monitoring without introducing significant infrastructure complexity for self-hosters?
2. Impact of GitHub Action usage limits on "Repo-as-DB" strategies for very high-frequency monitoring.
