# Dormant Client Reactivation SaaS — Master Project Plan

## 0. Purpose of This File

This file is the source-of-truth plan for Claude Code.

Claude must use this document to continue the product research and development process without jumping directly into coding.

The product is currently a **hypothesis**, not a validated SaaS.

The first objective is NOT to build a large CRM.

The first objective is to prove that businesses have a valuable, recurring problem around:

> **Finding old client/customer relationships that have gone cold but still have realistic revenue potential, understanding WHY they should be contacted, and knowing WHAT to do next.**

Working product concept:

**Dormant Client Reactivation / Revenue Recovery Intelligence**

Possible positioning:

> "Your old clients aren't dead leads. Find the ones worth reconnecting with."

Core product principle:

> **Don't just remind me. Understand what needs to happen next.**

---

# 1. Product Thesis

Small service businesses, freelancers, consultants, coaches and agencies often have hundreds of historical contacts across:

- CRM
- Google Sheets
- Gmail
- WhatsApp
- Calendar
- payment systems
- proposals
- invoices
- forms
- e-commerce systems

The problem is not simply that they forget to send reminders.

The deeper problem is:

1. They have valuable historical relationships.
2. Context is fragmented across different tools.
3. Some relationships become inactive.
4. They do not know which inactive contacts are actually worth reactivating.
5. They do not remember the previous context.
6. They do not know the best reason to restart the conversation.
7. By the time they remember, the relationship may already be cold.
8. Existing CRM tools mostly manage active pipelines and follow-ups.
9. Generic AI follow-up tools already exist.

Therefore the opportunity may be:

> **An intelligence layer that discovers hidden revenue opportunities inside old relationships.**

---

# 2. Important Strategic Decision

## DO NOT BUILD

Do not start by building:

- another generic CRM
- another contact manager
- another invoice generator
- another WhatsApp bulk sender
- another generic AI chatbot
- another generic AI follow-up reminder
- another email automation platform
- another pipeline board
- another task/reminder application

These markets are already crowded.

Competitors such as folk and Circle already cover significant parts of AI-powered relationship follow-up.

The differentiation must come from:

### "Who should I contact again, why, and what should I say?"

Especially:

### "Which OLD relationship has realistic revenue potential right now?"

---

# 3. Primary Target Customer — Current Hypothesis

Start narrow.

Primary ICP:

- freelancers
- solo agencies
- small digital marketing agencies
- consultants
- coaches
- service businesses
- small B2B businesses

Ideal customer characteristics:

- 50–1,000 historical contacts/customers
- already has old clients/leads
- has completed projects
- receives repeat business
- has past conversations/proposals
- uses spreadsheets, CRM, Gmail or WhatsApp
- personally handles sales/client relationships
- frequently forgets to reconnect

Do NOT initially target everyone.

### Secondary markets later

- e-commerce sellers
- recruiters
- real estate
- insurance
- larger sales teams

E-commerce may eventually become a separate use case around:

> "Which customers are ready for another purchase?"

But do not mix that into V0.

---

# 4. User's Own Pain Evidence

The founder's current workflow already contains relevant pain:

- creating invoices
- setting follow-ups
- checking calendar
- remembering client conversations
- reconnecting with clients after long gaps
- replying to clients
- sending promised material
- checking payments
- posting content
- updating CRM
- moving information between WhatsApp and Google Sheets
- moving information between Gmail and CRM
- moving form data into WhatsApp
- moving Razorpay information into Sheets
- moving Shopify information into Sheets

A particularly important pain:

> Around 30 clients/leads may be forgotten for follow-up in a typical month.

Founder also stated:

> If software automatically told him which relationships need attention, he would use it.

Founder willingness-to-pay hypothesis:

> Approximately ₹999/month for a genuinely useful product.

These are founder observations, NOT market validation.

They must be tested with external customers.

---

# 5. Core Product Promise

Potential core promise:

> **Find the old clients worth reconnecting with.**

Expanded:

