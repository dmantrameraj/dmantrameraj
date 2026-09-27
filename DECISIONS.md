# Decision Log

Format per [PROJECT_PLAN.md](PROJECT_PLAN.md) §41. Every major product decision gets an entry.
**Last updated:** 2026-09-27

| ID | Decision | Date | Status |
|---|---|---|---|
| D-001 | Focus on dormant client reactivation | 2026-09-27 | Hypothesis |
| D-002 | Do not build the SaaS yet — Phase 1 first | 2026-09-27 | Decided |
| D-003 | Never use third-party reactivation statistics | 2026-09-27 | Decided |
| D-004 | Test three price points, not ₹999 alone | 2026-09-27 | Proposed |
| D-005 | Narrow V0 to paid past clients only | 2026-09-27 | Proposed |
| D-006 | Promote Coretex, demote Gmail in integration order | 2026-09-27 | Proposed |
| D-007 | V0 does not send messages, in any channel | 2026-09-27 | Decided |
| D-008 | Recommended wedge: "the service you never sold them" | 2026-09-27 | Proposed |
| D-009 | Run field-fill measurement before any other Phase 2 work | 2026-09-27 | Decided |
| D-010 | Sell the concierge audit before building the SaaS | 2026-09-27 | Proposed |
| D-011 | Research files stay in this repo despite unrelated app code | 2026-09-27 | Decided |

---

## D-001 — Focus on dormant client reactivation

**Date:** 2026-09-27
**Status:** Hypothesis

**Reason:** Founder pain (plan §4) plus market evidence of a real, priced problem.

