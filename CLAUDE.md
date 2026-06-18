# Deadhand

A focused monitoring SaaS for solo devs, small teams, and agencies. One tool, three silent failures:

1. **Dead man's switch** — heartbeat/cron monitoring. Jobs ping a URL; we stay silent while pings arrive on time, alert when one's late, runs too long, or fails.
2. **Uptime** — HTTP checks (status, response time, keyword), plus SSL & domain expiry.
3. **Security drift** ★ — the wedge. Baseline an endpoint (security headers, cookie flags, redirects, exposed paths like `/.env`), then alert **only on regression** vs that baseline. A tripwire for "today is less safe than yesterday." Not a pentest.

**Positioning:** NOT "another cron+uptime tool" — Cronitor/BetterStack already bundle those. Lead with **security drift** (the underserved leg) + **flat pricing** (vs per-monitor pricing that punishes indie users). Web dashboard for everyone + monitors-as-code (YAML) for those who want it.

**Deliberately out of scope:** status pages, on-call/escalation, logs/APM/RUM, full pentest/DAST, multi-region/screenshots/traceroute. Staying narrow is the product.

## Current status: validation, no product yet

We're testing demand **before** writing the product. `index.html` is a fake-door landing page.

- **Stack:** single static `index.html`, no framework, no build. Deploy to Vercel or Cloudflare Pages. (Next.js is for the real product later, not the landing.)
- **Domain:** `deadhand.app` (bought). `.io`/`.com` are parked — revisit only if validation passes.
- **Analytics:** PostHog (US region, token in `index.html`). Key events: `section_interest`, `pricing_click`, `waitlist_signup`.
- **Waitlist:** Formspree (`xrevvpzn`) — stores submissions + `tier_interest`, CSV export.
- **Kill-criterion:** <30 waitlist signups in 2 weeks, OR interest lands only on uptime/cron and skips security → pivot the pitch or stop.

## Docs

- [docs/brand/brand-voice.md](docs/brand/brand-voice.md) — the soul: personality, two-mode voice, do/don't, vocabulary, microcopy. **Read before writing any user-facing copy.**
- [docs/brand/mascot.md](docs/brand/mascot.md) — Hank, the skeleton night-watchman: character bible, two-mode poses, wardrobe, palette, generation prompts.
- [docs/brand/positioning.md](docs/brand/positioning.md) — the idea, target customer, competitors, differentiation, pricing, SEO strategy.
- [docs/brand/utm-links.md](docs/brand/utm-links.md) — UTM-tagged share links per channel. Use these (not bare URLs) when posting, so PostHog attributes signups to a source.

## Working notes

- All user-facing copy must follow `docs/brand/brand-voice.md`. The hard rule: playful at rest, dead-serious in alerts.
- Pricing on the landing is a fake-door (Free $0 / Solo $5 / Team $12 / Agency $29, flat). Not real billing yet. **Cron + uptime are free; security drift (the wedge) is gated to paid (Solo+)** — the pricing structure itself sells the differentiation and measures willingness to pay for the wedge.
