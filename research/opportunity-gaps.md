# Opportunity Gaps & The Recommended Wedge

**Checked:** 2026-09-27
Answers plan §16 (validate each assumed gap), §47 Step 6 (comparison — see [competitors.md](competitors.md)) and **Step 7 (identify the strongest defensible wedge)**.

---

## 1. The plan's assumed gaps, tested

Plan §16 lists candidate gaps and says *"Do not assume these are gaps. Validate each one."* Here is the verdict from this pass. **"Validated" means evidence supports it; it does not mean it is a gap customers will pay to close.**

| Assumed gap (plan §16) | Verdict | Evidence |
|---|---|---|
| Too much CRM complexity | **Partly validated** | folk/Attio are full CRMs with pipelines, objects, seats, workflows; the ICP wants a list, not a system. But Clay/Dex are already simple — so simplicity alone is taken |
| Requires manual data entry | **Validated as a real burden** | Clay, folk, Attio all auto-ingest from email/calendar/LinkedIn; the *commercial* fields (value, services quoted, project status) are entered by hand everywhere. Nobody auto-derives those |
| Focuses on active leads | **Validated — the clearest structural gap** | folk's dormancy language attaches to *deals and leads*; Pipedrive Rotting is per-pipeline-stage; DealRecovery.ai is *closed-lost*. **Finished, paid, happy clients are nobody's object** |
| Generic follow-up reminders | **Validated** | Pipedrive: days idle, no reason. Dex: time-based. Clay: "relationship fading" |
| Poor historical relationship understanding | **Partly refuted** | Clay and folk build real interaction timelines. What they lack is *commercial* history, not history |
| Weak explanation of WHY to contact | **Partly refuted — be careful here** | folk ships "relationship briefs"; Circle Connect's AVIS claims "who to talk to, when, and **why**"; UserGems and DealRecovery.ai give an explicit external reason. The gap is not "no why" — it is **"no why derived from money you already exchanged"** |
| Weak post-sale reactivation | **Validated — strongest gap found** | Every tool in tiers A–C is pre-sale (pipeline) or relationship-social. Post-sale reactivation exists only in tier D at $33k+/yr or $5k+ engagements |
| Too much automation / spam risk | **Validated, and defensible** | GHL DBR is a 3–5 message bulk drip; Spamhaus says dormant-list sending damages domain reputation. A deliberately small, hand-sent list is a real and evidence-backed counter-position |
| Expensive for solo operators | **Validated** | folk $24–30/seat (≈₹2,100+), Attio $29, UserGems $2,750/mo. Nothing tier-D-shaped exists near ₹999 |
| Requires switching CRM | **Validated** | DealRecovery.ai needs CRM OAuth; folk/Attio need you to live in them |
| No simple CSV/Sheet entry | **Refuted** | folk, Attio, Clay all import CSV. CSV import is table stakes, **not a differentiator** |
| Poor India-friendly pricing | **Validated** | All competitor pricing found is USD; no India tier discovered for any of them |
| No clear revenue-recovery workflow | **Validated for the SMB tier** | The workflow exists at enterprise (UserGems) and as a human service ($5k–10k). Not as affordable software |

**Two of the plan's assumed gaps are refuted (CSV import, "no why") and one is partly refuted (historical understanding).** Those three should stop appearing in positioning and pitch material.

---

## 2. Where the real hole is

Combining the tier map in [competitors.md](competitors.md) §0 with the table above:

```
                    Reasons over CONTACT RECENCY        Reasons over MONEY ALREADY EXCHANGED
                    ────────────────────────────        ───────────────────────────────────────
  Pre-sale          Pipedrive Rotting (free)            folk / Attio AI          ($24–69/seat)
  (open pipeline)   HubSpot filters (free)              DealRecovery.ai          (price unknown)

  Relationship      Clay/Mesh (free–$20)                — nothing —
  (network)         Dex (~$12), Circle apps

  POST-SALE         — nothing —                         UserGems ($33k–120k/yr)
  (finished,                                            WinbackEngine ($5k dep.)
  paid clients)                                         WinBack Labs ($10k)
                                                        ▲
                                                        │
                                              ◄── THE HOLE: this reasoning,
                                                  for a 2-person agency,
                                                  at ₹999/month
```

**The hole is not a missing capability. It is a missing price point for an enterprise-proven capability, applied to a data source nobody else looks at: the user's own invoices, completed projects, and services they quoted but never sold.**

That framing matters because it tells you what is defensible (focus, data source, price, trust) and what is not (the AI, the dormancy detection, the message drafting — all commodity).

---

## 3. 🎯 The recommended wedge (plan §47 Step 7)

### The wedge, in one sentence

> **The unsold-service list: for each past client who already paid you, the one service you discussed-or-should-have and never sold — with the reason, ranked by what they already spent.**

### Why this specific framing, and not the plan's current framing

The plan's working positioning is *"find the old clients worth reconnecting with"* (§5, §43 Option B). The research says that phrasing loses, for three reasons:

1. **"Old clients worth reconnecting with" is Clay's and Circle Connect's sentence already** — at free and ~$12/month. We would be arguing about quality in a demo, on their turf.
2. It describes a **list of people**, which invites the reply *"I know who my old clients are."* Interview hypothesis **P2** is a genuine risk: a freelancer with 60 clients can name their top five from memory.
3. It is **revenue-blind in the wording**, which is exactly the thing the plan's own §7 says is the whole point.

