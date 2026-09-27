# Hypotheses

**Product:** Dormant Client Reactivation / Revenue Recovery Intelligence (working concept)
**Plan:** [PROJECT_PLAN.md](PROJECT_PLAN.md) §42
**Last updated:** 2026-09-27 (first research pass)

States: `Validated` · `Invalidated` · `Partially validated` · `Still unknown`
Evidence labels per plan §36: **FACT** / **HYPOTHESIS** / **ASSUMPTION** / **DECISION** / **EXPERIMENT**

> ⚠️ **No hypothesis below is validated by customer evidence. Zero interviews have been conducted.** Where a status reads "Partially validated", it is validated by *market* evidence (someone else's customers paying money) — never by ours.

---

## H1 — Small service businesses have valuable dormant client relationships

**Status:** Partially validated (market), Still unknown (our ICP)
**For:** Businesses pay $5,000 deposits (WinbackEngine), $10,000 pilots (WinBack Labs) and $33k–$120k/yr (UserGems) specifically to work lapsed relationships; "database reactivation" is a standardised GoHighLevel agency playbook with an entire implementation industry around it. → [market.md](research/market.md) §1
**Against:** Every priced buyer found is a franchise, an enterprise or an agency's client — **not a solo freelancer or a 3-person agency**. Nothing establishes that a freelancer's 60 past clients contain recoverable value.
**Next test:** Phase 2 Metrics 1, 3, 4 ([founder-data-test.md](research/founder-data-test.md)).

---

## H2 — They do not systematically identify which dormant relationships are worth reconnecting with

**Status:** Still unknown — **and at real risk**
**For:** Pipedrive Rotting and HubSpot filters detect *inactivity* with no ranking or reason; GHL DBR blasts the whole segment without selecting. Nobody in the affordable tier ranks by commercial value. → [competitors.md](research/competitors.md)
**Against:** A freelancer with 60 lifetime clients may simply **know** their best five. If so this is a problem of scale the ICP does not have. ([customer-pain.md](research/customer-pain.md) P2)
**Next test:** Interview Q23 — *can they list them from memory?* Plus Q20 screen-share timing.

---

## H3 — The reason/context for reactivation is more valuable than a simple reminder

**Status:** Still unknown — **the differentiation depends entirely on this**
**For:** UserGems' whole $33k+/yr business is "the reason it is warm now". DealRecovery.ai sells signals-with-reasons. Enterprise pays for the *why*.
**Against:** folk already ships "relationship briefs" and AI-drafted follow-ups from $24/seat; Circle Connect's AVIS claims to tell you "who to talk to, when, and **why**". The gap may be quality, not existence — a weak place to compete. → [competitors.md](research/competitors.md), [evidence-against.md](research/evidence-against.md) §1
**Next test:** 14-day folk trial + Circle Connect install on 50 real past clients. **Do this before writing code.**

---

## H4 — Users want AI to prepare the recommendation and message, but want human approval before sending

**Status:** Partially validated — but for an uncomfortable reason
**For:** Independently **necessary**, not just preferred: WhatsApp marketing templates require opt-in from recently-engaged contacts (India ₹1.09/msg), and Spamhaus-grade email practice says stop mailing addresses dormant 90–180 days because they become spam traps. Automated bulk sending to this exact list is unsafe. → [integrations.md](research/integrations.md) §4–5
**Against:** Every buyer paying real money in this category is buying **done-for-you outreach** ($5k–$10k engagements, AI calling agents). Human-approval-only may be the safe design *and* the commercially weak one. → [evidence-against.md](research/evidence-against.md) §4, §6
**Next test:** Interview Q29 — do they want the list, or do they want it done?

---

## H5 — CSV/Google Sheet input is enough to demonstrate initial value

**Status:** 🔴 **At serious risk — the biggest single threat to the product**
**For:** Zero integration cost, zero policy surface, universal.
**Against:** The thesis needs `total_value`, `previous_services`, `previous_interest`, `project_status`. The ICP is defined as people using "spreadsheets, Gmail or WhatsApp" — precisely the people whose sheet has name, phone and maybe a date. Without those fields the output degrades to *"124 days since contact"*, which Pipedrive gives away free. Also: **CSV import is table stakes** — folk, Attio and Clay all have it, so it differentiates nothing. → [evidence-against.md](research/evidence-against.md) §2
**Next test:** **Phase 2 Step 1 field-fill measurement. Kill threshold: <40%.** Run this before anything else.

---

## H6 — Users may pay around ₹999/month

**Status:** Still unknown — **and the plan is internally inconsistent here**
**For:** ₹999 is the conventional Indian "India tier" for a ~$49 international product.
**Against:** Market convention places **₹299–499** at freelancers and **₹999–1,999** at teams of 2–10 — so ₹999 does not match the plan's own primary ICP (freelancers, §3). Indian SMB WTP runs 60–70% below Western markets and is benchmarked against a junior salary (₹15–25k/mo). Zoho Standard is ₹800 and **Bigin is ₹400** for a whole CRM. Clay is free to 1,000 contacts. And this product has **no compliance driver** — the one factor shown to reliably raise Indian SMB WTP. → [pricing.md](research/pricing.md) §2–3
**Next test:** PX-1 (₹499/₹1,499 vs ₹999 landing test), PX-2 (₹9,999 concierge audit offered to 10 businesses), interview Q18–Q19 + Q29.

---

## H7 — Post-sale client reactivation is a stronger wedge than generic lead follow-up

**Status:** Partially validated — **the strongest finding of this pass**
**For:** Every affordable tool is either pre-sale (folk, Attio, Pipedrive, DealRecovery.ai = closed-lost pipeline) or relationship-social (Clay, Dex, Circle). **Finished, paid, satisfied clients are nobody's object below enterprise price.** The post-sale × commercial-reasoning square is occupied only by UserGems ($33k+/yr) and $5k–10k human services. → [opportunity-gaps.md](research/opportunity-gaps.md) §2
**Against:** Vendor-published decay curves (Low confidence) claim win-back success falls from ~40% at 30 days to <5% after 180 — implying the *long*-dormant end, which is exactly our target, is the low-yield end. → [evidence-against.md](research/evidence-against.md) §5
**Next test:** Phase 2 Metric 12 (dormancy distribution of the genuinely-worthwhile set) and Metric 13 (unsold-service hit rate).

---

## H8 — Coretex CRM can eventually become a strong data source/integration

**Status:** Partially validated on logic — **and should be promoted in priority**
**For:** Three independent reasons converge: (a) Coretex users are the only population **guaranteed** to have the structured commercial history H5 says is otherwise missing; (b) Gmail — the plan's current #2 integration — requires an annual CASA audit costing **$500–$4,500/yr**, roughly 22 customers' annual revenue at ₹499/mo, forever; (c) Coretex supplies warm, trusting users, answering both the trust objection and the distribution problem. → [opportunity-gaps.md](research/opportunity-gaps.md) §3, [integrations.md](research/integrations.md) §1–2
**Against:** Coretex's install base may be too small to validate anything; a captive audience is also a biased one.
**Next test:** count Coretex accounts with ≥50 past clients and populated value/service fields. If that number is ≥20, it is the beachhead.

---

## H9 — 🆕 Consent-aware reactivation sells better in India than reactivation alone

**Status:** Still unknown (new hypothesis from this pass)
**Reasoning:** The research finding that Indian SMB payment resistance *collapses when software prevents a fine or rejection* (GST, TDS being the precedents) is the strongest WTP lever found — and this product has no such driver as specified. But **India's DPDP consent, notice and security provisions become effective 13 May 2027**, and contacting long-dormant contacts whose consent predates the Act is exactly the grey area a reactivation product creates. A product that tracks `consent_source`, flags contacts that cannot lawfully be marketed to, and produces the notice/withdrawal mechanics would carry a compliance reason to be bought. → [integrations.md](research/integrations.md) §3, [pricing.md](research/pricing.md) §2
**Against:** May be premature — SMB urgency about DPDP is likely low until enforcement starts; could dilute a clear message.
**Next test:** add one interview question — *"Has anyone asked you about DPDP or data consent for your client list?"* Cheap to ask, and the answers will be honest.

---

## H10 — 🆕 The valuable object is "the service you never sold them", not "the client you forgot"

**Status:** Still unknown (new hypothesis — the recommended positioning)
**Reasoning:** *"Old clients worth reconnecting with"* is already Clay's and Circle Connect's sentence, at free-to-$12/month, and it invites *"I know who my old clients are."* *"Which past client discussed a service and never bought it, ranked by what they already paid you"* is (a) an intersection nobody can hold in their head, (b) **checkable against the user's own file, so the AI cannot fabricate it**, (c) inherently revenue-weighted, and (d) in the one square incumbents have left empty. → [opportunity-gaps.md](research/opportunity-gaps.md) §3
**Against:** Requires `previous_interest` to exist in real data — the same field H5 flags as likely missing. May also read as an accusation of past failure.
**Next test:** Phase 2 Metric 13 (does the data support it at all), then interview Q22–Q24 (does the framing land), then landing-page variant A/B vs the incumbent framing D.

---

## Summary

| ID | Hypothesis | Status | Biggest threat |
|---|---|---|---|
| H1 | Dormant relationships hold value | Partially validated (market) | No evidence at solo/small scale |
| H2 | They can't systematically identify them | Still unknown | They may just remember |
| H3 | Reason > reminder | Still unknown | folk/Circle may already do it |
| H4 | AI prepares, human approves | Partially validated | Buyers want it *done* |
| H5 | CSV/Sheet input is enough | 🔴 At serious risk | The needed fields aren't in the files |
| H6 | ₹999/month | Still unknown | Wrong tier for the stated ICP |
| H7 | Post-sale is the stronger wedge | Partially validated ⭐ | Value may decay before 120 days |
| H8 | Coretex as data source | Partially validated ⭐ | Install base size |
| H9 | Consent-aware angle (new) | Still unknown | Premature |
| H10 | "Unsold service" framing (new) | Still unknown ⭐ | Depends on H5's data |

**The three that decide everything: H5 (does the data exist), H3 (is folk already good enough), H7/H10 (is the post-sale wedge real).** All three are answerable in ~3 weeks with the founder's own data, two competitor trials, and ten conversations — **with no code written.**