> Connect your CRM, Gmail or spreadsheet. AI identifies dormant relationships with potential value, explains why they are worth contacting, recommends the next action, and prepares a personalized message.

The product should answer:

### WHO?
Who needs attention?

### WHY?
Why does this person/company matter?

### WHY NOW?
Why is this relationship worth reactivating now?

### WHAT?
What should I offer/discuss?

### HOW?
What should I say?

### WHERE?
Which communication channel makes sense?

### WHAT NEXT?
What should happen after the message?

---

# 6. Core Workflow

Example:

Customer:

Rahul

History:

- Website project completed
- ₹35,000 historical value
- Last meaningful contact: 124 days ago
- Invoice fully paid
- Previously discussed Google Ads
- No current project
- No recent communication

AI analysis:

> "Rahul appears to be a dormant client with previous commercial value. Your website project is complete, but you previously discussed Google Ads. A website performance review or Google Ads discussion may be a natural reason to reconnect."

Suggested action:

> Reactivate

Suggested message:

> Personalized message based on actual relationship history.

Human controls:

- Send
- Edit
- Snooze
- Ignore
- Mark as contacted

The AI must explain its reasoning.

---

# 7. Important Product Philosophy

The product should NOT simply say:

> "Rahul has not been contacted for 90 days."

That is a reminder.

The product should say:

> "Rahul has not been contacted for 124 days, previously paid ₹35,000, completed a website project, and had previously discussed Google Ads. This looks like a reasonable reactivation opportunity."

That is intelligence.

---

# 8. Initial Product Architecture

## V0

Do NOT begin with complex integrations.

Start with:

```text
CSV / Google Sheet
        ↓
Data Cleaning
        ↓
Contact / Customer History
        ↓
AI Analysis
        ↓
Dormant Relationship Detection
        ↓
Opportunity Scoring
        ↓
Reason / Explanation
        ↓
Recommended Next Action
        ↓
Personalized Message Draft
        ↓
Human Approval
```

The V0 objective is to prove the intelligence layer.

---

# 9. V0 Input Data

Create a standard import schema.

Minimum fields:

```text
name
company
email
phone
last_contact_date
first_contact_date
lead_or_customer
total_value
last_project
previous_services
project_status
last_conversation_summary
pending_action
previous_interest
notes
source
```

Optional:

```text
industry
location
deal_stage
invoice_status
payment_status
next_followup_date
number_of_projects
last_purchase_date
renewal_date
tags
```

The system must tolerate missing fields.

Do not require users to have perfect CRM data.

---

# 10. AI Analysis Requirements

For every contact, AI should determine:

### A. Relationship status

Possible values:

- Active
- Recently inactive
- Dormant
- Lost
- Unknown

### B. Commercial history

Determine:

- historical value
- number of projects
- previous services
- previous purchases
- relationship duration if possible

### C. Reactivation potential

Classify:

- High potential
- Medium potential
- Low potential
- Insufficient data

IMPORTANT:

This must not pretend to predict guaranteed revenue.

Use language such as:

- "potential"
- "possible opportunity"
- "worth reviewing"
- "reasonable reason to reconnect"

Avoid:

- "This client will buy"
- "Guaranteed revenue"
- "90% chance of closing"

### D. Reason

Generate a concise explanation:

> "Why this relationship deserves attention."

### E. Suggested trigger

Examples:

- project completed
- previous service discussion
- renewal window
- seasonal opportunity
- long inactivity after successful project
- unresolved proposal
- payment completed but no follow-up
- previous interest
- potential upsell based on past service

### F. Recommended action

Examples:

- Reactivate
- Ask for update
- Offer review
- Discuss renewal
- Offer related service
- Check satisfaction
- Send useful resource
- Do nothing

### G. Suggested message

Personalized draft based ONLY on known information.

Never fabricate:

- previous conversations
- dates
- purchases
- promises
- business problems
- personal details

If information is missing, write generically.

---

# 11. Opportunity Scoring

Do not over-engineer scoring initially.

Start with transparent factors.

Example:

