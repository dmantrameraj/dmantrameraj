# Evidence Against The Thesis (Anti-Bias File)

**Checked:** 2026-09-27
**Mandate:** plan §37 — *"Claude must actively search for evidence that the idea is BAD."* and §49 — *"Do not fall in love with the idea."*

This file answers one question: **what would prove this product is unnecessary?**
Ten risks below, ordered by how likely each is to kill the product. Each has a falsification test.

---

## 1. It is a feature of things people already own, not a product

**Evidence:**
- **Pipedrive "Rotting"**: per-stage `Rotting in (days)` toggle, red/green pipeline flags, filterable by owner/stage/age — shipping, free inside the CRM. ([official KB](https://support.pipedrive.com/en/article/the-rotting-feature), High confidence)
- **HubSpot**: a dormant-client list is **two advanced filters** — *"Last engagement date is more than 12 months ago"* + *"Number of associated deals is none"*. Five minutes of work, on a free-tier-capable platform. ([source](https://pipelinedecoded.com/blog/inactive-crm-contacts/), Medium-High)
- **folk** already markets AI Assistants that *"proactively suggest next actions, draft follow-ups, provide relationship briefs… reminding teams about dormant deals or leads"*, plus AI scoring and personalised-email generation across contact groups, from $24/seat/mo. ([source](https://lightfield.app/blog/folk-crm-pricing), Medium)
- **Clay/Mesh** nudges when relationships fade, with per-group cadence, from **free**. ([source](https://clay.earth/), Medium)

**Why it is serious:** three of the product's six promised outputs (detect dormant, score, draft message) are already in shipping products, one of them free. The remaining differentiation is *the quality of the "why"* — a subjective claim that is hard to demo and easy for an incumbent to copy in a sprint.

**Falsification test:** run the 14-day folk trial and the free Clay tier on 50 real past clients. If either produces a "why" the founder judges good enough to act on, **the differentiation is dead as specified** and the product must move to a different axis (data depth, India price, or done-for-you).

---

## 2. 🔴 The data the thesis needs probably does not exist in the ICP's files

**This is the highest-probability killer, and the plan contains the contradiction internally.**

- Plan §9 requires `total_value`, `last_project`, `previous_services`, `previous_interest`, `project_status`, `last_conversation_summary`, `pending_action` for the intelligence to be more than a reminder.
- Plan §3 defines the ICP as businesses that *"use spreadsheets, CRM, Gmail or WhatsApp"* — and plan §9 itself concedes *"Do not require users to have perfect CRM data."*
- Plan §7's own worked example (₹35,000 paid, project complete, Google Ads previously discussed) is only possible **because those four facts were recorded**. In a typical freelancer's sheet, they are not.

**Consequence if true:** with only `name`, `phone`, `last_contact_date`, the AI can output nothing better than *"124 days since contact"* — which is precisely the reminder plan §7 says is worthless, and which Pipedrive gives away free.

**Falsification test — run it first, it is the cheapest decisive test in the whole plan:**
Before anything else in Phase 2, take the founder's **real** client sheet/CRM export and measure **field fill rate** across the §9 schema. Record it in [founder-data-test.md](founder-data-test.md).
- If `total_value` + (`previous_services` or `previous_interest`) are present for **<40%** of contacts → the intelligence layer has nothing to reason over. Either the product must *extract* that context (from Gmail/WhatsApp threads — a far harder product with CASA costs, see [integrations.md](integrations.md)), or it must *ask the user 3 questions per contact* (which is data entry, the thing they hate), or the thesis fails.
- **A product whose value depends on data its ICP does not keep is not a product.**

---

## 3. Frequency may be too low to sustain a subscription

**Evidence:** the ICP is defined as having **50–1,000 historical contacts** (plan §3). Take the low-middle: a freelancer with 150 lifetime contacts, of whom maybe 40 are dormant-with-value. The product surfaces them **once**. After that first session, the monthly supply of *newly* dormant contacts is a function of how many clients finish projects each month — for a solo operator, perhaps 1–3.

**Why it is serious:** this is the classic **audit-tool trap**. High first-session value, near-zero month-2 value, churn after the first or second bill. The founder's own ₹999/mo hypothesis assumes recurring value that the arithmetic may not support at the small end of the ICP.

The plan's own §29 activation metric ("contacts at least 3 relevant dormant relationships in the first session") measures the *first* session — it does not test month 3, which is where the business lives.

**Falsification tests:**
1. In Phase 2, after processing the founder's 50 contacts, ask: **how many new ones would qualify next month?** If <5, the subscription premise is weak.
2. Add a retention metric to plan §29: **"qualified new opportunities surfaced per user in month 2 and month 3."**
3. Pricing consequence: if supply is lumpy, the honest model may be **one-off audit + optional low retainer**, or annual-only, not monthly SaaS.

---

## 4. The proven buyers in this category buy a service, not software

**Evidence (all Medium-High, all revealed preference):**
- WinbackEngine: **$5,000 deposit**, 3× ROI guarantee, **trained human agents phone** the lapsed customers. ([GlobeNewswire](https://www.globenewswire.com/news-release/2026/03/26/3263235/0/en/LTVplus-Launches-WinbackEngine-A-Performance-Based-Customer-Reactivation-Service-for-Multi-Location-Franchises.html))
- WinBack Labs: **$10,000 pilot**, 5× ROI guarantee, built and handed over. ([source](https://winbacklabs.com/programs-and-pricing/))
- AINORA: **done-for-you** calling/texting of the dormant database. ([source](https://ainora.lt/database-reactivation))
- "AI reactivation agents" sell **outbound calling**, not dashboards. ([source](https://www.petegabi.com/blog/best-ai-reactivation-agents-lost-customers/))

**Why it is serious:** every buyer willing to pay real money for this problem is paying for **the outreach being done and outcomes guaranteed**. Nobody discovered in this pass pays meaningfully for *being told who to contact*. A dashboard hands the hard part — the awkward message, the follow-through — back to the person who already failed to do it. Plan §20 then *mandates* human approval, which makes the product structurally unable to do the part buyers pay for.

**This is not fatal — it redirects.** It is a strong argument that the plan's **Phase 4 concierge is the business**, and the SaaS is at best the delivery tool for it. A defensible sequence: sell a ₹10,000–25,000 one-off "dormant client revenue audit + 20 drafted messages" to 5 real businesses. If they buy that, the SaaS has a proven demand curve behind it. If they will not buy a done-for-you version at 10× the SaaS price, they will not buy the SaaS.

**Falsification test:** offer the concierge audit to 10 ICP businesses. **Zero paid takers = the thesis is about the founder's preferences, not the market's.**

---

## 5. Reactivation value decays fast — and this product targets the decayed end

**Evidence (Low confidence source, high strategic importance):** a widely-repeated benchmark shape claims win-back success of **~40% at 30 days, 25% at 60, 12% at 90, and under 5% after 180 days** ([opensend.com](https://www.opensend.com/post/win-back-campaign-success-rate-statistics), vendor content).

**Why it matters even though the source is weak:** the plan's hero example is **124 days dormant**, and the ICP's "forgotten" clients will often be 6–24 months cold. If the decay shape is even directionally right, the product is aimed at the flattest part of the curve, while the highest-value intervention is at **30–60 days** — which is not "dormant client reactivation" at all, it is **ordinary follow-up discipline**, a crowded market the plan §2 explicitly refuses to enter.

**The uncomfortable possibility:** the valuable product may be the boring one the plan rules out (never let a live relationship go cold), and the exciting one (resurrect the long-dead) may be the low-yield half.

**Falsification test:** in Phase 2, bucket the founder's 50 contacts by dormancy (0–90 / 91–180 / 181–365 / 365+ days) and judge *reactivation-worthiness per bucket*. If almost all the genuinely worthwhile ones are under 120 days, **reposition toward early intervention** and say so in [DECISIONS.md](../DECISIONS.md).

---

## 6. The send step is legally and technically constrained — in both channels

**WhatsApp (High-ish confidence, Medium sources):** marketing template messages must go only to **opted-in contacts who engaged recently**; Meta re-categorises mixed content (e.g. an update with a discount) as **marketing**; India marketing rate **₹1.09/message**. From **1 Oct 2026**, service messages become billable after 1,000 free per number per month. ([aisensy.com](https://aisensy.com/pricing), [engagelab.com](https://www.engagelab.com/blog/whatsapp-business-api-pricing), [blueticks.co](https://blueticks.co/blog/whatsapp-business-pricing-marketing-messages-2026))

→ A dormant client from 2023 who never gave WhatsApp marketing opt-in **cannot be legitimately messaged** through the API. The founder's own workflow uses WhatsApp heavily; the product's most natural channel is its most restricted.

**Email (High confidence — Spamhaus):** industry practice is to **stop** emailing addresses dormant 90–180 days; abandoned mailboxes get **recycled into spam traps**; dormant addresses damage whole-domain reputation. ([Spamhaus](https://www.spamhaus.org/resource-hub/deliverability/what-is-an-email-sunset-policy-and-why-do-you-need-one/))

→ The product's output list is, by construction, a list email professionals would suppress.

**Why it is serious:** the value chain ends at *"send the message"*, and both channels resist it. The product can only ever be a **drafting assistant for one-to-one, human-sent messages** — which is the right and safe design (plan §20), but it caps perceived value versus tools that promise automation.

**Mitigation that is also a differentiator:** make the constraint the pitch (see [market.md](market.md) §4) — *don't blast your dormant list, it costs you your domain; send eight good messages instead.* Also: prefer the channel where the relationship already exists (a reply in an existing WhatsApp thread is a service window, not a marketing template).

---

## 7. Compliance and integration costs are real money for a solo founder

| Item | Cost / obligation | Confidence | Source |
|---|---|---|---|
| Gmail restricted scopes | **CASA audit by a Google-approved lab, revalidated annually**; ~**$500–$4,500** depending on tier (some report $540 DAST → $5,000+ pen test) | Medium-High on the requirement (official Google pages), Medium on cost | [Google restricted-scope verification](https://developers.google.com/identity/protocols/oauth2/production-readiness/restricted-scope-verification), [Google Cloud support](https://support.google.com/cloud/answer/13465431?hl=en), [deepstrike.io](https://deepstrike.io/blog/google-casa-security-assessment-2025) |
| India DPDP | Consent/notice/security provisions effective **13 May 2027**; consent must be free, specific, informed, unconditional, unambiguous; withdrawal one-click; pre-Act data usable only if a compliant notice is issued | Medium-High | [Fisher Phillips](https://www.fisherphillips.com/en/insights/insights/indias-new-data-privacy-rules-are-here), [Wikipedia: DPDP Rules 2025](https://en.wikipedia.org/wiki/Digital_Personal_Data_Protection_Rules,_2025) |

**Arithmetic that matters:** a $1,500/yr CASA audit ≈ ₹1.32L (at the assumed ₹88/USD) ≈ **11 customers' entire annual revenue at ₹999/mo**, for one integration, every year. Gmail is therefore **not** a V1 feature at this price point — it is a feature that requires ~100+ paying customers to be rational.

**Consequence:** the plan's §21 integration order (Sheets → Gmail → Calendar → Coretex) should be re-ordered to put **Coretex CRM before Gmail** — Coretex is the founder's own system, costs nothing in audits, and its users already have structured commercial history (the exact data §2 above says is missing elsewhere).

---

## 8. Price is squeezed from both sides

- Indian SMB WTP runs **60–70% below Western markets**; SMBs compare software to a junior salary (**₹15,000–25,000/mo**); **₹299–499** is the freelancer band and **₹999–1,999** the small-team band. ([upgrowth.in](https://upgrowth.in/saas-pricing-packaging-strategy-india-gtm/), [evandsouza.com](https://evandsouza.com/articles/saas-pricing-strategies-for-indian-startups-a-comprehensive-framework/), Low-Medium)
- Meanwhile the **free/cheap** end is occupied: Clay free up to 1,000 contacts, HubSpot free-tier filters, Pipedrive Rotting bundled, GHL DBR already paid for by any agency.
- And **compliance**, the one factor that reliably raises Indian SMB WTP, does not apply to this product as specified.

**Consequence:** ₹999/mo to a solo freelancer is a hard sell against free alternatives; ₹999 to a 2–10 person agency is plausible **but that agency already has GoHighLevel and knows how to run a DBR campaign.**

---

## 9. Trust: the product asks for the most sensitive file in the business

The upload is a list of clients, phone numbers, deal values and conversation notes — arguably the single most commercially sensitive artefact a small agency owns, handed to an unbranded new SaaS. The plan §23 takes privacy seriously, which is right, but no amount of policy text substitutes for brand trust at signup.

**Falsification test:** ask it directly in interviews (P8): *"Would you upload your client list with revenue figures to a new tool from a company you'd never heard of? What would have to be true first?"* If most say no, the go-to-market must run **through Coretex's existing trust** or through a **concierge NDA engagement**, not self-serve signup.

---

## 10. Distribution: the category's search surface is owned by content farms

Nearly every result across a dozen searches in this pass was an affiliate/SEO review site, a GHL implementation agency, or a vendor blog (folk's own comparison articles, "best X in 2026" pages, `syncgtm.com`, `softwarefinder.com`, `capterra`, `vendr`, and a long tail of GHL snapshot sellers).

**Consequence:** organic and paid acquisition for "dormant client reactivation" and "personal CRM" keywords is expensive and dominated by well-funded content operations. A solo founder cannot win that channel. Distribution must come from **the founder's own assets** — his agency's client base, Coretex CRM users, his network, and direct outreach — which caps early scale and makes the beachhead count in [market.md](market.md) §6 the real constraint.

---

## Summary: what would make us stop

| If this turns out true | Then |
|---|---|
| Field fill rate for value/services is **<40%** on the founder's own real data (§2) | **Stop.** The intelligence layer has no inputs. Rethink as data-capture, or as a Coretex-only feature |
| Fewer than **5** new qualified opportunities per month after the first sweep (§3) | Not a subscription. Sell as a one-off audit or annual |
| **Zero** paid takers for a ₹10–25k concierge audit out of 10 offers (§4) | **Stop.** The market prefers no solution to this solution |
| Almost all worthwhile reactivations are **<120 days** dormant (§5) | Reposition to early-stage follow-up; drop "dormant/revival" framing |
| folk or free Clay produces a "why" the founder would act on (§1) | Differentiation is dead as specified; compete on data depth + India price, or don't compete |
| Interviewees can name their top 5 dormant clients from memory in 30 seconds (P2) | The selection problem is not real at ICP scale. The real problem is doing the outreach — build for that instead |

**None of these can be assessed today.** All six are answerable within ~3 weeks using the founder's own data and 10 conversations, with no code written.
