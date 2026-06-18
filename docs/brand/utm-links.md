# UTM Links — validation campaign

Tag every shared link so PostHog → Web Analytics shows which channel drives signups. Without UTMs everything collapses into "direct / referrer" and you learn nothing about distribution.

**Convention:** `utm_source` = platform · `utm_medium` = format · `utm_campaign=validation` (constant this phase) · `utm_content` = specific place. PostHog auto-parses all of these.

Copy the link for wherever you post:

| Channel | Link |
|---|---|
| Reddit — r/webdev | `https://deadhand.app/?utm_source=reddit&utm_medium=post&utm_campaign=validation&utm_content=webdev` |
| Reddit — r/devops | `https://deadhand.app/?utm_source=reddit&utm_medium=post&utm_campaign=validation&utm_content=devops` |
| Reddit — r/selfhosted | `https://deadhand.app/?utm_source=reddit&utm_medium=post&utm_campaign=validation&utm_content=selfhosted` |
| Reddit — r/SaaS | `https://deadhand.app/?utm_source=reddit&utm_medium=post&utm_campaign=validation&utm_content=saas` |
| Reddit — comment (any) | `https://deadhand.app/?utm_source=reddit&utm_medium=comment&utm_campaign=validation` |
| IndieHackers | `https://deadhand.app/?utm_source=indiehackers&utm_medium=post&utm_campaign=validation` |
| Hacker News | `https://deadhand.app/?utm_source=hackernews&utm_medium=post&utm_campaign=validation` |
| Twitter / X | `https://deadhand.app/?utm_source=twitter&utm_medium=social&utm_campaign=validation` |
| Telegram channel/chat | `https://deadhand.app/?utm_source=telegram&utm_medium=community&utm_campaign=validation` |
| Discord community | `https://deadhand.app/?utm_source=discord&utm_medium=community&utm_campaign=validation` |
| Dev.to article | `https://deadhand.app/?utm_source=devto&utm_medium=article&utm_campaign=validation` |
| Product Hunt | `https://deadhand.app/?utm_source=producthunt&utm_medium=launch&utm_campaign=validation` |
| Lobsters | `https://deadhand.app/?utm_source=lobsters&utm_medium=post&utm_campaign=validation` |

## Notes

- Add a new row, don't improvise — consistent `utm_source` spelling keeps the report clean (one typo = a separate phantom channel).
- For a new subreddit/community, copy a similar row and change only `utm_content`.
- In PostHog: **Web Analytics** shows sources at a glance; build a Funnel filtered by `utm_source` to compare which channel actually converts to `waitlist_signup`, not just which sends clicks.