```text
Historical Value
Relationship Recency
Previous Purchase
Previous Service
Unfinished Opportunity
Previous Interest
Potential Timing
Relationship Strength
```

Possible internal score:

```text
0–100
```

But the UI should prioritize explanation over the score.

Example:

```text
82/100

Why:
✓ Previous paying client
✓ ₹35,000 historical value
✓ Project completed
✓ Previous interest in Google Ads
✓ 124 days since meaningful contact

Recommended:
Reconnect with a website performance / Google Ads discussion.
```

The score is a prioritization aid, NOT a prediction.

---

# 12. Critical Validation Experiment

Before building the SaaS:

## Founder Data Test

Take approximately 50 old/inactive contacts from:

- Coretex CRM
- old client spreadsheet
- Gmail
- previous customer records

Create a simple dataset.

For each contact record:

```text
Name
Last contact
Historical value
Previous service
Previous interest
Current status
Potential reactivation reason
Would you realistically contact them?
Potential opportunity value
```

Then manually/AI-assisted classify them.

Measure:

### Metric 1
How many of 50 are genuinely worth reactivating?

### Metric 2
How many have a specific legitimate reason to reconnect?

### Metric 3
How many have meaningful historical commercial value?

### Metric 4
Estimated potential pipeline represented by those contacts.

### Metric 5
How many would the founder personally contact if the system surfaced them?

### Metric 6
How many messages could realistically be sent this week?

Do NOT invent success numbers.

---

# 13. Validation Gate

Suggested interpretation:

### Strong signal

If a meaningful portion of old contacts reveal legitimate reactivation opportunities and meaningful historical/potential value, continue.

Example:

```text
50 contacts
15+ legitimate opportunities
Several have meaningful historical value
Multiple actionable reasons to reconnect
```

This is only an example threshold, NOT a hard market rule.

### Weak signal

If most old contacts are genuinely dead, irrelevant, or have no natural reason to reconnect, reconsider the thesis.

Do not manipulate the data to make the idea look good.

---

# 14. Customer Discovery

Interview 10–20 people from the ICP.

Do NOT ask:

> "Would you use this?"

Do NOT ask:

> "Would you pay ₹999?"

Those questions produce weak validation.

Ask about actual behavior.

## Interview questions

1. Tell me about the last client you forgot to follow up with.
2. How did you realize you had forgotten them?
3. Where was the client's information stored?
4. Was the conversation on WhatsApp, Gmail, CRM, spreadsheet or somewhere else?
5. How long had it been since you contacted them?
6. What was the potential value of that relationship?
7. Did you eventually contact them?
8. If not, why?
9. What would have made you contact them earlier?
10. How do you currently identify old clients worth reconnecting with?
11. Do you review your old clients regularly?
12. How do you know what to talk about after a long gap?
13. Have you ever reopened an old client and won another project?
14. How often does that happen?
15. What information do you need before contacting an old client?
16. What tools are you currently using?
17. What do you dislike about your current system?
18. Show me how you currently find old clients/leads.
19. What happens when a client relationship becomes inactive?
20. What is the most frustrating part of the process?

Focus on stories and real behavior.

---

# 15. Competitor Research

Claude must continue monitoring competitors.

Known competitors / adjacent products:

- folk
- Circle Connect
- generic CRM platforms
- CRM AI follow-up tools
- dormant lead reactivation services
- sales engagement tools
- customer retention tools
- WhatsApp automation products

Research objectives:

### For every competitor find:

```text
Product
Target customer
Core promise
Main workflow
Integrations
Pricing
AI capabilities
Reactivation capability
Follow-up capability
CRM capability
Automation capability
Weaknesses
Customer complaints
Reviews
Positioning
```

Use current official websites and current public sources.

Do not rely on outdated pricing.

---

# 16. Competitive Gap To Investigate

The key question:

> Are existing tools primarily reminding users about follow-ups, or are they actually identifying dormant relationships with legitimate commercial reasons for reactivation?

Research this carefully.

Look for gaps such as:

