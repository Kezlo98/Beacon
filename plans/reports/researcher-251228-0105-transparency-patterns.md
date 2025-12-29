# Research Report: Transparent Product Communication & Public Roadmaps
Date: 2025-12-28
Author: Researcher Agent

## 1. Transparency Patterns

### Linear: The "Unified Feed" & Momentum
- **Pattern**: Linear uses a "Changelog" as a narrative tool for momentum. It's not just a list of fixes but a high-production value showcase of "what's new."
- **Roadmap Disclosure**: They use "Initiatives" with specific attributes (owner, health, target dates).
- **Key Insight**: Transparency is used as a brand differentiator. "Write issues, not user stories" to maintain technical momentum that translates to public updates.

### Notion: The Feature Showcase
- **Pattern**: Notion groups updates into major "Releases" (e.g., Notion 2.44) and smaller incremental updates.
- **Roadmap Disclosure**: Public roadmaps are often shared as Notion pages themselves, reinforcing "Eating your own dog food."
- **Key Insight**: Use the product itself to communicate the roadmap to build meta-trust.

### Vercel: Shipping as a Service
- **Pattern**: Extremely high frequency (daily/weekly). "See what shipped" is the core CTA.
- **Roadmap Disclosure**: They often announce "Beta" or "Early Access" features within the changelog, blurring the line between roadmap and shipping.
- **Key Insight**: Velocity itself is a signal of transparency.

## 2. User Trust Building

### Status Page & Incident Communication
- **Trust Factors**:
  - **Timeliness**: First update within 15-30 minutes of incident detection.
  - **Clarity**: Avoiding technical jargon; using "Investigating," "Identified," "Monitoring," and "Resolved" states.
  - **Post-mortems**: Public RCA (Root Cause Analysis) for major outages is non-negotiable for high-trust brands (e.g., Vercel, AWS).
- **Update Frequency**: Real-time for active incidents; periodic (quarterly/monthly) for roadmap "Health" checks.

## 3. Technical Signals

### Automation & GitHub Integration
- **Patterns**:
  - **GitHub Actions**: Automating changelog generation from PR labels or Conventional Commits.
  - **CI/CD Exposure**: Showing "Build: Passing" or deployment status on public-facing docs/status pages.
  - **SDKs**: Providing public SDKs (e.g., `linear-sdk`) as a form of transparency for platform stability.
- **Manual vs. Automated**: Best practice is "Automated data, Manual narrative." Use automation to gather technical changes, but manual curation to explain the *value* to users.

## 4. Roadmap Disclosure Levels
- **Committed**: Features with target quarters (Q1, Q2) and assigned teams. High accountability.
- **Exploring/Backlog**: High-level themes without dates. Sets expectations for "vision" without promising "delivery."

## Sources
- [Linear Method: Product Updates](https://linear.app/method/product-updates)
- [Vercel Changelog](https://vercel.com/changelog)
- [Notion Releases](https://www.notion.com/releases)
- [Atlassian Statuspage Best Practices](https://www.atlassian.com/software/statuspage)

## Unresolved Questions
- How do these companies handle "NDA features" in an automated CI/CD pipeline without accidental leaks?
- What are the cost-benefit trade-offs for small teams maintaining high-production changelogs?
