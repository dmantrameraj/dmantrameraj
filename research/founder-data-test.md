# Phase 2 — Founder Dataset Experiment

**Status:** 🟡 **TEMPLATE READY — NOT RUN.** Every number below is blank on purpose.
**Rule:** plan §12 — *"Do NOT invent success numbers."* Nothing gets filled in here except from the real dataset.

---

## Why this is the most important experiment in the plan

It is the only evidence available that is **not** contaminated by vendor marketing ([market.md](market.md) §3), and it can falsify the product in about a day's work with no code written.

**Run the steps in this order.** Step 1 alone can end the project, and it takes an hour.

---

## Step 1 🔴 Field-fill measurement — do this FIRST

Export the founder's real past-client data (Coretex CRM + client spreadsheet + invoices). **Before judging any contact**, measure what is actually there.

| Field | Populated (n / 50) | % | Usable quality? |
|---|---|---|---|
| `name` | | | |
| `email` or `phone` | | | |
| `last_contact_date` | | | |
| 🔴 `total_value` | | | |
| 🔴 `last_project` | | | |
| 🔴 `project_status` | | | |
| 🔴 `previous_services` | | | |
| 🔴 `previous_interest` | | | |
| `last_conversation_summary` | | | |
| `pending_action` | | | |

**Gate:**

| Result | Action |
|---|---|
| `total_value` **and** (`previous_services` or `previous_interest`) ≥ **40%** | Continue to Step 2 |
| Below 40% | **STOP.** Read [evidence-against.md](evidence-against.md) §2. The intelligence layer has no inputs. Either the product becomes a data-capture tool, or it becomes a Coretex-only feature, or the thesis fails. Record the decision in [DECISIONS.md](../DECISIONS.md) either way |

**Founder's own note (fill in):** where did each 🔴 field have to come from — CRM, invoices, memory, WhatsApp scrollback? If the answer is "memory", that is a finding: **no software can read the founder's memory**, and neither can it read the customer's.

---

## Step 2 — Build the dataset

1. Copy [templates/founder-50-contact-template.csv](templates/founder-50-contact-template.csv), delete the EXAMPLE row.
2. Fill **~50 genuinely inactive** past contacts from Coretex CRM, the old client spreadsheet, Gmail and invoice records.
3. **Sampling rule (important):** take them in a consistent, unbiased order — e.g. every past client whose last contact falls in a date window — **not** the ones the founder already remembers as promising. Cherry-picking the good ones is the exact failure mode plan §13 warns about (*"Do not manipulate the data to make the idea look good"*).
4. Record the real dormancy spread:

| Bucket | Count |
|---|---|
| 0–90 days | |
| 91–180 days | |
| 181–365 days | |
| 365+ days | |

**⚠️ Store this file outside Git.** It contains real clients' personal data and revenue. Put it in a private drive, and keep only the aggregate numbers in this repo. `research/data/` is already git-ignored for this purpose.

---

## Step 3 — Founder judgement FIRST, blind to any AI output

Fill every `J_*` column for all 50 rows **before** running any model. If the AI runs first, its framing contaminates the human judgement and the false-positive measurement becomes meaningless.

---

## Step 4 — AI analysis

Run the §10 analysis (status, potential, score, reason, trigger, action, message draft) and fill the `AI_*` columns. Record the setup honestly:

| | |
|---|---|
| Model + version | |
| Date run | |
| Prompt used (path/commit) | |
| Fields given to the model | |
| Cost of the run (actual) | |

---

## Step 5 — Validate

Fill the `V_*` columns. Then the metrics.

---

## Metrics (plan §12) — fill from the dataset only

| # | Metric | Result | Notes |
|---|---|---|---|
| 1 | Of 50, how many are **genuinely worth reactivating** (`J_worth_reactivating = yes`) | | plan §13 example threshold: 15+ = strong signal. **This is an example, not a rule** |
| 2 | How many have a **specific legitimate reason** (`J_specific_reason = yes`) | | The reason must be more than elapsed time |
| 3 | How many have **meaningful historical commercial value** | | State the ₹ cut-off used |
| 4 | **Total historical value** of the Metric-1 set | ₹ | Historical revenue — never mix with potential |
| 5 | How many would the founder **personally contact** if surfaced | | |
| 6 | How many messages could realistically be sent **this week** | | The true capacity ceiling — if it is 5, a list of 40 is noise |

### Added metrics the research showed are necessary

| # | Metric | Result | Why |
|---|---|---|---|
| 7 | **AI false positives**: `AI_potential = High` but `J_worth_reactivating = no` | / | High FP rate destroys trust in one session |
| 8 | **AI false negatives**: `J_worth_reactivating = yes` but AI ranked Low/Insufficient | / | Missing the obvious wins is worse than noise |
| 9 | 🔴 **Fabrication rate**: rows with `V_reason_fabricated = yes` | / | **Any fabrication above 0 is a release blocker** (plan §10G, §26) |
| 10 | **Message quality**: as-is / minor edit / rewrite / unusable | / / / | If most need a rewrite, the drafting feature is not a feature |
| 11 | **Reason agreement**: AI reason matches `J_reason_text` in substance | / | Tests whether the "why" is real intelligence |
| 12 | **Dormancy distribution of the Metric-1 set** (0–90 / 91–180 / 181–365 / 365+) | / / / | If the good ones are nearly all <120 days, reposition — [evidence-against.md](evidence-against.md) §5 |
| 13 | **Unsold-service hit rate**: rows with a `previous_interest` that was never sold | / | Directly measures the recommended wedge ([opportunity-gaps.md](opportunity-gaps.md) §3). If this is near zero, the wedge does not exist |
| 14 | 🔴 **Monthly replenishment**: how many *new* contacts would qualify next month | | If <5, this is not a subscription — [evidence-against.md](evidence-against.md) §3 |
| 15 | **Time to produce the founder's own 50 judgements** | hrs | The upper bound of what the software must beat. Also the cost basis for the concierge offer |

---

## Step 6 — Decision (plan Phase 2)

| Condition | Decision |
|---|---|
| Step 1 field-fill < 40% | **PIVOT** — data-capture product, or Coretex-only feature |
| Metric 13 ≈ 0 | **PIVOT** — the unsold-service wedge does not exist in real data; fall back to recency+value ranking and accept a weaker differentiation |
| Metric 9 > 0 | **BLOCK** — fix the prompt/guardrails before anyone outside sees output |
| Metric 14 < 5 | **REPRICE** — one-off audit or annual, not monthly |
| Metric 12 concentrated <120 days | **REPOSITION** — early follow-up, not resurrection |
| Metrics 1, 2, 5 healthy and 9 = 0 | **CONTINUE** to Phase 3 (customer discovery) |

**Final decision:** _(not yet run)_
**Date:** _(not yet run)_
**Recorded in [DECISIONS.md](../DECISIONS.md) as:** _(pending)_

---

## Honesty checklist before recording any result

- [ ] The 50 contacts were selected by a rule, not by promise
- [ ] `J_*` was filled before the AI ran
- [ ] No row was deleted because it made the numbers look bad
- [ ] Historical value, potential value and recovered value are three separate columns and were never summed together (plan §28)
- [ ] The fabrication count is reported even if it is embarrassing
- [ ] The raw file stayed out of Git