- too much CRM complexity
- requires manual data entry
- focuses on active leads
- generic follow-up reminders
- poor historical relationship understanding
- weak explanation of WHY to contact
- weak post-sale reactivation
- too much automation
- spam risk
- expensive for solo operators
- requires switching CRM
- no simple CSV/Sheet entry
- poor India-friendly pricing
- no clear revenue-recovery workflow

Do not assume these are gaps.

Validate each one.

---

# 17. Important Differentiation Hypothesis

Potential positioning:

## Existing CRM

> Manage your pipeline.

## Follow-up tool

> Remind me who to follow up with.

## This product

> Find valuable relationships that have gone cold and tell me why I should reconnect.

This distinction must be validated with users.

---

# 18. Post-Sale Reactivation Wedge

Strong hypothesis to investigate:

Most tools focus on:

```text
Lead → Follow-up → Deal → Close
```

This product could focus on:

```text
Customer → Project Complete → Silence → Dormant → Reactivation → Repeat Revenue
```

Potential positioning:

> **Your old clients are your next leads.**

Or:

> **Turn forgotten client relationships into new opportunities.**

Do not finalize the positioning until customer interviews validate it.

---

# 19. MVP Feature Scope

If validation succeeds, MVP should include:

## Authentication

- signup
- login
- basic account

## Data Import

- CSV upload
- sample dataset
- column mapping

Later:

- Google Sheets
- Gmail
- Google Calendar
- Coretex CRM

## Contact Intelligence

- relationship status
- last meaningful interaction
- historical value
- previous service
- previous interest
- dormant detection
- opportunity score
- explanation

## Opportunity Dashboard

Example:

```text
ATTENTION TODAY

12 Reactivation Opportunities

₹3.2L Historical Value

4 High Priority
5 Medium Priority
3 Low Priority
```

Each contact:

```text
Rahul Sharma
Website Client

Last Contact:
124 days ago

Historical Value:
₹35,000

Why attention:
Previously purchased website development
Previously discussed Google Ads
No recent communication

Suggested action:
Website performance / Google Ads check-in

[Draft Message]
[Edit]
[Snooze]
[Ignore]
```

## Message Generator

Channels initially:

- Email
- WhatsApp copy

Do NOT automatically send messages in MVP.

Human approval is mandatory.

---

# 20. Human-in-the-Loop Rule

Default behavior:

```text
AI detects opportunity
        ↓
AI explains reason
        ↓
AI drafts message
        ↓
USER REVIEWS
        ↓
User sends
```

Never default to mass automated outreach.

The product should protect users from:

- spam
- incorrect personalization
- fabricated context
- inappropriate timing
- contacting people who should not be contacted

---

# 21. V1 Integrations

Only after V0 proves value.

Priority order:

### 1. Google Sheets

Easy onboarding.

### 2. Gmail

Historical email context.

### 3. Google Calendar

Meeting history and future timing.

### 4. Coretex CRM

Important strategic integration because the founder owns Coretex.

Potential workflow:

```text
Coretex CRM
      ↓
Relationship Intelligence
      ↓
Dormant Opportunities
      ↓
AI Recommendation
      ↓
Human Action
```

### 5. Razorpay

Payment/customer history.

### 6. WhatsApp

Only after privacy, API and compliance requirements are understood.

### 7. Shopify

Potential e-commerce expansion.

---

# 22. Coretex Strategic Opportunity

Coretex CRM can eventually become the data source.

Do NOT immediately merge the products.

Possible architecture:

```text
Coretex CRM
     +
Gmail
     +
Calendar
     +
Sheets
     ↓
Relationship Intelligence Layer
     ↓
Revenue Recovery Dashboard
```

Coretex could offer the intelligence as:

- premium add-on
- higher plan
- separate SaaS
- white-label feature

But this decision comes AFTER validation.

---

# 23. Privacy & Security Requirements

This product may process sensitive customer information.

Privacy must be treated as a core product requirement.

Principles:

