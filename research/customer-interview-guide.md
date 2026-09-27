# Customer Interview Guide (Phase 3)

**Status:** 🟡 Ready to use. **0 of 12–20 interviews done.**
Log every conversation in [customer-interviews.md](customer-interviews.md). Never fill a row that did not happen (plan §40 rule 11).

---

## 0. The two rules that make this worth doing

Plan §14 forbids the two questions everyone asks:
- ❌ *"Would you use this?"*
- ❌ *"Would you pay ₹999?"*

Because people say yes to be kind and it predicts nothing.

**Replace them with:** *"Tell me about the last time this happened to you."* Past behaviour is data. Future intentions are politeness.

**Second rule: do not pitch.** Do not describe the product until the last five minutes, and when you do, describe it flatly and then **shut up and watch their face**. Everything before that point is the evidence; everything after is contaminated.

---

## 1. Screener (use before booking — 4 questions, by WhatsApp or DM)

1. Roughly how many clients or customers have you worked with in total? (**need 50+**)
2. Do you have clients whose projects are finished and who you are not currently working with? (**need yes**)
3. Where do their details live — CRM, spreadsheet, phone, Gmail, somewhere else?
4. Who handles client relationships and sales — you personally, or someone else? (**need: them personally**)

**Quota (12–20 total):** 4–6 solo freelancers · 4–6 agencies of 2–10 · 2–4 consultants/coaches · 2–4 other service businesses.
**Deliberately include 3–4 people who you expect to say the problem is not real.** A sample of only enthusiasts guarantees a false positive (plan §37).

**Logistics:** 30 minutes, video or phone, recorded with permission, transcript kept out of Git. Offer something real for their time (a free reactivation audit works, and doubles as the Phase 4 test).

---

## 2. Script

### A. Warm-up (3 min)
1. Tell me what your business does and who your typical client is.
2. How many clients have you worked with, roughly, all-time?
3. How much of your work this year came from someone you had worked with before?
   *(Probe: was that repeat business, a referral, or a client who came back on their own?)*

### B. The last real incident — the core of the interview (10 min)
Plan §14 Q1–Q9. Stay on **one specific person** until it is fully described. Do not let them generalise.

4. Tell me about the last client you meant to follow up with and didn't.
5. How did you realise you had forgotten them?
6. Where was their information — which app, which file?
7. Was the conversation on WhatsApp, Gmail, a call, a CRM, or somewhere else?
8. How long had it been?
9. What would that relationship have been worth if it had come back?
10. Did you eventually contact them? *(If yes:* what happened? *If no:* what stopped you?)
11. What would have had to happen for you to contact them earlier?

> **Listen for which blocker they name, because it decides what to build:**
> "I forgot they existed" → **detection**
> "I didn't know what to say" → **context + drafting**
> "It felt awkward / like begging" → **framing and a legitimate reason** ← *this is the wedge*
> "I just never got round to it" → **accountability, not intelligence** ← *a different product*
> "There was no point, they were done" → **the thesis is weak for this person**

### C. Current behaviour (7 min)
Plan §14 Q10–Q18.

12. How do you currently work out which old clients are worth contacting again?
13. Do you ever review your old client list on purpose? When did you last do it?
14. After a long gap, how do you decide what to talk about?
15. Have you ever reopened an old client and won another project? Tell me about it.
16. How often does that happen — a few times a year, or rarer?
17. What do you need to know about a client before you contact them after a gap?
18. What tools do you use today? What do you pay for them?
19. What did you cancel in the last year, and why?
20. **Screen share: show me how you'd find an old client worth contacting right now.** *(Then stay quiet and time it. This single question is worth more than questions 1–19 combined.)*
21. What is the most frustrating part of all this?

### D. The unsold-service probe (3 min) — tests the recommended wedge
[opportunity-gaps.md](opportunity-gaps.md) §3 recommends positioning on *"the service you never sold them"*. Test it **before** naming the product:

22. Are there services you offer that a past client discussed with you but never actually bought?
23. Could you list those clients right now, or would you have to go digging?
24. If you had that list this afternoon — who paid you before, what they discussed and never bought, and what it was worth — what would you do with it?

> **The answer to 23 is the make-or-break signal.** If they can list them from memory, the selection problem is not real at their scale (hypothesis **P2** falsified) and the product must move to the doing, not the finding.

### E. Concept + price, last 5 minutes only
25. Describe the product **flatly**, in one sentence, no adjectives: *"It reads your past-client list and tells you which finished clients are worth contacting, why, and drafts the message — you approve before anything sends."*
26. What's your honest first reaction? *(Wait. Let the silence do the work.)*
27. What would make you not trust it?
28. Would you upload a client list with revenue figures to it? What would have to be true first?
29. **Instead of "would you pay":** *"If I did this for you by hand next week — cleaned your list, found the opportunities, wrote 20 messages — what would that be worth to you?"* Then: *"Can I do that for you? I'd charge ₹X."*
   → **This converts an interview into the Phase 4 concierge test and produces real WTP data.** A yes here outweighs any opinion given in the previous 28 questions.
30. Who else should I talk to?

---

## 3. Scoring each interview against the Build Gates (plan §38)

Score after each interview, from what they **did**, not what they said they would do.

| Gate | Question | Score | Evidence |
|---|---|---|---|
| **A — Problem** | Did they describe the problem unprompted, with a specific person and a specific loss? | ✅ / ⚠️ / ❌ | quote |
| **B — Frequency** | Does it happen often enough to matter? (Q16) | ✅ / ⚠️ / ❌ | |
| **C — Value** | Is there real money in it? (Q9) | ✅ / ⚠️ / ❌ | ₹ |
| **D — Workaround** | Do they have a painful current method? (Q12, Q20) | ✅ / ⚠️ / ❌ | time taken on Q20 |
| **E — Gap** | Does their existing tooling fail to solve it? (Q18) | ✅ / ⚠️ / ❌ | |
| **F — Trust** | Would they let AI read their client history? (Q28) | ✅ / ⚠️ / ❌ | |
| **G — Willingness** | Did they agree to the paid/free audit? (Q29) | ✅ / ⚠️ / ❌ | ₹ named, yes/no |

**Reading the aggregate honestly:**

| Pattern across 12+ interviews | Meaning |
|---|---|
| A–G mostly ✅, and 3+ accept a **paid** audit | Strong. Proceed to Phase 4 properly, then Phase 5 |
| A ✅ but B or C ❌ | Real but small. Reposition or drop |
| A–E ✅ but G ❌ everywhere | They have the problem and will not pay to solve it. The most common way this kills a product |
| Most can answer Q23 from memory | The selection problem is not real at this scale. **Build for the doing, not the finding** |
| A ❌ — you had to explain the problem to them | **Gate A fails. Stop.** Plan §38 |

---

## 4. Anti-bias discipline while interviewing

1. **Ask "why" three times** before accepting an answer.
2. **Count the silences.** If you are talking more than a third of the time, you are selling, not learning.
3. **Write the verbatim quote**, not your summary of it. Your summary will agree with you; their words won't.
4. **Log the interviews that went badly** with the same care as the good ones. A file of 12 enthusiastic interviews is a file you cannot trust.
5. **Never argue** with an objection during the interview. Write it down and thank them.
6. After every third interview, write one line: *"What did I just learn that I did not want to hear?"* If the answer is "nothing", the interviews are not working.
