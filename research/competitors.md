# Competitor Research

**Checked:** 2026-09-27
**Method:** web search evidence only — vendor pricing pages were blocked by this environment's network policy (see [README.md](README.md) §⚠️). All prices are **Medium confidence at best** until verified on the official page.
**Currency:** ASSUMPTION ≈₹88/USD where converted.

---

## 0. The map: four tiers, and where the gap actually is

The category is not one market. It splits by **price** and by **what the tool reasons over**:

| Tier | Price | Reasons over | Examples | Reactivation reasoning? |
|---|---|---|---|---|
| **A. Personal relationship CRM** | Free–$49/seat/mo | *Contact recency* + social/news signals | Clay/Mesh, Dex, Circle Connect, Circle CRM | Nudges when a relationship "fades" — **revenue-blind** |
| **B. SMB / startup CRM with AI** | $24–$69/seat/mo | *Open pipeline* | folk, Attio, Pipedrive, HubSpot | Flags idle **deals**, not finished **clients** |
| **C. Campaign playbook (agency)** | Included in GHL sub | *A dormant segment, in bulk* | GoHighLevel DBR, MoEngage, Klaviyo-type | Blasts the whole list with one message |
| **D. Signal-based reactivation** | $33k–$120k/yr, or $5k–$10k/engagement | *Old relationships + changed external circumstances* | UserGems, DealRecovery.ai, WinbackEngine, WinBack Labs, AINORA | **Yes — and validated by real spend** |

**The structural finding:** the reasoning the plan describes in §7 ("124 days + ₹35,000 + project complete + previously discussed Google Ads → reactivation opportunity") **only exists in Tier D, and Tier D starts at ~$33,000/year or a $5,000 engagement deposit.** Tier A does the nudge without the money. Tier B does the money without the finished clients. Tier C does the outreach without the selection.

Nothing found in this pass sells Tier-D *reasoning* at Tier-A *prices* to a service business with 50–1,000 past clients. That is the gap — and it is also the reason to be suspicious (see [evidence-against.md](evidence-against.md) §4: at Tier D the buyers pay for **done-for-you outcomes**, not a dashboard).

---

## TIER A — Personal relationship CRMs (closest on "who should I contact", furthest on "why, commercially")

### Clay / clay.earth (rebranding to **Mesh**)

**Source:** https://clay.earth/ · https://www.toolsforhumans.ai/ai-tools/clay · https://muncly.com/clay-earth-review-is-this-an-end-game-personal-crm/
**Checked:** 2026-09-27

**Finding:** Aggregates contacts automatically from email, calendar, LinkedIn and social, builds a searchable history, and **"nudges you when relationships start to fade"** with per-group cadences (close contacts monthly, weak ties quarterly). Has an "Automatic Reconnect" feature that surfaces a few random people for serendipity. Shows career moves, news mentions and life updates.

**Pricing:** Personal free (up to 1,000 contacts); Pro $20/mo (listed at $10/mo discounted); Team $49/seat/mo ($40 discounted); Enterprise custom. ≈₹1,760/mo for Pro at the assumed rate.

**Reactivation capability:** Recency-based nudge, yes. Commercial reasoning (historical value, services bought, quoted-but-unsold, project status) — **no evidence of any**.

**Why this matters to us:** This is the product a skeptic will say already does it. The honest difference: Clay answers *"you're losing touch with this person"*; the plan's product must answer *"this person paid you ₹35,000, the project is done, you quoted Ads and never sold it."* If we cannot hold that line in a demo, we are a worse Clay at a similar price.

**Confidence:** Medium (features consistent across 3 sources; pricing not verified on official page; the Mesh rebrand means details may be stale).

---

### Dex (getdex.com)

**Source:** https://getdex.com/ · https://getdex.com/pricing/ (fetch blocked) · https://www.capterra.com/p/275020/Dex/
**Checked:** 2026-09-27

**Finding:** Positioned exactly as *"reminds you to keep in touch with people you would otherwise forget."* LinkedIn + email + iCloud/social integrations, mobile/desktop/Chrome apps. Student/MBA discounts.

**Pricing:** ~$12/mo billed annually (≈₹1,056/mo), ~40% saving vs monthly.

**Reactivation capability:** Time-based keep-in-touch reminders. No commercial reasoning found.

**Confidence:** Medium-Low (official pricing page inaccessible; $12 figure appears in third-party summaries only).

---

### Circle Connect / Circle AI / Circle CRM (three separate apps, the plan conflated them)