Whereas *"the service you never sold them"*:

- **Names an object the user cannot hold in their head.** They know *who* their clients are; they do **not** know the intersection of *"who is dormant" × "what we discussed that never happened" × "what they already spent"* across 200 rows. That intersection is the only genuinely hard cognitive task in the workflow — and the only one worth software.
- **Is checkable, so it cannot be fabricated.** Every recommendation points at a fact already in the user's own file: an invoice paid, a project marked complete, a service in `previous_interest` with no matching `last_project`. This satisfies plan §26 guardrails by construction — the AI is *retrieving* a reason, not *inventing* one.
- **Is inherently revenue-weighted.** "₹35,000 paid, Google Ads discussed, never sold" carries its own business case. No opportunity score needed to justify the click.
- **Sits in the validated hole** (post-sale × commercial reasoning) rather than the contested squares.
- **Survives the "I could do this in HubSpot" objection.** A HubSpot filter finds *"last engagement > 12 months, no deals"*. It cannot find *"paid for a website, we quoted Ads in the thread, never bought"*.
- **Reframes "dormant" from a problem into an asset**, which matters for a market whose own decay statistics (see [evidence-against.md](evidence-against.md) §5) work against the resurrection story.

### Positioning candidates to test (replacing plan §43's five)

| | Line | Tests |
|---|---|---|
| **A** (recommended) | **"You already sold them once. Here's what you never sold them."** | The unsold-service wedge |
| **B** | **"₹4.2 lakh of your past clients never bought the second thing."** | Quantified, uses the user's own numbers — strongest if the data supports it |
| **C** | "Don't blast your old list. These eight are worth a real message." | The anti-spam / deliverability counter-position |
| **D** | "Your old clients are your next leads." (plan §18) | Keep as control — it is the incumbent framing |

Test A/B/C against D in the plan §31 landing-page test. **Do not finalise before interviews** (plan §17, §43).

### Scope discipline this wedge implies

**In V0:** past clients who **paid at least once** and whose project is **complete or lapsed**. Nothing else.
**Out of V0:** never-converted leads, active clients, e-commerce buyers, networking contacts. Those are the squares where free tools already sit.

This is narrower than plan §3's ICP, deliberately: it guarantees `total_value > 0` and a `last_project` exists, which is exactly the data the intelligence layer needs and [evidence-against.md](evidence-against.md) §2 warns is usually missing.

### What makes it defensible (honestly — and it is not the AI)

| Layer | Defensibility | Note |
|---|---|---|
| Dormancy detection | **None** | free in Pipedrive/HubSpot |
| Message drafting | **None** | any LLM; folk ships it |
| Opportunity scoring | **Weak** | folk has AI scoring |
| **Reasoning over the user's own commercial history** | **Moderate** | requires a schema and product focus incumbents have chosen not to build |
| **Post-sale focus + ₹-priced + no migration** | **Moderate** | a positioning moat, not a technical one |
| **Coretex CRM as a first-party structured source** | **Strongest asset the founder has** | see below |
| Trust/distribution via the founder's agency + Coretex users | **Moderate** | the only viable channel given §10 of evidence-against |

### The Coretex insight — promote it

Plan §21 orders integrations Sheets → Gmail → Calendar → **Coretex (4th)**. The research says **move Coretex to first or second**:

1. The single biggest kill risk is **missing commercial data** ([evidence-against.md](evidence-against.md) §2). Coretex CRM users *already have structured client history* — the one population where the intelligence layer is guaranteed to have inputs.
2. Gmail is the most expensive integration in the plan: restricted scopes ⇒ **CASA audit, ~$500–$4,500, re-validated annually** ⇒ roughly 11+ customers' annual revenue at ₹999, every year ([integrations.md](integrations.md) §2).
3. Coretex gives a warm, trusting install base — the answer to the trust problem (P8) and the distribution problem.
4. Plan §22 says the merge decision comes after validation. Agreed — but **validate on Coretex data first**, which is not the same as merging the products.

---

## 4. The one-line product definition this wedge produces

> Upload or connect your past-client list. For every client who already paid you and has gone quiet, it finds the service you discussed but never delivered, explains the reason in one line you can verify, ranks them by what they already spent, and drafts a message you approve before it sends.

Compare against the plan's §5 promise — same spirit, but every clause is checkable against the user's own file, and none of it claims to predict intent.

---

## 5. Open questions this file cannot answer

1. Do ICP files actually contain "quoted but not sold" information anywhere? (**Phase 2 field-fill measurement — do this first.**)
2. Will users accept "the service you never sold them" as a *positive* frame, or does it read as an accusation of failure? (**Interview + landing-page test.**)
3. Is the unsold-service list big enough per user per month to justify a subscription? ([evidence-against.md](evidence-against.md) §3.)
4. Does Circle Connect's AVIS already do commercial reasoning? (**Install it.**)
5. Does folk's AI Assistant already produce an acceptable "why" on a completed project? (**14-day trial.**)

Until 1, 4 and 5 are answered, **no code.** (Plan §47 Step 10.)
