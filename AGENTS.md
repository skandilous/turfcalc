# TurfCalc.au — rules for the agent team

turfcalculator.com.au is a free, independent turf calculator and guide site for Australian homeowners.
Static HTML/CSS/JS, no build step. Clean URLs (`/how-to-lay-turf` serves `how-to-lay-turf.html`).
Hosting is outside Vercel; the live site deploys from `main` on GitHub (`skandilous/turfcalc`).
The owner is Skandi. Goal: more organic visitors from Google **and** more citations in AI answer
engines (ChatGPT, Perplexity, Google AI Overviews, Copilot) — then AdSense revenue.

## The team (scheduled tasks, all Australia/Sydney time)

| Agent | When | Job | Can merge to main? |
|---|---|---|---|
| SEO/GEO strategist | Mon | Measure, research demand, keep `.agents/content-plan.md` current, write the weekly report | No site changes; commits `.agents/` files directly |
| Writer | Tue | Write 1 new guide + refresh 1 existing page, open a PR labelled `content` | No |
| Editor | Wed | Independently fact-check the writer's PR; merge if it passes, else fix or escalate | **Yes, content PRs only** |
| Technical SEO engineer | Thu | One structural/technical SEO or GEO improvement as a PR for Skandi | No — Skandi merges |
| Outreach | Fri | Find backlink prospects, write Gmail **drafts** only | n/a |

### What may go live without Skandi
- **Content PRs** (new files under `guides/`, edits to body copy of existing guide pages, the guides
  index, sitemap entries for new guides, `llms.txt` entries) — merged by the Editor after its check.
- `.agents/*.md` bookkeeping files — any agent may commit these directly to `main`.

### What always waits for Skandi (PR, never merged by an agent)
Anything in `<head>` site-wide, nav/footer, `style.css`, JavaScript, the calculators, `index.html`
layout, `robots.txt`, redirects/hosting config, analytics/AdSense tags, new calculators, deleting pages,
changing URLs.

## Content rules (non-negotiable)
1. **Australian** spelling, units (m², m³, mm), prices in AUD incl. GST, and Australian context
   (climate zones, states, local varieties: Sir Walter buffalo, Kikuyu, TifTuf, Eureka, Zoysia, couch).
2. **No invented numbers.** Every price, coverage figure, pallet size or statistic must come from a source
   fetched in this run (supplier price pages, state government, Bureau of Meteorology, council water rules,
   university/extension or industry body pages). Give ranges, name the source, add an "as of <Month YYYY>".
3. **Answer-first (GEO).** The first paragraph answers the headline question directly, with a number
   where there is one. H2s are the questions people actually type. Use tables for numbers. Each page
   gets an FAQ block (3–5 Qs) with matching `FAQPage` JSON-LD.
4. Independent: no claims of affiliation, no fake reviews, testimonials, author personas or credentials.
   Byline is "TurfCalc.au guides". No affiliate links unless Skandi adds a program.
5. No health/safety overreach (chemicals: refer to the product label and state rules).
6. Every new guide links to the calculator (`/`) and 2+ related pages; add a link **to** it from at least
   one existing relevant page (content edit, allowed).
7. 900–1,800 words. Quality over volume. One topic/keyword cluster per page — never cannibalise an
   existing page (check the table in README.md and `guides/`).

## How to publish a guide
1. Copy `.agents/post-template.html` to `guides/<slug>.html`, fill every `{{…}}`, **delete the
   `noindex` line**. Slug = lowercase-hyphenated target query (e.g. `best-time-to-lay-turf-melbourne`).
2. Add `<li><a href="/guides/<slug>">Title</a><span class="d">one-line summary</span></li>` directly
   under `<!-- GUIDES-LIST -->` in `guides/index.html` (newest first).
3. Add `<url><loc>https://turfcalculator.com.au/guides/<slug></loc><lastmod>YYYY-MM-DD</lastmod><priority>0.7</priority></url>` to `sitemap.xml`.
4. Add a line to the Guides section of `llms.txt`.
5. Validate: `python3 -c "import json,re,sys;[json.loads(m) for m in re.findall(r'<script type=\"application/ld\+json\">(.*?)</script>', open(sys.argv[1]).read(), re.S)]" guides/<slug>.html`
   and check no `{{` remains (`grep -c '{{' guides/<slug>.html` must be 0).

## Coordination files (in `.agents/`)
- `content-plan.md` — strategist-owned queue of the next 4–6 topics with target query, intent,
  angle, sources to use, internal links. The writer takes the top `ready` item.
- `log.md` — append one line per run: `YYYY-MM-DD | agent | what happened | PR/commit link`.
- `questions.md` — open questions/blockers for Skandi (agents read his answers here; never repeat an
  open question).
Do **not** put email addresses, outreach contacts or private analytics exports in this public repo.

## Git
Branches: `content/<slug>`, `seo/<short-name>`. Push with
`git -c push.negotiate=true push -u origin <branch>`. Open PRs with `gh pr create`. Never force-push
`main`, never rewrite history.
