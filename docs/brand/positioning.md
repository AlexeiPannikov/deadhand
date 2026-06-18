# Deadhand — Positioning & Go-to-Market

## The idea

One narrow, affordable monitoring tool covering three silent failures (dead man's switch / uptime / security drift) in one dashboard and one alert flow. For technical buyers who value simplicity and hate bloat.

## Target customer

Solo developers, small SaaS teams, and agencies managing client sites. They currently either stitch together separate tools (cron monitor + uptime checker + manual SSL reminders) or overpay for a big observability suite where this is a minor bundled feature.

## The honest competitive reality

"Unify three tools" is **only half a differentiator** — the cron + uptime + SSL-expiry combo is **already bundled** by incumbents:

- **BetterStack** — uptime, SSL, domains, DNS, ports, SMTP, *and* cron via heartbeats. Complex per-metric pricing (~$79/mo at 100 monitors).
- **Cronitor** — grew from cron into uptime + SSL + domain expiry + status pages. Per-monitor + per-seat ($2/monitor + $5/user → $100+/mo fast).
- **Healthchecks.io** — the cron/heartbeat gold standard. Generous free tier (20 checks). Open source.
- **UptimeRobot, HetrixTools** — uptime + SSL (+ blacklist).

Coming out as "another cron+uptime tool" = 5th identical product with no angle.

## Where the real gap is

**Security drift** — security-headers regression after a deploy, exposed `/.env` / `/.git`, cookie-flag loss, broken HTTPS redirect. Mainstream uptime tools **do not** watch this (SSL expiry is commodity; posture *regression* is not). Today this is split between one-shot checkers (securityheaders.com clones) and heavy DevSecOps. Continuous baseline-and-diff + alert, in one tool with uptime, is the wedge.

## Two differentiators

1. **Security drift as the headline** (cron + uptime = table stakes you include so people don't need a second tool).
2. **Flat pricing** — incumbents charge per-monitor / per-seat. Flat-rate is a proven counter-wedge (whole comparison pages exist around "flat vs per-monitor").

**Pricing structure (fake-door): Free $0 / Solo $5 / Team $12 / Agency $29, flat, cumulative.** Cron + uptime are free like everyone else; **security drift is gated to paid (Solo+)**. This makes the pricing itself sell the differentiation, and a `pricing_click` on a paid tier is a clean signal of willingness to pay for the wedge (vs free-seekers picking Free).

## Scope discipline

**Build (MVP):** heartbeat/cron, HTTP uptime + keyword + SSL/domain expiry, security-drift baseline+diff, one alert flow (email/Slack/Telegram/webhook/Discord), web dashboard + monitors-as-code (YAML).

**Deliberately NOT:** status pages, on-call/escalation, logs/APM/RUM, full pentest/DAST/CVE scanning, multi-region/screenshots/traceroute, chasing 25+ integrations. Saying no is part of the pitch.

## SEO strategy

Head term **"cron job monitoring" is owned** by Cronitor/Healthchecks — don't fight it. Win on three flanks:

1. **"X alternative" pages** — "healthchecks.io alternative", "cronitor alternative", "dead man's snitch alternative". High intent, these rank in this niche.
2. **Security-drift long-tail** (low competition, our unique angle) — "security headers monitoring", "alert when security headers change", "detect exposed .env endpoint", "security regression after deploy", "ssl certificate expiry monitoring".
3. **Brand + "dead man's switch"** — matches the name, less contested than "cron monitoring".

## Validation (current phase)

Fake-door landing (`index.html`). Main hypothesis: *people will pay for security-drift alerting, not just uptime.*

- PostHog events: `section_interest` (which of 3 pains pulls), `pricing_click` (which flat tier), `waitlist_signup`.
- **Kill-criterion:** <30 waitlist in 2 weeks, OR all interest lands on uptime/cron and skips security → pivot pitch or stop.
- If it passes: build the real product (Next.js + dashboard + API), then make an offer on `deadhand.io`/`.com`.
