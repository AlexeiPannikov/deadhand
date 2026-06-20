# Deadhand

A focused monitoring SaaS for solo devs, small teams, and agencies. One tool, three silent failures:

1. **Dead man's switch** — heartbeat/cron monitoring. Jobs ping a URL; we stay silent while pings arrive on time, alert when one's late, runs too long, or fails.
2. **Uptime** — HTTP checks (status, response time, keyword match).
3. **SSL & domain expiry** — watch TLS certs and domain registration; warn well before either lapses.

**Positioning:** flat pricing (vs per-monitor pricing that punishes indie users), one tool instead of three, and the dead man's switch for cron as the lead hook. Web dashboard for everyone + monitors-as-code (YAML) for those who want it.

> ⚠️ **Open strategic gap (2026-06-20):** security drift — formerly the documented wedge — was **dropped** by founder decision after the keyword recon suggested weak search demand and an already-crowded header-monitoring niche. The honest consequence: Deadhand currently competes head-on with Cronitor/BetterStack/UptimeRobot on **flat pricing alone**, which is a thin differentiator. A new wedge/angle still needs to be defined. Note this pivot was made **before** any real validation traffic (Reddit posts were filtered/banned, PostHog has ~0 `section_interest` data), so the "nobody wants security drift" call is a hunch, not data.

**Deliberately out of scope:** status pages, on-call/escalation, logs/APM/RUM, full pentest/DAST, multi-region/screenshots/traceroute. Staying narrow is the product.

## Current status: validation, no product yet

We're testing demand **before** writing the product. `index.html` is a fake-door landing page.

- **Stack:** single static `index.html`, no framework, no build. Deploy to Vercel or Cloudflare Pages. (Next.js is for the real product later, not the landing.)
- **Domain:** `deadhand.app` (bought). `.io`/`.com` are parked — revisit only if validation passes.
- **Analytics:** PostHog (US region, token in `index.html`). Key events: `section_interest`, `pricing_click`, `waitlist_signup`.
- **Waitlist:** Formspree (`xrevvpzn`) — stores submissions + `tier_interest`, CSV export.
- **Kill-criterion:** <30 waitlist signups in 2 weeks → pivot the pitch or stop. (The old "interest skips security" sub-criterion is retired now that the security leg is dropped.)

## Docs

- [docs/brand/brand-voice.md](docs/brand/brand-voice.md) — the soul: personality, two-mode voice, do/don't, vocabulary, microcopy. **Read before writing any user-facing copy.**
- [docs/brand/mascot.md](docs/brand/mascot.md) — Hank, the skeleton night-watchman: character bible, two-mode poses, wardrobe, palette, generation prompts.
- [docs/brand/positioning.md](docs/brand/positioning.md) — the idea, target customer, competitors, differentiation, pricing, SEO strategy.
- [docs/brand/utm-links.md](docs/brand/utm-links.md) — UTM-tagged share links per channel. Use these (not bare URLs) when posting, so PostHog attributes signups to a source.

## Working notes

- All user-facing copy must follow `docs/brand/brand-voice.md`. The hard rule: playful at rest, dead-serious in alerts.
- Pricing on the landing is a fake-door (Free $0 / Solo $5 / Team $12 / Agency $29, flat). Not real billing yet. **Cron + uptime are free; paid (Solo+) adds faster checks, more channels, SSL & domain expiry, and higher monitor counts.** The paid gate is now feature/volume-based (not a single wedge), so it measures willingness to pay for convenience rather than for a unique capability — a weaker signal worth keeping in mind.
