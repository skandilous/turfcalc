# Weekly SEO/GEO report (strategist)

Newest week at the bottom. Last 8 weeks kept in full; older weeks rolled into one line each.

> Note: while PR #3 is unmerged, the content plan, log and questions files live on the `agents/setup` branch
> (committing them to `main` now would conflict with PR #3). This report is on `main`.

## Week of 2026-11-16

### Rankings / indexation
Method: web search per query (the search tool isn't AU-localised, so positions are indicative). Keyword volumes,
difficulty, positions and backlinks: **not available** (Open SEO connector needs reconnecting; Search Console not verified).

| Query | TurfCalc | Top 3 seen |
|---|---|---|
| site:turfcalculator.com.au | **not found** (returned other sites only) | — |
| turf calculator australia | not found | lawnsolutionsaustralia.com.au, australianlandscapesupplies.com.au, horticulture.com.au |
| how much turf do i need australia | not found | bunnings.com.au, canstar.com.au, lawnsolutionsaustralia.com.au |
| turf prices australia (per m2) | not found | yellowpages.com.au (2026 guide), premiergrass.com.au, nuway.com.au (2026 price PDFs) |
| turf prices sydney | not found | blogspot scraper, oneflare.com.au, horticulture.com.au |
| how to lay turf australia | not found | lawnsolutionsaustralia.com.au (×3) |
| best time to lay turf australia | not found | myhometurf.com.au, trade.bunnings.com.au, myhometurf.com.au |
| how long before you can walk on new turf | not found | lawnstarter.com, myjobquote.co.uk, calendar-uk.co.uk (no AU page in top 3) |
| turf prices melbourne | not found | asterbank.pages.dev, horticulture.com.au, whatsthedamage.com.au |
| turf prices brisbane | not found | nuway.com.au (×2), whatsthedamage.com.au |
| pallet of turf m² australia | not found | localsearch.com.au (×2), lawnsolutionsaustralia.com.au |
| sir walter buffalo vs kikuyu | not found | spam pages.dev, myhometurf.com.au, lawnsolutionsaustralia.com.au |
| cost to returf a backyard australia | not found | myhometurf.com.au, canstar.com.au, region.com.au |

Live-site check: **not available** — the agent sandbox couldn't reach turfcalculator.com.au this run (outbound fetch blocked),
so page status/schema on the live site wasn't verified.

### GEO (AI-answer style questions)
Asked 5 natural-language questions (turf cost per m², best time to lay turf in Melbourne, how much turf/extra to order,
when to walk on/mow new turf, turf calculator). TurfCalc was cited/surfaced in **none**. Sources that do surface:
Lawn Solutions Australia, myhometurf, Canstar, Yellow Pages, Oneflare, Bunnings (incl. Workshop forum), lawnbyseason.com,
NuWay supplier PDFs; for aftercare questions, mainly UK/US sites.
Gaps vs those pages: (1) explicit **"2026" / dated price tables** — we show no "as of" date; (2) **city-specific** pages
(only Sydney so far); (3) **supplier-sourced numbers** (price lists, pallet sizes); (4) **AU aftercare timelines** —
nobody AU ranks well for "walk on new turf", an easy GEO win.

### Shipped last week
Nothing new went live. Open PRs: #2 *Add structured data and llms.txt* (open since 2026-08-04, mergeable) and
#3 *Set up the SEO/GEO agent team* (opened 2026-11-15, mergeable). No writer/editor/engineer/outreach runs yet (first week).

### Next
Writer (Tue): new guide **turf prices brisbane** (sourced SEQ supplier table) + refresh **/turf-prices-australia**
(dated prices, FAQ). Then pallet m², walk-on-new-turf, best time to lay. Engineer (Thu): sitemap `lastmod` + "Last updated"
lines, or the turf cost estimator. Full queue: `.agents/content-plan.md`.

### Only Skandi can do
1. **Merge PR #2, then PR #3** (GitHub → Pull requests → each → "Merge pull request"). Until #3 is in, the writer has no
   guides section/template and can't publish. Both are currently conflict-free.
2. **Verify Google Search Console**: search.google.com/search-console → Add property → Domain → `turfcalculator.com.au`
   → add the DNS TXT record at your registrar → Verify → Sitemaps → submit `https://turfcalculator.com.au/sitemap.xml`
   → URL inspection → "Request indexing" for `/` and `/turf-prices-sydney`. The site isn't showing in search results yet.
3. **Reconnect Open SEO** in Claude (Settings → Connectors → Open SEO → reconnect) so next week has real AU volumes,
   positions and backlinks.

## Week of 2026-11-23

### Rankings / indexation
Method: web search per query (not AU-localised; positions indicative). Keyword volumes, difficulty, positions: **not available**
(Open SEO now connected but **0 credits**; Search Console not linked). Backlinks: **not available**; Ahrefs free Domain Rating:
**turfcalculator.com.au DR 0** (myhometurf.com.au 49, lawnsolutionsaustralia.com.au 59). Live-site check: **not available**
(sandbox proxy refuses turfcalculator.com.au).

| Query | TurfCalc | Top 3 seen | vs last week |
|---|---|---|---|
| site:turfcalculator.com.au | **not found** (other sites only) | — | same |
| turf calculator australia | not found | lawnsolutionsaustralia.com.au (×2), australianlandscapesupplies.com.au | same |
| how much turf do i need australia | not found | bunnings.com.au, yellowpages.com.au, canstar.com.au | same |
| turf prices australia per m² | not found | yellowpages.com.au (2026 guide), premiergrass.com.au, lawnsolutionsaustralia.com.au | same |
| turf prices sydney | not found | horticulture.com.au PDF, yellowpages.com.au, oneflare.com.au | same |
| turf prices brisbane | not found | whatsthedamage.com.au, nuway.com.au PDF (×2) | same |
| turf prices melbourne | not found | horticulture.com.au PDF, yellowpages.com.au, asterbank.pages.dev | same |
| how to lay turf australia | not found | airtasker.com, lawnsolutionsaustralia.com.au (×2) | same |
| how to measure lawn for turf australia | not found | lawnsolutionsaustralia.com.au (×3) | new check |
| turf types australia / buffalo vs kikuyu | not found | domain.com.au, canstarblue.com.au, allhomes.com.au | new check |
| pallet of turf m² australia | not found | localsearch.com.au (×2), lawnsolutionsaustralia.com.au | same |
| how long before you can walk on new turf | not found | myjobquote.co.uk, aol.com, mybuilder.com (no AU page in top 3) | same |
| best time to lay turf australia | not found | trade.bunnings.com.au, a Google Business page, lawnsolutionsaustralia.com.au | same |
| cost to returf a backyard australia | not found | canstar.com.au, yellowpages.com.au, myhometurf.com.au | same |

### GEO (AI-answer style questions)
Asked: turf cost per m² incl. laying · how much extra turf to order for wastage · when to first mow new buffalo turf ·
best month to lay turf in Melbourne · turf calculator australia. TurfCalc surfaced in **none**. Sources that do surface:
Yellow Pages 2026 guide, Canstar, Localsearch, Lawn Solutions, Oneflare, mowrator, a MidCoast Council turf fact sheet,
lawnbyseason.com; for wastage and Melbourne timing, mostly **UK** sites (onlineturf, rolawn, homebuilding, idealhome).
Gaps vs cited pages (unchanged + new): dated 2026 price tables; city pages; supplier/council-sourced numbers; an AU
wastage % answer (UK sites own it — fold into the pallet guide); AU aftercare timeline. New low-quality competitors
(grassdelivery.pages.dev, blogspot/web.app pages) are ranking on AU queries — a sign these SERPs are winnable with real sourcing.

### Shipped last week
Nothing. Writer ran 2026-11-17 and stopped: PR #3 not merged. No editor, engineer or outreach runs logged.
Open PRs: **#3** *Set up the SEO/GEO agent team* (open since 2026-11-15) and **#2** *Add structured data and llms.txt*
(open since 2026-08-04). No merged pages to check.

### Next
Writer (Tue): **turf prices brisbane** (still top — dated SEQ supplier table, NuWay 2026 price lists), refresh
**/turf-prices-australia** (add "as of November 2026" + per-variety table + FAQ). Queue after: pallet m² (+ wastage %),
walk-on-new-turf, best time to lay, Melbourne prices, cost to returf. Engineer (Thu): sitemap `lastmod` + "Last updated",
then the turf cost estimator. Full queue: `.agents/content-plan.md` on `agents/setup`.

### Only Skandi can do
1. **Merge PR #2, then PR #3** — github.com/skandilous/turfcalc → Pull requests → #2 → "Merge pull request" → Confirm;
   repeat for #3. This is the only thing blocking publishing; week 2 lost.
2. **Get the site indexed** — search.google.com/search-console → Add property → Domain → `turfcalculator.com.au` → add the
   DNS TXT record → Verify → Sitemaps → submit `https://turfcalculator.com.au/sitemap.xml` → URL inspection → "Request
   indexing" for `/`. Then in Open SEO (app.openseo.so → TurfCalculator AU → Search performance) connect that property —
   it's free and gives agents real queries/positions. `site:` still returns nothing.
3. Optional: add `turfcalculator.com.au` to allowed domains (claude.ai → Settings → Capabilities) so agents can check
   the live site; and answer the hosting question in `questions.md`.