**Source:** https://apps.apple.com/in/app/circle-connect/id6476190388 · https://apps.apple.com/us/app/circle-ai/id6743581221 · https://circlecrm.app/ · https://withincircle.com/ai-personal-crm
**Checked:** 2026-09-27

**Finding:** The plan §15 lists "Circle Connect" as a known competitor. There are at least **four distinct "Circle" products**, and the plan should stop treating them as one:
- **Circle Connect** — business relationship app with **"AVIS, an AI Relationship Assistant that tells you who to talk to, when, and why"**, organised as a daily agenda. This is the single closest positioning match found to the plan's §5 "WHO / WHY / WHY NOW".
- **Circle AI** — consumer/social: outreach suggestions, smart reminders, gift ideas, streaks, a **"Warmth Score"**.
- **Circle CRM** — *"circle back to people before relationships go cold… who's heating up, cooling off, and needs your attention."*
- **Circle (software)** — unrelated community platform (Wikipedia entry); don't confuse it in notes.

**Pricing:** Not established in this pass. **Unverified.**

**Reactivation capability:** Claimed "who / when / why" — but these are App Store marketing descriptions, and there is no evidence the "why" is derived from commercial history rather than elapsed time.

**Why this matters:** Circle Connect's marketing copy is nearly identical to the plan's intended positioning. **Action: install Circle Connect and Circle CRM and use them on 20 real contacts before writing a single line of product code.** If AVIS already produces a usable "why now", the differentiation collapses to data depth and India pricing.

**Confidence:** Medium on existence/positioning, Low on capability (vendor copy only), Unverified on price.

---

## TIER B — SMB/startup CRMs with AI

### folk

**Source:** https://lightfield.app/blog/folk-crm-pricing · https://efficient.app/apps/folk · https://www.folk.app/articles/crm-with-ai-follow-up-assistant
**Checked:** 2026-09-27

**Finding:** Contacts, companies, pipelines, notes, reminders, email/calendar context, enrichment, outreach, AI. **AI Assistants "proactively suggest next actions, draft follow-ups, and provide relationship briefs… reminding teams about dormant deals or leads."** "Magic Fields" = an AI prompt as a custom field type (can generate a personalised email across a group of contacts). Also AI-based scoring and classification.

**Pricing (as of Aug 2026 per source):** Standard $30/member/mo ($24 annual); Premium $60 ($48); Enterprise from $100 ($80). 14-day trial. Standard ≈₹2,112/mo — **2.1× the plan's ₹999 hypothesis, per seat.**

**Reactivation capability:** This is the most dangerous competitor on paper: *dormant* + *relationship brief* + *drafted follow-up* + *AI scoring* is four of our six promised outputs, already shipping.

**The gap to probe (not yet validated):** folk's dormancy language attaches to **deals and leads** (open pipeline), and the drafting is a generic AI field, not reasoning over *paid invoices, completed projects and quoted-but-unsold services*. **Unverified** — must be tested in a trial.

**Confidence:** Medium (pricing from 2 aggregators + vendor's own article; not verified on folk's pricing page).

---

### Attio

**Source:** https://attio.com/ · https://www.coffee.ai/articles/attio-crm-pricing-2026 · https://www.stacksync.com/blog/attio-crm-2025-review-features-pros-cons-pricing
**Checked:** 2026-09-27

**Finding:** Positions as "the CRM for agentic revenue". AI attributes (fields that auto-fill via a web-research agent), an agent layer that researches prospects and runs as workflow steps, and natural-language actions ("move all deals from Acme to closed-lost and log a note").

**Pricing:** Free (up to 3 seats); Plus $29/user/mo annual; Pro $69; Enterprise custom. Monthly ≈24% premium. **Hybrid model: seats + usage credits** for enrichment/AI/workflow runs.

**Reactivation capability:** Strong general agents, no reactivation-specific product. Aimed at startup revenue teams, not solo service businesses.

**Note for our own architecture:** Attio's seats+credits model is the honest answer to AI cost pass-through, and worth copying in structure (see [pricing.md](pricing.md) §4).

**Confidence:** Medium.

---

### Pipedrive — "Rotting" (the strongest "it already exists" argument)

**Source:** https://support.pipedrive.com/en/article/the-rotting-feature (official KB, via search) · https://solvaa.co.uk/how-to-use-the-pipedrive-rotting-feature-to-track-deal-inactivity-and-boost-conversions/
**Checked:** 2026-09-27

