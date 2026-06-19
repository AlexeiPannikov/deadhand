# Deadhand — Brand Voice & Soul

The personality guide. Read before writing any user-facing words: landing copy, dashboard strings, emails, alerts, social.

## The soul, in one line

**Deadhand isn't about death. It's about the thing that doesn't die.**

Your hand stays on the switch even when you're asleep, on holiday, or gone. The brand reference is the Soviet **"Dead Hand" / Perimeter** system — vigilance that keeps watch and acts without you. That's loyalty past the point where you can pay attention. Warm and dependable, not grim.

The mascot energy: a **loyal skeleton night-watchman** who stands guard so you can sleep — not a mourner at a grave.

Mood reference: **Grim Fandango / Día de los Muertos** — death made colorful, playful, hand-tamed. NOT Gothic, NOT funeral, NOT horror.

## Two modes (this is the whole character)

The product's value is **silence** — no news means everything's alive. So the voice has two gears, and the contrast between them *is* the brand.

| | At rest (everything alive) | When something dies |
|---|---|---|
| **Tone** | Dry, deadpan, calm with a smirk. "Calm menace." | Blunt, factual, decisive. Zero jokes. |
| **Goal** | Reassure without being boring | Get the human to act, fast |
| **Example** | "All quiet. Sleep well." | "nightly-backup hasn't checked in for 47 min. Go look." |

A relaxed gravedigger who snaps to attention the instant the corpse is real.

## The hard rule (don't break this — it costs trust)

**Personality lives in the chrome. Alerts stay factual.**

- Play in: empty states, marketing, landing, recovery messages, onboarding, mascot, social.
- Be dead-serious in: the actual alert when something is broken. An agency whose client's prod is down does not want gallows humor in the notification. State what broke, when, what to do. Nothing else.

Playful at rest, dead-serious when it matters.

## Do / Don't

**Do**
- Lean on the "guardian that never sleeps" idea — vigilance, loyalty, you-can-let-go.
- Use death imagery *lightly and warmly* (a wink, never a sob).
- Keep it short. A night-watchman doesn't monologue.
- Make silence feel good ("nothing's dead, sleep well").

**Don't**
- No FUD, no fear-selling, no "ARE YOU EXPOSED?!" — anxiety is the competitor's tool, not ours.
- No grief, mourning, gloom, edgelord darkness.
- No death puns inside real alerts.
- No corporate-observability jargon (no "single pane of glass", no "actionable insights").

## Color semantics

- **Red** = dead / broken. Used sparingly, only for real failure.
- **Amber** = alive / warm / ironic — the resting state. Give amber weight so the brand reads playful, not horror. Red dominating = gloom; amber present = warmth.

## Vocabulary

**Ours:** alive / dead, check in, stays silent, go look, it lives, on watch, sleep well, the switch, never sleeps.

**Not ours:** synergy, observability suite, single pane of glass, actionable insights, leverage, robust, seamless.

## Microcopy bank (reuse / extend)

- Empty dashboard: *"Nothing's dead. Yet. We'll tell you."*
- All healthy: *"All quiet. Sleep well."*
- Alert (factual mode): *"nightly-backup hasn't checked in for 47 min. Go look."*
- Recovery: *"It lives. nightly-backup is back."*
- Onboarding: *"Add one line. Then forget we exist — until something dies."*
- Waitlist confirm: *"You're on the list. We'll wake you when it's time."*
- Footer: *"a dead man's switch for your whole stack."*

## Canonical landing copy (source of truth — keep index.html + og-image in sync with this)

Single source for the hero/social copy. If you change it here, change it in `index.html` (and regenerate `assets/og-image.png`). Last updated 2026-06-19.

- **Hero pill (the "what"):** *Dead man's switch · Uptime · Security drift*
- **Hero H1 (the feeling — lead with this everywhere):** *We're on watch.* **Sleep well.** ← "Sleep well." is the amber-accent half.
- **Hero subhead (the proof / breadth):** *A deploy quietly strips your CSP. A cron job silently stops. An endpoint starts returning 500. Your site still "works" — so nothing alerts you. Deadhand keeps watch over all three: silent while everything's alive, blunt the second it isn't.*
- **Social card title (og:title / twitter:title):** *Deadhand — we're on watch. Sleep well.*
- **SEO `<title>`:** *Deadhand — on watch while you sleep. Cron, uptime & security drift, one monitor.* (keeps the "security drift" keyword for search)
- **Social card body (og/twitter description):** *Silent while everything's alive, blunt the second it isn't. … cron, uptime, and security drift … Flat pricing.*

Retired slogans (don't reuse as primary — kept for history): *"Catch security drift before your users (or attackers) do"* — was the H1; demoted because it only covered the security leg. The "silent while everything's alive…" line lives on as the subhead, not the headline.
