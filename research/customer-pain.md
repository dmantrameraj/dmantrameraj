# Customer Pain Register

**Checked:** 2026-09-27
**Status:** ⚠️ **Desk research only. Zero customer interviews have been conducted. No customer pain in this file is validated.**

---

## 0. Honest statement against plan §47 Step 4

Plan §47 Step 4 asks for **"at least 10 concrete examples of customer pain."** This pass **did not deliver that**, and it is important not to pretend otherwise:

- **Reddit is inaccessible** to the research tooling (`reddit.com` is blocked to the search user agent), so the community-pain channel the plan relies on in §34 produced nothing. Manual protocol in [reddit-insights.md](reddit-insights.md).
- Generic searches for freelancers forgetting to follow up returned **newsletter and Gumroad marketing content**, not accounts of real pain — e.g. advice posts telling freelancers to "email every person who has bought from you", and "periodically contacting clients who have fallen off the radar reminds people you're available" ([thesimplefreelancer.substack.com](https://thesimplefreelancer.substack.com/p/a-timeline-of-my-newest-clients), [workspace.fiverr.com](https://workspace.fiverr.com/blog/4-keys-to-retaining-clients-as-a-freelancer), [getittogetheralready.substack.com](https://getittogetheralready.substack.com/p/dont-sleep-on-the-follow-up)). These are **prescriptions, not evidence** — somebody advising people to do X is weak evidence that people find not-doing-X painful.
- **Concrete pain examples can only come from interviews.** Anything else written here would be fabrication, which plan §40 rule 11 forbids.

**Count of genuinely concrete, first-person pain examples currently held: 1 (the founder's own).**
**Target before Gate A can be assessed: 10, from [customer-interview-guide.md](customer-interview-guide.md).**

---

## 1. Founder's own pain (first-party — the strongest evidence currently held)

**Evidence type: FACT (first-party, N=1).** Source: [`../PROJECT_PLAN.md`](../PROJECT_PLAN.md) §4, as stated by the founder.

| # | Pain | Notes |
|---|---|---|
| F1 | ~**30 clients/leads per month** may be forgotten for follow-up | The single most important number in the whole plan. Needs measuring, not recalling — see EXPERIMENT below |
| F2 | Context is split across WhatsApp, Gmail, Google Sheets, Coretex CRM, calendar, Razorpay, Shopify, forms | Matches the fragmentation thesis |
| F3 | Manual copying between systems: WhatsApp→Sheets, Gmail→CRM, forms→WhatsApp, Razorpay→Sheets, Shopify→Sheets | This is a *data plumbing* pain, arguably bigger than the *selection* pain |
| F4 | Remembering prior client conversations after a long gap | The "what do I even say" problem |
| F5 | Sending promised material; replying to clients; checking payments | Follow-through, not reactivation |
| F6 | Stated: if software told him which relationships need attention, he would use it | **Intent statement, not behaviour.** Weak by plan §14's own standard |
| F7 | Stated WTP ≈ ₹999/month | Founder's own number; see [pricing.md](pricing.md) |

**⚠️ Critical caveat the plan itself makes (§4): "These are founder observations, NOT market validation."** One person, who is also the builder, is the most biased possible sample. F6 in particular is the exact question plan §14 says never to ask.

**EXPERIMENT (do this in the next 30 days, it is cheap and decisive):**
Instead of trusting F1, **count it**. For 30 days keep a single running list: every time the founder realises he should have contacted someone earlier, log name, days since last contact, historical value, and whether he then contacted them. At the end:
- If the real number is ~30/month → F1 is FACT and the frequency case (Gate B) is strong for at least one user.
- If it is 3/month → the problem is real but **too infrequent to sustain a subscription**, and the product should be repositioned (see [evidence-against.md](evidence-against.md) §3).

This costs nothing, runs in parallel with Phase 2/3, and converts the plan's single most load-bearing number from memory into data.

---

## 2. Pain evidenced by revealed preference (third parties paying to solve it)

**Evidence type: FACT about the market, HYPOTHESIS about our ICP.** This is stronger than any survey, because money moved — but note **none of these buyers are our ICP**. They are franchises, enterprises and agencies' clients.

| # | Evidence | What pain it implies | Whose pain | Source |
|---|---|---|---|---|
| R1 | $5,000 deposits for humans to phone lapsed customers | "We know there is money in our lapsed list and we cannot work it ourselves" | Multi-location franchises | [WinbackEngine](https://www.winbackengine.com/) |
| R2 | $10,000 pilots to build one win-back cohort | Same, with an ROI guarantee demanded | Mid-market | [WinBack Labs](https://winbacklabs.com/programs-and-pricing/) |
| R3 | $33k–$120k/yr to be told when a past customer's circumstances changed | "Our old relationships are our best pipeline and we lose track of them" | B2B enterprise sales teams | [UserGems pricing](https://salesmotion.io/blog/usergems-pricing) |
| R4 | An entire GHL implementation industry around "database reactivation" | Agencies' clients have dormant databases they never work | SMB clients of agencies | [hlgrowthpartner.com](https://hlgrowthpartner.com/post/gohighlevel-database-reactivation-campaign-2026) |
| R5 | AINORA's headline: *"How much revenue is sitting dormant in your CRM?"* | The pain is recognisable with no explanation needed | SMB | [ainora.lt](https://ainora.lt/database-reactivation) |
| R6 | DealRecovery.ai's offer: a **free pipeline audit** as the lead magnet | Buyers will hand over CRM access to find out what they are missing | B2B | [dealrecovery.ai](https://dealrecovery.ai/) |

**R6 is directly actionable for us:** it validates the plan §32 fake-door shape. "Upload your old client list, get a free reactivation audit" is a lead magnet a competitor is already running successfully enough to build a site around.

---

## 3. Pain asserted by vendors (weak — recorded for completeness, not for decisions)

**Evidence type: ASSUMPTION.** All of these are vendors describing pain they sell against. Useful only as language to test in interviews, never as proof.

| # | Asserted pain | Source | Confidence |
|---|---|---|---|
| V1 | Businesses do not know how much revenue is dormant in their CRM | AINORA | Low |
| V2 | Teams cannot see relationships scattered across CRM, email, calendar, LinkedIn | [getboomerang.ai](https://www.getboomerang.ai/glossaries/relationship-intelligence-platforms-2026) | Low |
| V3 | Teams need reminding about dormant deals and leads, and drafting takes hours of manual review | [folk](https://www.folk.app/articles/crm-business-development) / folk AI articles | Low (a competitor's own framing — note they claim to have solved it) |
| V4 | Relationships "fade" without the owner noticing | Clay/Mesh | Low |
| V5 | Sales teams chase stale data and stale deals | Attio, Pipedrive Rotting | Low-Medium (the feature exists, so some demand does) |
| V6 | Dormant leads are cheaper to work than new ad spend | GHL DBR ecosystem, unanimously | Medium (consistent economic logic, and agencies sell it repeatedly) |

**V6 is the most transferable to the ICP** and the best interview probe: *"When you needed revenue this month, did you go to ads, referrals, or your old client list — and why?"*

---

## 4. The 10 pain hypotheses that must be tested (replacing the 10 examples we do not have)

Each is phrased so an interview can **falsify** it. Column "Evidence now" is deliberately brutal.

| # | Pain hypothesis | Evidence now | Falsified if an interview shows… |
|---|---|---|---|
| P1 | Service businesses have past clients with real commercial value who are no longer in contact | F1–F2 (N=1), R1–R5 (not our ICP) | Their past clients were one-off, low-value, or genuinely finished |
| P2 | They cannot easily tell **which** dormant contacts are worth contacting | none beyond N=1 | They can name their top 5 instantly from memory — very likely for a freelancer with 60 clients |
| P3 | They forget the prior context and that stops them reaching out | F4 | They remember fine; the blocker is awkwardness or time, not memory |
| P4 | The blocker is **not knowing what to say**, not lack of a reminder | plan §7 asserts it; no external evidence | They know what to say and simply do not get round to it (→ we are building an accountability tool, not intelligence) |
| P5 | It happens often enough to be worth a monthly subscription | F1 (unmeasured, self-reported) | The dormant list is exhausted in one or two sessions (→ one-off audit, not SaaS) |
| P6 | Their data exists in a usable form (services, values, last project) | **Contradicted by the ICP definition itself** — the plan says they use "spreadsheets, Gmail or WhatsApp" | Their sheet has name, phone and nothing else (→ see [evidence-against.md](evidence-against.md) §2, the biggest kill risk) |
| P7 | Current workarounds (memory, sheets, CRM filters, reminders) are painful enough to switch | none | They already use Pipedrive Rotting / a HubSpot filter / a monthly manual sheet review and are content |
| P8 | They trust AI enough to read their client history and revenue data | none | They refuse to upload a client list to an unknown vendor — plausible and must be asked directly |
| P9 | They would act on the recommendation, not just look at it | none; and R1–R2 suggest buyers prefer **done-for-you** | They say "nice list" and send nothing (→ Phase 4 is the real test) |
| P10 | They would pay ~₹999/mo | F7 (founder only); market says ₹999 is the **team** tier not the freelancer tier | They anchor at ₹299–₹499, or want commission-based pricing |

**Gate A (plan §38) is assessed on P1–P4 being described by real customers *without being led*.** None can be assessed today.

---

## 5. Interview targets

Per plan §14: 10–20 people from the ICP. Recruiting list to build (fill in as you go):

| Segment | Target count | Source of introductions | Recruited | Interviewed |
|---|---|---|---|---|
| Solo freelancers (design/dev/marketing) | 4–6 | founder's network, local groups | 0 | 0 |
| Small digital marketing agencies (2–10) | 4–6 | agency peers, Coretex users | 0 | 0 |
| Consultants / coaches | 2–4 | LinkedIn | 0 | 0 |
| Local service businesses (B2B-ish) | 2–4 | existing clients | 0 | 0 |
| **Total** | **12–20** | | **0** | **0** |

Script, screener and scoring: [customer-interview-guide.md](customer-interview-guide.md). Log every interview into [customer-interviews.md](customer-interviews.md) — **never summarise from memory, and never fill a row that did not happen.**
