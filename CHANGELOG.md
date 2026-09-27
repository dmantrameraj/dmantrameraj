# Changelog

Required by [PROJECT_PLAN.md](PROJECT_PLAN.md) §40 rule 6.

---

## 2026-09-27 — Phase 1 research pass #1

**No product code written.** Plan §47 Step 10 (STOP before building) respected.

### Added
- `PROJECT_PLAN.md` — the master plan vendored into the repo as the source of truth
- `research/README.md` — index, evidence labels, confidence legend, and an explicit statement of this pass's limits
- `research/market.md` — market structure, demand evidence, and a finding that published reactivation statistics are unusable
- `research/competitors.md` — 16 products across four tiers, comparison matrix, per-product sources and confidence
- `research/customer-pain.md` — pain register separated by evidence quality; states plainly that 0 interviews exist
- `research/evidence-against.md` — 10 reasons the product may be unnecessary, each with a falsification test (plan §37)
- `research/opportunity-gaps.md` — each of plan §16's assumed gaps tested; recommended wedge (plan §47 Step 7)
- `research/pricing.md` — competitor prices, India WTP, AI unit economics, price-test design
- `research/integrations.md` — real cost and policy of each integration; revised integration order
- `research/reddit-insights.md` — **blocked**, with a manual 60-minute protocol instead of invented content
- `research/founder-data-test.md` — Phase 2 protocol, 15 metrics, all blank
- `research/customer-interview-guide.md` — screener, 30-question script, gate scoring
- `research/customer-interviews.md` — empty log with per-interview template
- `research/templates/founder-50-contact-template.csv` — 50-contact dataset template (plan §47 Step 8)
- `research/templates/import-schema.md` — V0 import schema spec with the critical-field kill threshold
- `HYPOTHESES.md` — H1–H8 from plan §42, assessed; **H9** and **H10** added from this pass
- `DECISIONS.md` — D-001 … D-011
- `CHANGELOG.md` — this file

### Changed
- `.gitignore` — excludes real client data, interview transcripts and `.env` files

### Untouched
- The existing Vite/React app in this repo ("Imaginom" poster designer) — not modified in any way

### Key findings
1. **The plan's thesis is proven at enterprise price and as a human service, not as affordable software.** UserGems charges $33k–$120k/yr for this reasoning; WinbackEngine takes a $5,000 deposit to have humans phone lapsed customers. Nothing comparable exists near ₹999/month.
2. **The single biggest risk is missing data, not competition.** The intelligence layer needs `total_value`, `previous_services` and `previous_interest`, and the stated ICP (spreadsheet/Gmail/WhatsApp users) probably does not record them. One hour of measurement can settle it.
3. **Published reactivation statistics are unusable** — an 8× spread (<5% to 40%) across vendor sources for the same claim.
4. **Recommended wedge:** *"the service you never sold them"* — dormant × already paid × discussed-but-never-bought. Checkable against the user's own file, so it cannot be fabricated.
5. **Gmail is the most expensive integration in the plan** — an annual CASA audit at $500–$4,500/yr ≈ 22 customers' annual revenue at ₹499/mo. Coretex should come first.
6. **Two of the plan's assumed gaps are refuted** (CSV import as a differentiator; "no competitor explains why") and should leave the pitch.

### Not done — and why
- **0 customer interviews** — cannot be done by desk research; plan §47 Step 4's "10 concrete pain examples" is therefore **not met**, and 10 falsifiable pain hypotheses are provided in its place
- **Reddit/community research** — `reddit.com` is inaccessible to the research tooling; manual protocol supplied
- **No official vendor pricing page was reachable** — this environment's network policy blocked every vendor domain, so all prices are capped at Medium confidence and must be re-verified
- **No market sizing** — no credible source existed; fabricating a TAM would breach plan §40 rule 13
- **G2/Capterra competitor complaints** (plan §15) — not captured yet