- minimum necessary data
- clear consent
- user-controlled integrations
- secure OAuth
- encrypted credentials/tokens
- no selling customer data
- no training on customer data without explicit policy/permission
- clear data deletion
- audit logs where appropriate
- user can disconnect integrations
- transparent AI processing
- do not store unnecessary message content

Before production Gmail/WhatsApp integrations, investigate:

- OAuth requirements
- API policies
- data retention
- permissions
- encryption
- compliance requirements
- provider restrictions

---

# 24. Technical Direction

Claude Code may choose the implementation stack after research.

Do not lock architecture prematurely.

Preferred philosophy:

```text
Simple
Maintainable
Cheap to operate
API-first
AI-model agnostic
Easy to deploy
Secure
```

Possible components:

```text
Frontend
Backend API
PostgreSQL/MySQL
AI provider
Background jobs
Authentication
OAuth integrations
Vector/search layer only if actually required
```

Do NOT add vector databases, microservices, Kubernetes, event buses, etc. unless justified.

Start as a modular monolith.

---

# 25. AI Architecture

Separate AI tasks.

Potential pipeline:

```text
Raw Data
   ↓
Normalization
   ↓
Entity Resolution
   ↓
Timeline Construction
   ↓
Relationship Summarization
   ↓
Opportunity Detection
   ↓
Reason Generation
   ↓
Next Action
   ↓
Message Draft
```

Do not send the entire database blindly to the model.

Use relevant context.

Example:

```text
Customer Profile
+
Recent Relevant History
+
Historical Commercial Data
+
Previous Interests
+
Current Timing
```

Then ask AI to reason.

---

# 26. AI Guardrails

The AI must:

- distinguish facts from assumptions
- identify missing information
- avoid fabricated context
- avoid fake urgency
- avoid manipulative sales language
- avoid pretending to know customer intent
- explain why it made a recommendation
- provide confidence/uncertainty where appropriate

Example:

BAD:

> "Rahul definitely needs Google Ads now."

GOOD:

> "You previously discussed Google Ads with Rahul. Since the website project is complete and there has been no recent contact, a performance review could be a natural reason to reconnect."

---

# 27. Product UX

The UX should feel like an assistant, not another CRM.

Main dashboard:

```text
Good morning, Meraj.

You have 8 relationships worth reviewing.

----------------------------------

🔥 REACTIVATE NOW

Rahul Sharma
₹35,000 historical value
124 days inactive

Why:
Previously discussed Google Ads.

Next action:
Offer a website performance review.

[Draft Message]

----------------------------------

🟡 NURTURE

Amit...
...

----------------------------------

⚪ LEAVE ALONE

...
```

The user should understand the recommendation in seconds.

---

# 28. Dashboard Metrics

Potential metrics:

```text
Relationships Analyzed
Dormant Relationships
Reactivation Opportunities
Historical Value
Potential Opportunity Value
Messages Drafted
Relationships Reactivated
Responses
Meetings Booked
Repeat Revenue
```

Be careful with "potential opportunity value".

Clearly distinguish:

```text
Historical Revenue
Potential Opportunity Value
Actual Recovered Revenue
```

Never mix these numbers.

---

# 29. Success Metrics

Primary product metric:

> Number of dormant relationships that lead to meaningful user action.

Possible activation metric:

> User identifies and contacts at least 3 relevant dormant relationships within the first session.

Long-term:

```text
Reactivation rate
Response rate
Meetings created
Repeat purchases
Recovered revenue
Weekly active users
Monthly active users
Retention
```

North-star candidate:

> **Meaningful relationship reactivations per active customer per month**

Validate this later.

---

# 30. Pricing Hypothesis

Founder willingness-to-pay hypothesis:

> ₹999/month.

Do NOT assume market willingness-to-pay.

Test pricing after problem validation.

Potential future structure:

### Free

- limited contacts
- limited analysis

### Starter

- small contact database
- monthly analysis

### Pro

- Gmail/Sheets/CRM integrations
- higher limits
- advanced intelligence

### Business

- team
- multiple data sources
- advanced automation

Pricing should be validated through customer interviews and actual conversion experiments.

---

