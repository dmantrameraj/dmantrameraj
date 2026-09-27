# V0 Import Schema

Specifies the columns in [founder-50-contact-template.csv](founder-50-contact-template.csv). Based on plan §9, with additions the research made necessary.

**Design rule (plan §9):** the system must tolerate missing fields. Do not require perfect CRM data. **But** — [evidence-against.md](evidence-against.md) §2 shows the product is worthless without the 🔴 fields below, so the product must *measure and report* what it is missing rather than silently degrading into a reminder.

---

## Column groups

### A. Identity (from plan §9)

| Field | Required | Notes |
|---|---|---|
| `name` | ✅ | |
| `company` | | |
| `email` | one of email/phone | validate before surfacing (bounces waste a slot) |
| `phone` | one of email/phone | E.164 preferred |
| `source` | | where the relationship came from |
| `lead_or_customer` | ✅ | **V0 scope = `customer` only** (see [opportunity-gaps.md](opportunity-gaps.md) §3) |

### B. Timeline

| Field | Required | Notes |
|---|---|---|
| `first_contact_date` | | relationship duration |
| `last_contact_date` | ✅ | drives dormancy |
| `last_contact_channel` | **added** | email / whatsapp / call / meeting — decides *where* to reconnect (plan §5 "WHERE?") |
| `last_inbound_date` | **added** | last time *they* contacted *you*. Two reasons: a genuinely warm relationship has recent inbound, and WhatsApp/email policy cares about recent engagement ([integrations.md](integrations.md) §4) |

### C. 🔴 Commercial history — the fields the whole thesis rests on

| Field | Required | Notes |
|---|---|---|
| `total_value` | 🔴 | historical revenue. **Without this there is no ranking** |
| `number_of_projects` | | repeat behaviour |
| `last_project` | 🔴 | what you actually did |
| `project_status` | 🔴 | completed / lapsed / stalled / ongoing |
| `previous_services` | 🔴 | what they **bought** |
| `previous_interest` | 🔴 | what they **discussed but never bought** — *the single highest-value field in the schema*; it is what makes the wedge possible |
| `invoice_status`, `payment_status` | | "paid in full, then silence" is a strong trigger |
| `last_purchase_date`, `renewal_date` | | timing |

### D. Context

| Field | Notes |
|---|---|
| `last_conversation_summary` | the "what do I say" input |
| `pending_action` | something you promised and never delivered — the most legitimate reason to reconnect that exists |
| `notes`, `industry`, `location`, `tags` | |
| `consent_source` | **added** — how you obtained permission to contact them. Needed for DPDP (effective 13 May 2027) and WhatsApp opt-in. Cannot be reconstructed later; capture from day one ([integrations.md](integrations.md) §3) |

### E. `J_*` — Founder's own judgement (Phase 2 only)

Fill these in **before** looking at any AI output, or the test is worthless.

| Field | Values |
|---|---|
| `J_worth_reactivating` | yes / no / maybe |
| `J_specific_reason` | yes / no — is there a *specific legitimate* reason, not just elapsed time? |
| `J_reason_text` | the reason in the founder's own words |
| `J_potential_value` | ₹ estimate of a realistic next engagement |
| `J_would_contact_this_week` | yes / no — the behavioural question (plan §12 Metric 5/6) |
| `J_confidence` | high / medium / low |
| `J_why_not` | if no: dead business / bad fit / relationship damaged / no need / unreachable / other |

### F. `AI_*` — Model output (Phase 2)

`AI_status` (Active / Recently inactive / Dormant / Lost / Unknown) · `AI_potential` (High / Medium / Low / Insufficient data) · `AI_score` (0–100) · `AI_reason` · `AI_action` · `AI_trigger` · `AI_message_draft`

### G. `V_*` — Validation of the AI against the founder's judgement

| Field | Values | Purpose |
|---|---|---|
| `V_reason_accurate` | yes / no | is the stated reason factually right? |
| `V_reason_fabricated` | **yes / no** | **did the AI invent a conversation, date, promise, purchase or problem that is not in the row?** Any `yes` is a critical defect — plan §10G / §26 |
| `V_action_sensible` | yes / no | |
| `V_message_sendable` | as-is / minor edit / rewrite / unusable | the real product metric |
| `V_verdict` | TP / FP / FN / TN | true/false positive/negative vs `J_worth_reactivating` |
| `V_notes` | free text | |

---

## Field-fill measurement (do this before anything else)

For each 🔴 field, record `% of rows populated` in [founder-data-test.md](founder-data-test.md) §1.

**Kill threshold:** if `total_value` **and** (`previous_services` or `previous_interest`) are populated for **fewer than 40%** of rows, stop and re-read [evidence-against.md](evidence-against.md) §2 before doing anything else. That result means the intelligence layer has no inputs in the real world, and the product as specified cannot work.