**Evidence:**
- WinbackEngine: $5,000 deposit, 3× ROI guarantee, human agents calling lapsed customers — [GlobeNewswire, 2026-03-26](https://www.globenewswire.com/news-release/2026/03/26/3263235/0/en/LTVplus-Launches-WinbackEngine-A-Performance-Based-Customer-Reactivation-Service-for-Multi-Location-Franchises.html)
- WinBack Labs: $10,000 pilot, 5× ROI guarantee — https://winbacklabs.com/programs-and-pricing/
- UserGems: $33k–$120k/yr for past-customer/champion signals — https://salesmotion.io/blog/usergems-pricing
- "Database reactivation" is a standard GoHighLevel agency playbook with a whole implementation industry — https://hlgrowthpartner.com/post/gohighlevel-database-reactivation-campaign-2026

**Still needs:** Customer validation. Every priced buyer above is a franchise, an enterprise, or an agency's client — **none is our stated ICP**. Zero interviews conducted.

---

## D-002 — Do not build the SaaS yet

**Date:** 2026-09-27
**Status:** Decided (per plan §47 Step 10, §38)

**Reason:** Gates A–G are unassessed. The three decisive questions (does the data exist, is folk already good enough, is the post-sale wedge real) are answerable in ~3 weeks with no code.

**What was built instead:** the Phase 1 research set, the Phase 2 dataset protocol, and the Phase 3 interview guide.

**Reversal condition:** Phase 2 CONTINUE + ≥10 interviews scoring Gates A–E, before any application code.

---

## D-003 — Never use third-party reactivation statistics

**Date:** 2026-09-27
**Status:** Decided

**Reason:** The available "benchmarks" range from **<5% to 40%** for the same claim — an 8× spread — and every source is a vendor or affiliate. The only figure describing a concrete measurable outcome (GHL's "2–8% reply rate") is both the lowest and refers only to a reply, not a sale.

**Evidence:** [market.md](research/market.md) §3, eight mutually inconsistent claims with sources.

**Consequence:** no win-back percentage, ROI multiple or LTV claim appears in the landing page, pricing model, or any customer conversation. The only numbers we use will be our own measured results. This strengthens plan §31's "do not claim guaranteed revenue" into **"do not claim any rate at all."**

---

## D-004 — Test three price points, not ₹999 alone

**Date:** 2026-09-27
**Status:** Proposed (needs founder approval)

**Reason:** The plan is internally inconsistent: §3 names **freelancers** as the primary ICP; §30 hypothesises **₹999/month**, which market convention places in the **2–10 person team** band (freelancers sit at ₹299–499).

**Evidence:** [pricing.md](research/pricing.md) §2–3. Indian SMB WTP 60–70% below Western; Zoho CRM Standard ₹800/user, **Bigin ₹400** for a full CRM; Clay free to 1,000 contacts.

**Decision:** Free / **Solo ₹499** / **Studio ₹1,499** / **one-off Audit ₹9,999–24,999**, all ex-GST, with ₹999-single-tier as the A/B control.

**Still needs:** PX-1 landing test and PX-2 concierge offer.

---

## D-005 — Narrow V0 to paid past clients only

**Date:** 2026-09-27
**Status:** Proposed

**Reason:** Restricting V0 to contacts who **paid at least once** and whose project is **complete or lapsed** guarantees `total_value > 0` and a `last_project` exists — the exact data the intelligence layer needs and which is most often missing. It also lands the product squarely in the one unoccupied square (post-sale × commercial reasoning) instead of the squares where free tools already sit.

**Excluded from V0:** never-converted leads, active clients, e-commerce buyers, networking contacts.

**Evidence:** [opportunity-gaps.md](research/opportunity-gaps.md) §2–3, [evidence-against.md](research/evidence-against.md) §2.

**Cost:** narrower than plan §3's ICP. Accepted deliberately.

---

## D-006 — Promote Coretex, demote Gmail in the integration order

**Date:** 2026-09-27
**Status:** Proposed (changes plan §21)

**Reason:** Three independent reasons converge.
1. Gmail needs **restricted OAuth scopes** ⇒ a **CASA audit by a Google-authorised lab, re-validated annually**, costing roughly **$500–$4,500/yr** ([Google docs](https://developers.google.com/identity/protocols/oauth2/production-readiness/restricted-scope-verification), [Google Cloud support](https://support.google.com/cloud/answer/13465431?hl=en), [deepstrike.io](https://deepstrike.io/blog/google-casa-security-assessment-2025)). At a $1,500 mid-estimate that is ≈₹1.32L ≈ **22 customers' full annual revenue at ₹499/mo, every year, for one integration.**
2. Coretex users are the only population **guaranteed** to hold the structured commercial history the thesis needs.
3. Coretex supplies warm, trusting users — answering both the trust objection and the distribution problem.

**New order:** CSV → Google Sheets → **Coretex CRM** → Calendar → Razorpay → **Gmail** → WhatsApp → Shopify.

**Note:** this is *not* a decision to merge Coretex and this product (plan §22 rightly defers that). It is a decision about which data source to read first.

**Still needs:** verify whether the non-restricted `gmail.metadata` scope suffices — if it does, Gmail may be cheap after all.

---

## D-007 — V0 does not send messages, in any channel

**Date:** 2026-09-27
**Status:** Decided

**Reason:** Not a philosophical choice — a policy and deliverability one.
- **WhatsApp:** marketing templates must go only to **opted-in contacts who engaged recently** (India ₹1.09/msg); from **1 Oct 2026** service messages become billable after 1,000/number/month. Our output is by definition people who have *not* engaged in 120+ days. ([aisensy.com](https://aisensy.com/pricing), [engagelab.com](https://www.engagelab.com/blog/whatsapp-business-api-pricing))
- **Email:** sunset practice stops at 90–180 days; abandoned mailboxes become **recycled spam traps**; dormant addresses damage whole-domain reputation. ([Spamhaus](https://www.spamhaus.org/resource-hub/deliverability/what-is-an-email-sunset-policy-and-why-do-you-need-one/))

**Decision:** V0 produces copy-to-clipboard text the user sends themselves, from their own account. No bulk sending, ever. This matches plan §20 and the founder's actual current workflow.

**Bonus:** the constraint is also the sharpest differentiator against the GHL bulk-drip incumbent — *"blasting your dormant list costs you your domain; these eight are worth a personal message."*

---

## D-008 — Recommended wedge: "the service you never sold them"

**Date:** 2026-09-27
**Status:** Proposed (plan §47 Step 7 deliverable)

**Reason:** *"Find the old clients worth reconnecting with"* is already Clay's and Circle Connect's sentence at free-to-$12/month, and it invites the reply *"I know who my old clients are."* The defensible object is the **intersection** — dormant × already paid × discussed-but-never-bought — which nobody can hold in their head, is **checkable against the user's own file so the AI cannot fabricate it**, is inherently revenue-weighted, and sits in the one square incumbents left empty.

**Evidence:** [opportunity-gaps.md](research/opportunity-gaps.md) §1–3, [competitors.md](research/competitors.md) comparison matrix.

**Honest caveat:** the wedge is a *combination*, not an invention. Every individual capability is commodity. Defensibility comes from focus, data source, price and trust — **not technology**.

**Still needs:** Phase 2 Metric 13 (does `previous_interest` exist in real data), interview Q22–Q24, landing A/B.

---

## D-009 — Run field-fill measurement before any other Phase 2 work

**Date:** 2026-09-27
**Status:** Decided

**Reason:** The highest-probability failure mode is that the ICP's files **do not contain** `total_value`, `previous_services` or `previous_interest`, in which case the AI can only ever output "124 days since contact" — the reminder plan §7 rejects and Pipedrive gives away free.

**Test:** measure fill rate across the §9 schema on the founder's real export. **Kill threshold: <40%** for `total_value` AND (`previous_services` OR `previous_interest`).

**Cost:** about an hour. **It can end the project before any other work is done, which is the point.**

**Evidence:** [evidence-against.md](research/evidence-against.md) §2, [founder-data-test.md](research/founder-data-test.md) Step 1.

---

## D-010 — Sell the concierge audit before building the SaaS

**Date:** 2026-09-27
**Status:** Proposed

**Reason:** Every buyer discovered paying real money for this problem is buying a **service with guaranteed outcomes**, not a dashboard: $5,000 deposits, $10,000 pilots, done-for-you calling and texting, AI calling agents. Nobody was found paying meaningfully to *be told* who to contact. A dashboard hands the hard part back to the person who already failed to do it.

**Decision:** offer a **₹9,999–24,999 "dormant client revenue audit"** (cleaned data, ranked opportunities, 20 written messages, a walkthrough call) to 10 ICP businesses. Zero paid takers = the thesis reflects the founder's preferences, not the market's. It also funds the build and produces the only trustworthy outcome data we will ever have.

**Evidence:** [evidence-against.md](research/evidence-against.md) §4; [customer-pain.md](research/customer-pain.md) §2 R1–R6; DealRecovery.ai already runs a free-audit lead magnet.

---

## D-011 — Research files stay in this repo despite unrelated app code

**Date:** 2026-09-27
**Status:** Decided (low-stakes, revisit freely)

**Reason:** This repository (`dmantrameraj/dmantrameraj`) currently contains an unrelated Vite/React app ("Imaginom", an AI poster designer). The plan specifies root-level `HYPOTHESES.md`, `DECISIONS.md` and `/research/*`, and the plan is the source of truth, so those paths were followed exactly. The existing app was left completely untouched.

**Recommendation:** when Phase 5 starts, move this work to a dedicated repository. Mixing a poster app and a CRM-intelligence product in one repo will get confusing the moment there is code.

---

## Template for new entries

```md
## D-0NN — <decision>

**Date:** YYYY-MM-DD
**Status:** Hypothesis / Proposed / Decided / Reversed

**Reason:**

**Evidence:**
- <source URL> — checked YYYY-MM-DD — confidence

**Cost / what we give up:**

**Still needs:**

**Reversal condition:**
```