# 31. Landing Page Validation

Before full development, create a simple landing page/fake-door test.

Potential headline:

> **Your Old Clients Aren't Dead Leads.**

Subheadline:

> AI finds the relationships worth reconnecting with, explains why they matter, and prepares a personalized message.

CTA:

> **Find My Lost Opportunities**

Alternative:

> **See Who I Should Reconnect With**

Landing page should show:

1. Problem
2. How it works
3. Example opportunity
4. Human approval
5. Privacy
6. CTA

Do not claim guaranteed revenue.

---

# 32. Fake-Door Experiment

Potential flow:

```text
Landing Page
      ↓
CTA
      ↓
Signup / Waitlist
      ↓
Upload CSV
      ↓
"Analysis coming soon"
```

Better:

If technically possible, provide a real lightweight CSV analysis instead of a fake result.

The goal is to measure:

- landing page conversion
- data upload intent
- number of people willing to analyze old contacts
- actual opportunity quality
- willingness to use repeatedly

---

# 33. Research Task For Claude

Claude must research:

### Market

- dormant client reactivation
- customer win-back
- customer retention
- relationship intelligence
- sales follow-up
- CRM AI
- revenue recovery
- client reactivation
- customer success

### Competitors

Research current products.

For each product record:

```text
URL
Pricing
ICP
Positioning
Features
Integrations
AI
Reactivation
Reviews
Weaknesses
Differentiation
```

Use current sources.

Prefer:

- official product pages
- official pricing pages
- product documentation
- reputable review sources
- Reddit/community discussions for qualitative pain
- current market reports where useful

---

# 34. Research Output Format

Claude should maintain:

```text
/research
    market.md
    competitors.md
    customer-pain.md
    reddit-insights.md
    pricing.md
    integrations.md
    opportunity-gaps.md
```

Every major factual claim should have:

- source URL
- date checked
- short evidence
- confidence level

Example:

```md
## folk

Source:
https://www.folk.app/

Checked:
2026-09-27

Finding:
folk provides AI-powered follow-up capabilities that identify inactive conversations and suggest follow-up actions.

Confidence:
High
```

---

# 35. Customer Research Database

Create:

```text
/research/customer-interviews.md
```

For every interview:

```text
Interview ID
Date
ICP
Business type
Number of clients
Current tools
Pain described
Actual example
Current workaround
Financial impact
Frequency
Existing solution
Reaction to concept
Willingness to test
Important quote
```

Do not fabricate interview data.

---

# 36. Evidence Rules

Separate:

### FACT

Directly supported by source/user data.

### HYPOTHESIS

An idea that still needs validation.

### ASSUMPTION

Something currently believed but unverified.

### DECISION

A deliberate product decision.

### EXPERIMENT

A test designed to validate/refute a hypothesis.

Use these labels throughout research.

---

# 37. Anti-Bias Rule

Claude must actively search for evidence that the idea is BAD.

Do not only search for confirmation.

For every major thesis ask:

> "What evidence would prove this product is unnecessary?"

Look for:

- customers already solve it easily
- existing CRM features are enough
- users do not have enough historical data
- users do not trust AI with customer conversations
- reactivation rate is too low
- users don't want another tool
- willingness to pay is weak
- problem occurs too infrequently
- integration complexity destroys margins

If evidence is weak, say so.

---

# 38. Build Gate

DO NOT BUILD MVP until these conditions are reasonably supported:

### Gate A — Problem

Real customers describe the problem without being led.

### Gate B — Frequency

Problem happens often enough to matter.

### Gate C — Value

There is meaningful commercial value in solving it.

### Gate D — Current workaround

Customers currently use spreadsheets, reminders, CRM, memory, manual search, etc.

### Gate E — Gap

Existing solutions do not fully solve the specific problem.

### Gate F — Trust

Users are comfortable enough with AI analyzing relevant business history.

### Gate G — Willingness

At least some target users are willing to test/pay.

---

# 39. Suggested Execution Phases

## PHASE 1 — Market Validation

Status:

