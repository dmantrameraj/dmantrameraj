# Integration Research — Real Cost, Policy and Sequence

**Checked:** 2026-09-27
Answers plan §21 (integration priority) and §23 (privacy/security investigation before Gmail/WhatsApp).

---

## 1. Recommended sequence (changed from plan §21)

| Order | Integration | Why here | Blocking cost |
|---|---|---|---|
| **1** | **CSV upload** | Zero cost, zero policy surface, works for everyone. Table stakes — every competitor has it, so it buys no differentiation, only access | none |
| **2** | **Google Sheets** | Easiest real onboarding; non-restricted scopes; the ICP already lives there | low |
| **3** | **Coretex CRM** ⬆ *promoted from 4th* | **The only data source guaranteed to hold the commercial fields the whole thesis depends on** (see [evidence-against.md](evidence-against.md) §2), plus a warm, trusting install base. No audit cost | founder-controlled |
| **4** | Google Calendar | Meeting history/timing; non-restricted in its read-only form (verify scope class) | low |
| **5** | Razorpay | Payment history = `total_value` and `payment_status`, the highest-signal commercial fields | API review only |
| **6** | **Gmail** ⬇ *demoted from 2nd* | Richest context, **most expensive integration in the plan**: restricted scopes ⇒ annual CASA audit. Defer until ~100+ paying customers | **$500–$4,500/yr, recurring** |
| **7** | WhatsApp Business API | Powerful but opt-in-constrained for exactly our use case | per-message + BSP fees |
| **8** | Shopify | Only if the e-commerce use case is pursued (plan §3 says not in V0) | low |

**The one structural change:** Coretex up, Gmail down. Justification in [opportunity-gaps.md](opportunity-gaps.md) §3 and [pricing.md](pricing.md) §4.

---

## 2. Gmail — the expensive one

**FACT (Medium-High confidence, official Google sources):**
- Apps using **restricted scopes** (Gmail, Drive) in production must pass a **CASA** (Cloud Application Security Assessment) carried out by a **Google-authorised third-party lab**, and must **re-validate annually**.
- CASA uses a risk-based, multi-tiered approach; apps are assigned assurance level **AL1 or AL2** based on user count, requested scopes and other signals.
- Authorised labs issue a **Letter of Validation** to Google.