**Finding:** A toggle per pipeline stage: *"Rotting in (days)"*. Deals not updated within the threshold are flagged; pipeline colour-codes green (has scheduled activity) vs red (idle, no upcoming task); rotting deals can be filtered by owner, stage and age.

**Reactivation capability:** Detects **inactivity** on **open deals**, with zero explanation and zero commercial weighting. Exactly the "reminder, not intelligence" the plan §7 rejects — **but it ships free inside a CRM the ICP may already pay for.**

**Confidence:** High (official knowledge base content).

---

### HubSpot

**Source:** https://community.hubspot.com/t5/Dashboards-Reporting/Creating-a-report-on-deals-that-have-been-inactive-for-X-days/m-p/539872 · https://pipelinedecoded.com/blog/inactive-crm-contacts/
**Checked:** 2026-09-27

**Finding:** Inactive-deal visual indicators in the deal board (Board actions → Edit cards). Inactive **contact** segments are buildable today with advanced filters: *"Last engagement date is more than 12 months ago"* + *"Number of associated deals is none."*

**Why this matters:** A competent HubSpot user can build our core list view **in about five minutes with two filters**. Our value therefore cannot be *finding* dormant contacts. It has to be the **ranking + the reason + the draft**.

**Confidence:** Medium-High (community + practitioner sources; mechanism is well-known).

---

## TIER C — The incumbent playbook in the founder's own market

### GoHighLevel "Database Reactivation" (DBR)

**Source:** https://hlgrowthpartner.com/post/gohighlevel-database-reactivation-campaign-2026 · https://automatetogrow.com/database-reactivation-win-back-dormant-leads/ · https://ghlcrm.me/gohighlevel-database-reactivation/ · https://hiregohighleveldeveloper.com/blog/database-reactivation-campaign-gohighlevel/
**Checked:** 2026-09-27

**Finding:** DBR is **not a product — it is the standard agency playbook**, and it is what a digital marketing agency in this ICP already knows how to do:
1. a smart list / tag defining the dormant segment (typically **no meaningful activity for 90+ days**),
2. a GHL Workflow dripping **3–5 SMS-led, email-supported messages over ~a week**,
3. an if/else that pulls anyone who replies out of the sequence,
4. handoff to a booking calendar + pipeline stage.

The stated goal is **not to sell in the message — the goal is a reply**, then a human or Conversation AI qualifies in 2–3 exchanges and pushes to a booking link. Marketed to agencies as the fastest way to put booked calls on a client's calendar in week one, before spending an ad rupee.

**Claimed results:** "typically 2–8% reply rate" on a cleaned list, "$10K in 48 hours", "booked jobs in 7–14 days". **These are agency marketing claims on affiliate/SEO pages — Low confidence, treat as unverified.**

**Why this is the most important competitor in the file:** It is free-ish (inside a GHL subscription), it is already in the founder's own professional vocabulary, and it solves the *action* end. Its weakness is precisely the plan's thesis: **it blasts the entire dormant segment with one message and does not decide who is worth contacting or why.** That is both our opening and our biggest commercial threat — an agency can run DBR today with no new tool.

**Confidence:** Medium on mechanics (consistent across 4+ independent sources), Low on all percentage claims.

---

### E-commerce lifecycle platforms (adjacent, not V0)

**Source:** https://www.moengage.com/customer-lifecycle/reactivate/ · https://porchgroupmedia.com/blog/email-reactivation-strategies-to-win-back-dormant-customers/ · https://www.nutshell.com/engagement/resources/5-ways-recapture-inactive-customers
**Checked:** 2026-09-27

**Finding:** MoEngage-class platforms detect **cohorts** going dormant and trigger omnichannel campaigns pre-emptively; Bloomreach-class combine a real-time CDP with omnichannel execution. Standard practice: start within 30–90 days of inactivity and segment by dormancy depth (1–2 months = gentle nudge, 6+ months = stronger incentive).

**Relevance:** Confirms the plan's §3 decision to keep e-commerce out of V0 — this tier is cohort/campaign-shaped, not relationship-shaped, and it is well served.

**Confidence:** Medium.

---

## TIER D — Where the plan's actual thesis is already proven (and expensive)

### UserGems — proof the wedge is worth real money

**Source:** https://salesmotion.io/blog/usergems-pricing · https://syncgtm.com/blog/usergems-review · https://pipeline.zoominfo.com/sales/usergems-review
**Checked:** 2026-09-27