**NOT STARTED / IN PROGRESS**

Tasks:

- competitor research
- customer pain research
- Reddit/community research
- pricing research
- existing solution mapping
- identify gaps
- document hypotheses

Output:

```text
/research/*
```

---

## PHASE 2 — Founder Dataset Experiment

Tasks:

- collect 50 historical contacts
- normalize data
- analyze relationships
- manually validate AI output
- calculate opportunity counts
- calculate historical value
- identify false positives
- identify false negatives

Output:

```text
/research/founder-data-test.md
```

Decision:

```text
CONTINUE
or
PIVOT
```

---

## PHASE 3 — Customer Discovery

Tasks:

- recruit 10–20 ICP users
- conduct interviews
- document actual stories
- identify repeated pain
- compare current workflows
- test product concept
- test positioning

Output:

```text
/research/customer-interviews.md
/research/customer-discovery-summary.md
```

---

## PHASE 4 — Concierge MVP

Do NOT build full SaaS yet.

Offer manual service:

```text
Customer uploads CSV
        ↓
System/manual analysis
        ↓
Return:
- dormant opportunities
- reasons
- recommended actions
- message drafts
```

Goal:

Prove users actually act on recommendations.

---

## PHASE 5 — Lightweight SaaS MVP

Only after concierge validation.

Build:

- authentication
- CSV upload
- contact normalization
- opportunity analysis
- dashboard
- explanation
- message drafts
- human approval
- basic history
- basic billing if needed

---

## PHASE 6 — First Integration

Add Google Sheets or Gmail.

Choose based on customer discovery data.

Do NOT add integrations simply because they sound useful.

---

## PHASE 7 — Coretex Integration

If the product proves useful:

```text
Coretex CRM
      ↓
Relationship Intelligence
      ↓
Reactivation Opportunities
```

Potential strategic advantage:

Coretex users already have structured customer history.

---

# 40. Claude Code Working Rules

Claude must:

1. Read this file before major product decisions.
2. Never skip validation gates.
3. Never start large-scale coding because the idea sounds good.
4. Keep research and implementation separate.
5. Maintain a decision log.
6. Maintain a changelog.
7. Record assumptions.
8. Record rejected ideas.
9. Use current web research for current market facts.
10. Cite sources in research files.
11. Never fabricate customer research.
12. Never fabricate competitor features.
13. Never fabricate pricing.
14. Never claim product-market fit.
15. Prefer the simplest architecture.
16. Ask for user approval before destructive changes.
17. Keep code modular.
18. Write tests for important business logic.
19. Protect API keys and secrets.
20. Never commit secrets to Git.

---

# 41. Decision Log

Create:

```text
DECISIONS.md
```

Format:

```md
## Decision: Focus on dormant client reactivation

Date:
2026-09-27

Status:
Hypothesis

Reason:
Founder pain + initial market research suggests a potential gap between generic follow-up reminders and deeper relationship reactivation intelligence.

Evidence:
[List sources]

Still needs:
Customer validation.
```

Every major product decision should follow this format.

---

# 42. Product Hypotheses To Test

Maintain:

```text
HYPOTHESES.md
```

Initial hypotheses:

### H1
Small service businesses have valuable dormant client relationships.

### H2
They do not systematically identify which dormant relationships are worth reconnecting with.

### H3
The reason/context for reactivation is more valuable than a simple reminder.

### H4
Users want AI to prepare the recommendation and message, but want human approval before sending.

### H5
CSV/Google Sheet input is enough to demonstrate initial value.

### H6
Users may pay around ₹999/month if the product consistently surfaces useful opportunities.

### H7
Post-sale client reactivation may be a stronger wedge than generic lead follow-up.

### H8
Coretex CRM can eventually become a strong data source/integration.

Every hypothesis must eventually be:

```text
Validated
Invalidated
Partially validated
Still unknown
```

---

# 43. Current Product Positioning Candidates

Do not finalize yet.

### Option A

> **Your old clients are your next leads.**

### Option B

> **Find the clients worth reconnecting with.**

