# Research Index — Dormant Client Reactivation

**Owner:** Meraj
**Source of truth for scope:** [`../PROJECT_PLAN.md`](../PROJECT_PLAN.md)
**Phase:** PHASE 1 — Market Validation (in progress)
**Last research pass:** 2026-09-27

---

## Files

| File | Purpose | State |
|---|---|---|
| [market.md](market.md) | Market landscape, category structure, demand evidence | First pass done |
| [competitors.md](competitors.md) | Per-product findings with sources + confidence | First pass done (16 products) |
| [customer-pain.md](customer-pain.md) | Pain evidence register, by evidence quality | **Desk research only — 0 interviews** |
| [evidence-against.md](evidence-against.md) | Anti-bias: reasons this product may be unnecessary | First pass done (10 kill risks) |
| [opportunity-gaps.md](opportunity-gaps.md) | Validated vs. assumed gaps + the recommended wedge | First pass done |
| [pricing.md](pricing.md) | Competitor pricing, India WTP, unit economics | First pass done |
| [integrations.md](integrations.md) | Real cost/compliance of each integration | First pass done |
| [reddit-insights.md](reddit-insights.md) | Community pain | **BLOCKED — manual protocol provided** |
| [founder-data-test.md](founder-data-test.md) | Phase 2 protocol + empty metrics table | Template ready, **not run** |
| [customer-interview-guide.md](customer-interview-guide.md) | Phase 3 screener, script, scoring | Template ready, **not run** |
| [customer-interviews.md](customer-interviews.md) | Interview log | Empty — awaiting real interviews |
| [templates/founder-50-contact-template.csv](templates/founder-50-contact-template.csv) | Dataset template for Phase 2 | Ready |
| [templates/import-schema.md](templates/import-schema.md) | V0 import schema spec | Ready |

Root-level: [`../HYPOTHESES.md`](../HYPOTHESES.md), [`../DECISIONS.md`](../DECISIONS.md), [`../CHANGELOG.md`](../CHANGELOG.md)

---

## Evidence labels (per plan §36)

- **FACT** — directly supported by a cited source or the founder's own first-party data
- **HYPOTHESIS** — an idea that still needs validation
- **ASSUMPTION** — currently believed, unverified
- **DECISION** — a deliberate product decision
- **EXPERIMENT** — a test designed to validate or refute

## Confidence legend

| Level | Meaning |
|---|---|
| **High** | Official vendor/regulator/standards page, or founder's own first-party data |
| **Medium** | Multiple independent third-party sources agreeing, or one credible primary-ish source (press release, official KB via search) |
| **Low** | Single third-party source, affiliate/SEO review site, or vendor marketing claim |
| **Unverified** | Recorded for follow-up; not usable in any decision yet |

---

## ⚠️ Known limits of this research pass — read before trusting any number

1. **Direct page fetches were blocked.** This session's network policy denied outbound access to vendor domains (`www.folk.app`, `getdex.com`, `attio.com` — and even `en.wikipedia.org`). All competitor/pricing findings below therefore come from **search-result evidence, not from the vendors' own pricing pages**. Plan §33 asks for official pages; that requirement is **not yet met**. Every price is capped at **Medium** confidence until re-checked on the official page.
2. **Reddit is not accessible to the search tool** (`reddit.com` is blocked to its user agent). Plan §34's `reddit-insights.md` could not be filled by automated research. A manual 60-minute protocol is in [reddit-insights.md](reddit-insights.md).
3. **Zero customer interviews exist.** Plan §47 Step 4 asks for 10 concrete customer pain examples. Desk research cannot produce those. [customer-pain.md](customer-pain.md) separates what is genuinely evidenced from what is still a guess, and says so plainly rather than padding the count.
4. **Most "reactivation statistics" on the open web are vendor marketing.** They contradict each other by 8x (see [market.md](market.md) §3). None of them are usable in a landing page or a business case.
5. **Currency conversion assumption:** where USD figures are converted to INR, this uses **≈₹88/USD** — an **ASSUMPTION**, not a checked rate. Verify before using any ₹ figure in a decision.

## How to re-run this research correctly

Re-check each **Medium**-confidence price on the vendor's own pricing page, then upgrade to High and update the `Checked` date. Either raise this environment's network access level (cloud environment menu in the session title bar → Edit → Network access; levels documented at https://code.claude.com/docs/en/claude-code-on-the-web), or open the pages manually and paste the numbers in.