**Finding:** Tracks **past champions and past customers** and surfaces them as warm leads when their circumstances change (job change, promotion, new hires at target accounts, buying-group changes). Claims past champions who moved companies convert at **3× normal lead rates** and new hires are **2.5× more likely to buy in their first 90 days** (vendor claims — Low confidence). Now 30+ signal types.

**Pricing:** Core **$2,750/mo ($33,000/yr)**, Advanced $5,750/mo ($69,000/yr), Elite $10,000/mo ($120,000/yr), plus ~$3,000 implementation.

**Why this is the single most useful competitor finding:** It establishes that *"an old relationship plus a changed circumstance equals warm revenue"* is a proposition enterprises pay **₹29 lakh–₹1 crore a year** for. The thesis is not crazy. What is unproven is whether the **same reasoning, applied to 200 past clients of a two-person agency, is worth ₹999/month** — a ~1,000× price gap and a completely different data environment (they have Salesforce + LinkedIn + enrichment; our ICP has a messy Google Sheet).

**Confidence:** Medium on price (two independent sources agree on the tiers), Low on the conversion multiples.

---

### DealRecovery.ai — the closest direct competitor found

**Source:** https://dealrecovery.ai/ · https://dealrecovery.ai/resources/guides/abandoned-opportunity-recovery/ · https://dealrecovery.ai/resources/signals/competitor-stumble-signal-reactivation/
**Checked:** 2026-09-27

**Finding:** *"Find hidden revenue in your CRM."* Connects to the CRM by **read-only OAuth**, runs a **nightly scan**, claims **100+ data points**, and surfaces **stale prospects worth re-engaging at the right time** with personalised outreach reps can send in seconds. Monitors re-engagement signals: funding changes, hiring, leadership change, competitor stumbles. Offers a free "pipeline audit".

**Pricing:** Not published. **Unverified.**

**Assessment:** This is the plan's product, built for **B2B closed-lost pipeline** rather than **completed service projects**, using **external company signals** rather than **the founder's own commercial history**. The read-only-OAuth + nightly-scan + free-audit shape is a strong pattern to copy. Their focus on external signals is also their limit for our ICP: a ₹35,000 website client in Nagpur has no funding round to detect.

**Confidence:** Medium (vendor site content, consistent across several of their own pages).

---

### Done-for-you reactivation services — the revealed-preference evidence

| Service | Model | Price | Source |
|---|---|---|---|
| **WinbackEngine** (LTVplus) | Trained **human agents phone** lapsed customers for multi-location franchises (fitness, dental, med spa) | **$5,000 deposit**, 3× ROI guarantee, refundable if missed | GlobeNewswire release, 2026-03-26 |
| **WinBack Labs** | 2-month build for one high-potential cohort, handed over as an owned asset | **$10,000 pilot**, 5× ROI guarantee | winbacklabs.com/programs-and-pricing |
| **AINORA** | Done-for-you: calls and texts dormant leads/past customers in your CRM to re-book appointments | Not published | ainora.lt/database-reactivation |
| **"AI reactivation agents"** (e.g. Olivia) | High-volume outbound **calling**, intent qualification, CRM updates, win-back incentives | Not published | petegabi.com/blog/best-ai-reactivation-agents-lost-customers/ |

**Finding (FACT):** Multiple businesses charge **$5,000–$10,000 per engagement**, with ROI guarantees, purely to reactivate a client's dormant database. Their headline is *"How much revenue is sitting dormant in your CRM?"* (AINORA).

**The two readings, and both are important:**
1. **Supportive** — real money changes hands for this exact problem. It is not a founder fantasy.
2. **Damaging** — every one of these is **human-delivered and outcome-priced**, and the offer is *"we will do it"*, not *"here is a dashboard."* See [evidence-against.md](evidence-against.md) §4. This is the strongest argument for the plan's own Phase 4 concierge step.

**Sources:** https://www.globenewswire.com/news-release/2026/03/26/3263235/0/en/LTVplus-Launches-WinbackEngine-A-Performance-Based-Customer-Reactivation-Service-for-Multi-Location-Franchises.html · https://winbacklabs.com/programs-and-pricing/ · https://ainora.lt/database-reactivation · https://www.winbackengine.com/
**Confidence:** Medium-High on the offer structures (press release + vendor pricing pages), Low on any outcome claim.

---

## Adjacent / watch list

