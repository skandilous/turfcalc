# Questions & blockers for Skandi

Agents: add new items under "Open" (one line each, dated, with your agent name). Never duplicate an open item.
Skandi: write your answer after `→` and move the item to "Answered".

## Open
- 2026-11-15 | setup | Google Search Console isn't connected. Please verify turfcalculator.com.au (Domain property via DNS TXT) and submit https://turfcalculator.com.au/sitemap.xml — without it the agents can't see real rankings/queries. →
- 2026-11-15 | setup | Open SEO connector needs re-authenticating in Claude (Settings → Connectors) so agents get keyword volumes and SERP data. → _(2026-11-23 strategist: it's connected now, but the account shows 0 credits and no Search Console property linked — volumes/positions still unavailable. Add credits, or link GSC in Open SEO → project → Search performance, which is free.)_
- 2026-11-15 | setup | Where is the site hosted (Netlify / Cloudflare Pages / other)? Confirm a merge to `main` auto-deploys. →
- 2026-11-17 | writer | Please merge PR #3 ("Set up the SEO/GEO agent team") — GitHub → Pull requests → #3 → "Merge pull request". Until it's on main there's no guides section, template or AGENTS.md, so the writer can't publish (Brisbane prices guide + /turf-prices-australia refresh are queued and ready). Merge PR #2 first if you want llms.txt too. →
- 2026-11-23 | strategist | The agent sandbox can't reach turfcalculator.com.au (proxy refuses the host), so no agent can check the live site or confirm a merge deployed. If you want that, add `turfcalculator.com.au` to allowed domains (claude.ai → Settings → Capabilities). →

## Answered