Sources: [Google restricted-scope verification](https://developers.google.com/identity/protocols/oauth2/production-readiness/restricted-scope-verification) · [Google Cloud support: Security Assessment](https://support.google.com/cloud/answer/13465431?hl=en)

**Cost (Medium confidence — third-party reports, varies by lab and tier):** roughly **$500–$4,500**; one report describes the spread as a **$540 DAST scan** at the low end to a **$5,000+ penetration test** at the high end. Source: [deepstrike.io](https://deepstrike.io/blog/google-casa-security-assessment-2025)

**Consequence at our price point:** a mid-estimate $1,500/yr ≈ **₹1.32L** ≈ **~22 customers' entire annual revenue at ₹499/mo, every single year, for one integration.**

**Practical mitigations (to verify before committing):**
1. Check whether the **non-restricted** `gmail.metadata` scope class (headers/labels, no message bodies) is sufficient for our reasoning. If "who did I last exchange email with, and when" is enough, we may avoid restricted scopes entirely. **⚠️ Unverified — confirm the current scope classification directly in Google's docs.**
2. Let the **user paste or forward** the relevant thread instead of granting inbox access. Ugly, cheap, and privacy-friendly.
3. Use **Google Sheets + Calendar + Razorpay + Coretex** as the data spine and treat Gmail as a premium add-on funded by scale.

---

## 3. India DPDP — a fixed deadline, and a possible wedge

**FACT (Medium-High confidence, multiple independent sources incl. a law firm):**

| Date | What happens |
|---|---|
| 13 Nov 2025 | Data Protection Board established; administrative provisions in force |
| 13 Nov 2026 | Consent-manager registration opens |
| **13 May 2027** | **Consent, privacy-notice and security provisions become effective** (end of the ~18-month implementation phase) |

Requirements that bear directly on this product:
- Standalone, plain-language **privacy notice before consent**, itemising data categories, purposes, rights procedures and complaint mechanisms; available in English and any of the 22 official Indian languages.
- Consent must be **free, specific, informed, unconditional and unambiguous**. Prohibited: pre-checked boxes, prominent-accept/hidden-reject, consent walls, bundled consent, confusing language.
- **Withdrawal must be as easy as granting** — a one-click digital process.
- Data collected **before** the Act may continue to be processed **only if a compliant notice is issued** to those data principals; historical consent that does not meet the standard is a risk to remediate.

Sources: [Fisher Phillips](https://www.fisherphillips.com/en/insights/insights/indias-new-data-privacy-rules-are-here) · [Wikipedia: Digital Personal Data Protection Rules, 2025](https://en.wikipedia.org/wiki/Digital_Personal_Data_Protection_Rules,_2025) · [techprescient.com](https://www.techprescient.com/blogs/dpdp-act-rules/) · [inhouseapac.com](https://www.inhouseapac.com/insights/india-dpdpa-phased-rollout-consent-2026)

**What this means for us specifically:**
1. The user uploads **third parties' personal data** (their clients' names, phones, emails, deal values). The user is the **Data Fiduciary**; we are a **Data Processor** acting on their instructions. That requires a **written processing agreement**, security measures, deletion on instruction, and no use of their data for our own purposes (including model training — plan §23 already says this).
2. The awkward clause is the last one: **contacting people whose consent predates the Act, without a compliant notice, is exactly the situation a reactivation product creates.** A dormant client from 2023 may never have received a compliant notice.
3. **This is a product opportunity, not just a liability.** [pricing.md](pricing.md) §2 records that **compliance is the one factor that reliably raises Indian SMB willingness to pay**. A reactivation tool that also (a) records where each contact came from and what they consented to, (b) flags contacts that cannot be lawfully marketed to, and (c) generates the notice/withdrawal mechanics, has a *compliance reason to be bought* — which reactivation alone does not.
   → Logged as **H9** in [HYPOTHESES.md](../HYPOTHESES.md).

**Minimum bar before the first external user uploads anything (not negotiable):**
- privacy notice + processing terms drafted;
- encryption at rest and in transit;
- a working "delete my data" that actually deletes;
- no secrets in Git (plan §40 rule 20);
- an audit log of who exported what;
- explicit statement: customer data is never used to train models.

---

## 4. WhatsApp — the channel constraint that shapes the product

**FACT (Medium confidence; India rates from a major Indian BSP):**
- Pricing moved from **per-conversation to per-template-message**; charged on successful delivery.
- **India rates:** marketing template **₹1.09/message**; utility and authentication **₹0.145**.
- Four categories: marketing (always charged, highest), utility, authentication, service (non-template replies inside a customer-initiated window — free).
- **From 1 Oct 2026:** service messages and utility templates inside the customer-service window become **billable per message**, and service messages become billable after **1,000 free per business phone number per month**.
- **Marketing messages should go only to opted-in contacts who engaged recently.**
- Meta **re-categorises mixed content** — e.g. an order update carrying a discount code is billed and policed as **marketing**, not utility.

Sources: [aisensy.com/pricing](https://aisensy.com/pricing) · [engagelab.com](https://www.engagelab.com/blog/whatsapp-business-api-pricing) · [blueticks.co](https://blueticks.co/blog/whatsapp-business-pricing-marketing-messages-2026) · [webhippo.in](https://webhippo.in/blog/whatsapp-business-api-pricing-india)

**The problem, stated plainly:** our output is a list of people who have **not engaged in 120+ days**. WhatsApp marketing policy asks for opted-in contacts who **engaged recently**. Those are close to mutually exclusive.

**Design consequences:**
1. **V0 must not send WhatsApp messages.** Generate **copy-to-clipboard text** the user pastes into their own WhatsApp — the founder's actual current workflow anyway, zero policy exposure, zero per-message cost.
2. If the API is used later, prefer **replying inside an existing thread** (service window) over a marketing template to a cold contact.
3. Track `consent_source` and `last_inbound_message_date` per contact from day one — you cannot reconstruct them later, and DPDP will want them.
4. Cost is a non-issue (30 messages ≈ ₹33/month). **Permission is the issue.**

---

## 5. Email — a constraint worth turning into positioning

**FACT (High confidence — Spamhaus):** sunset policies typically stop at **90 days** (daily senders) or **180 days** (monthly senders); abandoned mailboxes are **recycled into spam traps**, so 180+ days unengaged materially raises trap risk; dormant addresses drag **whole-domain** reputation down, hurting delivery to people who do want the mail.
Sources: [Spamhaus](https://www.spamhaus.org/resource-hub/deliverability/what-is-an-email-sunset-policy-and-why-do-you-need-one/) · [Bento](https://bentonow.com/docs/deliverability/list_hygiene) · [Omnisend](https://support.omnisend.com/en/articles/3405334-what-is-an-email-sunset-policy)

**Consequences:**
1. **Never build bulk sending.** The product's list is exactly the list deliverability professionals suppress. One-to-one, hand-sent, from the user's own mailbox, is the only safe mode — which happens to be what plan §20 already mandates.
2. **Validate addresses before surfacing** an opportunity; a bounced 2-year-old address wastes a slot in a ranked list of eight.
3. **Use it as the pitch** (see [opportunity-gaps.md](opportunity-gaps.md) §3, line C): *"Blasting your dormant list costs you your domain. These eight are worth a personal message."* This is the rare case where a real technical constraint is also the sharpest available differentiator against the incumbent GHL bulk-drip playbook.

---

## 6. Other sources

| Source | Value | Effort | Note |
|---|---|---|---|
| **Razorpay** | `total_value`, `payment_status`, `last_purchase_date` — the highest-signal commercial fields | Medium | Verify current API scopes and data-retention terms. **Unverified in this pass** |
| **Google Sheets** | The realistic V1 onboarding path | Low | Non-restricted scopes; confirm current classification |
| **Google Calendar** | Meeting history = the best proxy for "meaningful contact" | Low | Read-only; confirm scope class |
| **Shopify** | E-commerce repeat-purchase timing | Low | Out of V0 scope per plan §3 |
| **Coretex CRM** | Structured client history, first-party, no audit cost, warm users | Founder-controlled | **Do this second** |

---

## 7. Verification checklist before any integration ships

- [ ] Confirm the **current** scope classification (restricted vs sensitive vs basic) for each Google API used — in Google's own docs, not a blog
- [ ] Get **two written quotes** from Google-authorised CASA labs before committing to Gmail
- [ ] Draft the DPDP privacy notice + data-processing terms (needed well before 13 May 2027)
- [ ] Confirm Razorpay API terms permit storing customer contact data for this purpose
- [ ] Confirm the WhatsApp BSP's own opt-in requirements (they are often stricter than Meta's)
- [ ] Implement deletion, export and audit logging **before** the first external upload, not after