| Product | Relevance | Source | Confidence |
|---|---|---|---|
| **SigParser** | Scans email history to uncover hidden contacts and *"rediscover past clients / re-engage dormant relationships"* — closest thing found to "Gmail in, dormant relationships out" | sigparser.com | Low-Medium (vendor copy) |
| **Common Room / Unify / Champify** | Signal-based selling for B2B. Useful guardrail language, quoted below | commonroom.io, coldiq.com/blog/common-room-vs-unify | Medium |
| **Nutshell** | Publishes re-engagement guidance for inactive customers; SMB CRM | nutshell.com | Medium |
| **Octavius.ai, CartBoss, voxwise, ATJ, Construction Snapshot** | Content-marketing operations around "customer reactivation"; indicates a crowded SEO surface, see [evidence-against.md](evidence-against.md) §10 | various | Low |

### One line worth pinning to the product's guardrails

> "A buying signal is an observed change that may affect fit, timing, or relevance. **It is not proof that a named person wants a sales message.**"
> — Common Room, https://www.commonroom.io/blog/signal-based-selling-definition/ (checked 2026-09-27)

That is the most defensible framing found for plan §26, and it is a competitor saying it. Our opportunity score must be presented as **an observed change, never as intent**.

---

## Comparison matrix (plan §47 Step 6)

Scoring: ● = clearly does it · ◐ = partial / adjacent · ○ = no evidence · ? = unverified

| | Price entry | Reasons over commercial history | Explains *why now* | Ranks by revenue potential | Drafts message | Post-sale (finished clients) | CSV/Sheet in, no migration | Human-approval default | Fits ₹999/mo solo India |
|---|---|---|---|---|---|---|---|---|---|
| **Clay / Mesh** | Free / $20 | ○ | ◐ (recency + news) | ○ | ◐ | ◐ | ◐ | ● | ◐ |
| **Dex** | ~$12 | ○ | ○ (time only) | ○ | ◐ | ◐ | ◐ | ● | ◐ |
| **Circle Connect** | ? | ? | ◐ claimed ("who/when/why") | ? | ● claimed | ◐ | ? | ● | ? |
| **folk** | $24/seat | ◐ | ◐ (dormant deals/leads) | ◐ (AI scoring) | ● | ○ (pipeline-shaped) | ● | ● | ○ |
| **Attio** | Free / $29 | ◐ | ◐ | ◐ | ● | ○ | ● | ● | ○ |
| **Pipedrive (Rotting)** | in CRM | ○ | ○ (days idle) | ○ | ○ | ○ | ● | ● | ◐ |
| **HubSpot filters** | Free tier | ○ | ○ | ○ | ○ | ◐ | ● | ● | ● |
| **GHL DBR playbook** | in GHL sub | ○ | ○ (segment only) | ○ | ● (one template for all) | ● | ● | ○ (bulk drip) | ◐ |
| **DealRecovery.ai** | ? | ◐ (CRM + external signals) | ● | ● | ● | ○ (closed-lost) | ○ (CRM OAuth) | ● | ? |
| **UserGems** | $2,750/mo | ● | ● | ● | ● | ● | ○ | ● | ○ |
| **WinbackEngine / Labs** | $5k–$10k | ● (human) | ● | ● | n/a (they call) | ● | ● | n/a | ○ |
| **→ Proposed product** | ₹999 target | **must be ●** | **must be ●** | **must be ●** | ● | **●** | **●** | **●** | **●** |

**Read the bottom row honestly:** the only cells where the proposed product is unoccupied by an incumbent are the **combination** of commercial-history reasoning + post-sale focus + no-migration input + solo-India price. Each individual capability is taken. **The wedge is a combination, not an invention** — which means it is defensible on focus and price, not on technology. See [opportunity-gaps.md](opportunity-gaps.md).

---

## What this file still needs (do not skip before building)

1. Verify every price on the vendor's own pricing page; upgrade confidence, update dates.
2. **Run a 14-day folk trial** with 50 of the founder's real past clients. Record verbatim what its AI Assistant says about a completed-and-paid project. This single test can invalidate the differentiation.
3. **Install Circle Connect + Circle CRM**; judge whether AVIS's "why" is commercial or temporal.
4. Request the DealRecovery.ai free pipeline audit; capture their output format and their pricing.
5. Find pricing for Circle Connect, DealRecovery.ai, AINORA.
6. Search G2/Capterra reviews for *complaints* about folk/Attio/Clay dormancy features — the plan §15 asks for customer complaints and reviews, and none were captured in this pass.