### Option C

> **Never let valuable client relationships go cold.**

### Option D

> **AI that finds the business opportunities hiding in your old relationships.**

### Option E

> **Don't remind me. Tell me who needs my attention.**

Test these with real customers.

---

# 44. Potential Product Names

Do not register/build branding around these yet.

Possible working names:

- Reactivate
- Reconnect AI
- ClientPulse
- Revive
- Relate
- Revival
- Reclaim
- LoopBack
- ClientLoop
- RevenueLoop
- WarmBack
- ReconnectOS

Name selection comes AFTER product validation.

---

# 45. Future Product Expansion

If the core product works:

```text
Dormant Client Reactivation
        ↓
Relationship Intelligence
        ↓
Revenue Recovery
        ↓
Customer Retention
        ↓
Renewal Detection
        ↓
Upsell Opportunities
        ↓
Referral Opportunities
        ↓
Relationship Health
```

Potential future insight:

> "Your relationship with this customer is becoming weaker."

But this should come later.

---

# 46. Long-Term Vision

Potential long-term product:

## Business Relationship Intelligence Layer

Instead of becoming another CRM, the product sits above existing business tools.

```text
CRM
Gmail
Calendar
WhatsApp
Sheets
Payments
E-commerce
Forms
        ↓
RELATIONSHIP INTELLIGENCE
        ↓
What needs attention?
Why?
Why now?
What should I do?
What should I say?
        ↓
Human approval
        ↓
Action
```

This is the larger vision.

But the first product should solve ONE painful problem.

---

# 47. Immediate Next Actions

Claude should perform these in order.

## Step 1

Review this entire file.

## Step 2

Create:

```text
/research/market.md
/research/competitors.md
/research/customer-pain.md
/research/opportunity-gaps.md
/research/pricing.md
HYPOTHESES.md
DECISIONS.md
```

## Step 3

Perform fresh competitor and market research.

## Step 4

Find at least 10 concrete examples of customer pain.

## Step 5

Find evidence AGAINST the product thesis.

## Step 6

Create a competitor comparison.

## Step 7

Identify the strongest defensible product wedge.

## Step 8

Create the founder 50-contact dataset template.

## Step 9

Create the customer interview questionnaire.

## Step 10

STOP.

Do not build the SaaS yet.

Wait for validation data.

---

# 48. Definition of "Ready to Build"

Claude may recommend moving to development only when the evidence supports:

```text
Problem = real
Frequency = sufficient
Value = meaningful
Current workaround = painful
Competition = understood
Differentiation = plausible
User trust = acceptable
Willingness to test/pay = demonstrated
```

Even then, start with the smallest possible MVP.

---

# 49. Final Instruction To Claude

The most important rule:

> **Do not fall in love with the idea. Find out whether customers actually care.**

Your job is not to make the product sound exciting.

Your job is to discover:

1. Is this a real problem?
2. Who experiences it most?
3. How frequently?
4. What does it cost them?
5. How do they solve it today?
6. Why are existing products insufficient?
7. What would make them switch?
8. What is the smallest product that creates measurable value?
9. Will they use it repeatedly?
10. Will they pay for it?

If evidence says the current idea is weak, propose a better adjacent problem.

If evidence says the idea is strong, define the smallest possible product and only then start building.

---

# 50. Founder Context

Founder:

**Meraj**

Relevant existing products:

- Meraj Tech Services
- Coretex CRM
- Coretex Lead Dashboard

Technical environment:

- Windows PC
- Claude Code
- Antigravity
- n8n
- Hostinger
- AWS/VPS where required
- PHP/MySQL experience through existing projects
- AI-assisted development

Founder preference:

- simple
- practical
- low operational complexity
- AI-assisted
- recurring SaaS revenue
- personally usable product
- strong real-world pain
- no unnecessary features

The founder is a marketer/product thinker and beginner-to-intermediate developer using AI-assisted coding.

Therefore Claude should explain important technical decisions clearly and avoid unnecessary engineering complexity.

---

# END OF MASTER PLAN
