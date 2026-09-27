# Market Research

**Checked:** 2026-09-27
**Confidence caveats:** see [README.md](README.md) §⚠️ — no official pages could be fetched; Reddit inaccessible.

---

## 1. Is there a market, or only a market for content about the market?

**FACT:** There is real, priced demand for dormant-database reactivation as a **service**.

| Evidence | What it proves | Source |
|---|---|---|
| WinbackEngine (LTVplus) launched Mar 2026 charging a **$5,000 deposit** with a 3× ROI guarantee to phone lapsed customers for franchises | A CX company with 500+ staff judged this a standalone product line | [GlobeNewswire 2026-03-26](https://www.globenewswire.com/news-release/2026/03/26/3263235/0/en/LTVplus-Launches-WinbackEngine-A-Performance-Based-Customer-Reactivation-Service-for-Multi-Location-Franchises.html) |
| WinBack Labs sells a **$10,000 pilot** with a 5× ROI guarantee | Buyers accept five-figure prices for one cohort | [winbacklabs.com](https://winbacklabs.com/programs-and-pricing/) |
| UserGems charges **$33k–$120k/yr** to surface past customers/champions when circumstances change | Enterprise pays heavily for exactly this reasoning | [salesmotion.io](https://salesmotion.io/blog/usergems-pricing) |
| "Database reactivation" is a named, standardised **agency playbook** in GoHighLevel with a large ecosystem of implementation content | Agencies sell it to clients repeatedly | [hlgrowthpartner.com](https://hlgrowthpartner.com/post/gohighlevel-database-reactivation-campaign-2026), [automatetogrow.com](https://automatetogrow.com/database-reactivation-win-back-dormant-leads/) |
| AINORA's landing headline is literally *"How much revenue is sitting dormant in your CRM?"* | The pain is marketable without explanation | [ainora.lt](https://ainora.lt/database-reactivation) |

**Confidence: Medium-High.** These are revealed preferences (money moving), not survey answers.

**HYPOTHESIS (unproven):** that this demand exists *at the bottom of the market as software*. Every priced data point above is either **enterprise software** or a **human service at $5k+**. No evidence was found in this pass of anyone successfully selling dormant-client *intelligence* as self-serve software to solo operators. That is the hole the plan proposes to fill, and it is currently **an assumption, not a finding**.

---

## 2. Category structure

**FACT:** "Relationship intelligence" is an established category — described as created around 2018 to solve B2B relationships being scattered across CRM, email, calendar and LinkedIn ([getboomerang.ai glossary](https://www.getboomerang.ai/glossaries/relationship-intelligence-platforms-2026), Medium-Low confidence, single source).

**FACT:** "Signal-based selling" is the current enterprise framing: signal types include first-party activity, **relationship changes**, account intent, market events and website visitor identification ([Common Room](https://www.commonroom.io/blog/signal-based-selling-definition/), [syncgtm.com](https://syncgtm.com/blog/buying-signals-tools-sell-right-accounts-2026)).

**Implication for positioning:** the plan's §17 three-way distinction (CRM manages pipeline / follow-up tool reminds / this product finds cold-but-valuable relationships) is real but **already occupied at the top of the market under the name "signal-based selling"**. Marketing should therefore *not* claim a new category. The defensible claim is a **new price point and a new data source** for an existing, enterprise-proven idea: *your own invoices and project history are the signal*.

---

## 3. ⚠️ The reactivation "statistics" on the open web are unusable

The plan §12 says "Do NOT invent success numbers." The web will happily invent them for us. Numbers found in one search, all presented as benchmarks:

| Claim | Source type |
|---|---|
| Strong win-back campaigns reactivate **10–30%** of lapsed customers | vendor blog |
| Average win-back success rates run **20–40%** | vendor blog |
| A healthy programme reactivates **12–20%** of all lapsed customers | vendor blog |
| **~40%** at 30-day lapse, 25% at 60, 12% at 90, **<5% after 180 days** | vendor blog "benchmark summary" |
| Email reactivation typically converts **8–15%** of the lapsed segment | vendor blog |
| GHL DBR gets **2–8% reply** rate (a *reply*, not a sale) | agency SEO page |
| ROI "often around 7:1"; **71%** of marketers say win-back is the highest-ROI email tactic | vendor blog |
| Reacquired customers **double or triple** LTV; **47%** generate more revenue than before | vendor blog |

**Sources:** [opensend.com](https://www.opensend.com/post/win-back-campaign-success-rate-statistics) · [winbackengine.com benchmarks](https://winbackengine.com/blog/customer-reactivation-rate-benchmarks/) · [mailmend.io](https://mailmend.io/blogs/win-back-campaign-statistics) · [clepher.com](https://clepher.com/win-back-campaign/) · GHL pages above.

**FINDING (Medium-High confidence, and it is a negative one):** The credible-sounding range spans **<5% to 40%** — an 8× spread — and the only figure describing a *concrete, measurable* outcome (GHL's 2–8%) is also the **lowest and refers only to a reply**. Every source is a vendor or affiliate with an incentive. No independent or academic benchmark surfaced.

**DECISION (recorded in [DECISIONS.md](../DECISIONS.md)):** Do not use any third-party reactivation statistic in the landing page, pricing model, or investor/customer conversation. The only trustworthy number will be the founder's own Phase 2 + Phase 4 measured result. Plan §31's "Do not claim guaranteed revenue" is upgraded to: **do not claim any rate at all until we have measured our own.**

**Also note:** the same search surfaced the "40% at 30 days → <5% at 180 days" decay claim. If that shape is even directionally true, it is **bad news for this product's core premise**, which is about contacts dormant **124+ days**. See [evidence-against.md](evidence-against.md) §5.

---

## 4. Timing conventions the market has settled on

**FACT (Medium confidence, consistent across sources):** 90 days of no meaningful activity is the de-facto dormancy threshold — GHL DBR defines the segment as "no meaningful activity for 90 days or more"; e-commerce practice is to start within 30–90 days and segment by depth.

**FACT (High confidence — Spamhaus, an authority, not a vendor):** Email sunset policies use **90 days for daily senders, 180 for monthly senders**; abandoned mailboxes are **recycled into spam traps**; 180+ days without engagement materially raises the odds an address is now a trap, and dormant addresses drag whole-domain reputation down.
Sources: [Spamhaus](https://www.spamhaus.org/resource-hub/deliverability/what-is-an-email-sunset-policy-and-why-do-you-need-one/) · [Bento docs](https://bentonow.com/docs/deliverability/list_hygiene) · [Omnisend](https://support.omnisend.com/en/articles/3405334-what-is-an-email-sunset-policy)

**This is a product-defining constraint, and a genuine differentiator:**
The whole industry's advice is *"stop emailing people who have been quiet for 180 days."* The plan's product exists to surface people quiet for **124+ days**. Those two facts are only compatible if the product does what the plan §20 already insists on: **a small, hand-approved, individually-reasoned, one-to-one message — not a campaign.**

That reframes the pitch from "find more people to email" to something sharper and evidence-backed:

> **Sending to your whole dormant list burns your domain. This tells you the eight worth a personal message.**

**Confidence: High** on the deliverability facts; **HYPOTHESIS** that this framing sells.

---

## 5. India-specific market conditions

| Finding | Detail | Confidence | Source |
|---|---|---|---|
| Indian SMB willingness-to-pay is structurally low | 60–70% lower than Western markets; heavy discount expectation; big metro vs Tier-2/3 gap | Low-Medium (consultant content) | [upgrowth.in](https://upgrowth.in/saas-pricing-packaging-strategy-india-gtm/) |
| SMBs benchmark software against **labour**, not other software | If it costs more than a junior employee (**₹15,000–25,000/mo**), value must be overwhelming | Low-Medium | [evandsouza.com](https://evandsouza.com/articles/saas-pricing-strategies-for-indian-startups-a-comprehensive-framework/) |
| Tier conventions | **₹299–₹499/mo** = individual freelancers/micro; **₹999–₹1,999/mo** = small teams of 2–10 | Low-Medium | [evandsouza.com](https://evandsouza.com/articles/saas-pricing-strategies-for-indian-startups-a-comprehensive-framework/), [productgrowth.in](https://productgrowth.in/insights/saas/saas-pricing-rupee-vs-dollar/) |
| ₹999 is the standard "India tier" against ~$49 international | Common practice | Low-Medium | [playto.so](https://www.playto.so/blogs/how-to-price-your-saas-for-indian-vs-international-customers-in-2026) |
| WTP has genuinely risen since 2019 | GST compliance created mandatory software buying for millions | Low-Medium | [upgrowth.in](https://upgrowth.in/saas-pricing-packaging-strategy-india-gtm/) |
| **Compliance is the reliable unlock** | When software helps avoid a fine or rejection, payment resistance drops sharply (GST, TDS, labour docs have this property) | Low-Medium, but strategically important | [upgrowth.in](https://upgrowth.in/saas-pricing-packaging-strategy-india-gtm/) |

**Two consequences for this product:**

1. **₹999 sits above the freelancer band.** The plan's §3 primary ICP explicitly includes *freelancers*, but the plan's §30 price hypothesis (₹999) is priced for *teams of 2–10*. That is an internal inconsistency in the plan. Either the ICP narrows to small agencies, or the entry price drops to ₹399–₹499. **Flagged for a decision; see [pricing.md](pricing.md) §3.**
2. **This product has no compliance driver** — and the one thing that reliably loosens Indian SMB wallets is compliance. There is, however, an adjacent compliance fact arriving on a fixed date: **DPDP obligations bite by 13 May 2027** ([integrations.md](integrations.md) §3), and reactivation outreach to old contacts is exactly where consent gets murky. A possible later hypothesis (**H9**, added to [HYPOTHESES.md](../HYPOTHESES.md)): *"reactivate your old clients, with consent handled properly"* may sell better in India than reactivation alone.

---

## 6. Market sizing

**Not attempted.** No credible bottom-up figure for "Indian service businesses with 50–1,000 past clients who would pay for reactivation intelligence" could be sourced, and top-down "customer retention software market size" numbers on the open web come from the same class of vendor content as §3. Fabricating a TAM would violate plan §40 rule 13.

**What to do instead (EXPERIMENT):** size the beachhead by hand — count the reachable ICP the founder can actually contact in 90 days (his own agency client base, Coretex CRM users, local business networks, WhatsApp/LinkedIn reach). If that list is under ~200 businesses, distribution is the binding constraint, not market size. Record the real number here before Phase 5.

---

## 7. What the market evidence says to do next

1. **Do not build yet** — consistent with plan §47 Step 10. No customer-side evidence exists.
2. **The strongest available proof point is the founder's own dataset** (Phase 2), because every external number is contaminated.
3. **Run the concierge offer before the SaaS** (plan Phase 4) — because every proven buyer in this category is buying a *service*, not a *dashboard*.
4. **Price-test three points** (₹499 / ₹999 / ₹1,999), not one, given §5.
