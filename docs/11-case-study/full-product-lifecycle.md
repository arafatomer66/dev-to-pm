# A Full Product Lifecycle

*Claros Analytics — 18 months, every concept in this knowledge base. B2B SaaS, mid-market finance teams.*

---

## The concept coverage map

This case study deliberately hits every major topic in the curriculum. Use this map to find the concepts you care about:

| Concept | Month(s) |
|---------|---------|
| Product vision & strategy | 1 |
| Market analysis & competitive intelligence | 1–2 |
| OKRs & metrics | 1, 7, 13 |
| Positioning | 2 |
| Discovery & user research | 2–3 |
| PRD writing | 3, 8 |
| Prioritization | 4, 10 |
| Stakeholder management | Throughout |
| Go-to-market & launch | 6, 11 |
| Pricing & packaging | 7 |
| Working with engineering | 3, 8 |
| Working with design | 5 |
| Working with sales | 4, 9 |
| Working with leadership | 7, 13 |
| Business models & unit economics | 7 |
| Launch crisis | 11 |
| Data-driven decisions | 12 |
| Platform strategy | 13 |
| Product sunset | 17 |
| Career pitfalls (meta) | Throughout |

---

## The company: Claros Analytics

**What it is:** B2B SaaS analytics platform for mid-market finance teams. Connects to ERPs, CRMs, and data warehouses to produce automated financial reports.

**Where we start:** $6M ARR, 150 customers, 20-person company. Two PMs. You own the core analytics product.

---

## Month 1: Strategy Reset

### The situation

Q2 ended with NRR at 92% — the business is leaking. Customers are using the core report builder but churning at 18-month mark when they've outgrown the default templates. Larger customers want custom KPIs; the product doesn't support it.

At the same time, Competitor X just launched an AI-powered "report writing" feature that's generating buzz. Three prospects have mentioned it in sales calls.

### The strategic question

Do you: (a) double down on mid-market finance teams and close the customization gap, or (b) chase the AI feature and try to match the competitor's new angle?

**You do the analysis:**

Market analysis: mid-market finance teams represent a $1.2B SAM. Enterprise finance is adjacent but requires 3–4x the engineering investment in security, compliance, and admin tooling.

Competitive intelligence: Competitor X's AI feature generates reports from natural language prompts. Impressive demo. You talk to two ex-customers of theirs who tested it: "It creates reports but they need significant cleanup. Not reliable enough for board-level presentations."

Win/loss review: Your last 10 losses — 7 were to Competitor X. Reason: they have a custom KPI builder. 3 were to spreadsheets.

**The diagnosis:** You're losing to Competitor X not because of AI — because you can't build custom KPIs. The AI feature is noise; the customization gap is the real threat.

**The strategy memo you write:**

> *Diagnosis: We're losing mid-market deals because our report customization is limited to pre-built templates. Customers who outgrow the defaults either build workarounds or churn to Competitor X.*
>
> *Guiding policy: Close the customization gap for mid-market finance teams before expanding scope. We will not chase AI features until our core value proposition is defensible.*
>
> *This quarter's priorities: (1) Custom KPI builder, (2) Report scheduling (already in flight), (3) Discovery on what "expanding scope" means for year 2.*

Leadership aligns. The roadmap is set.

---

## Month 2: Discovery

### Research sprint

You spend 3 weeks in discovery before writing a single PRD. The question: what does "customization" mean to mid-market finance teams, and what's the minimum version that creates real value?

You run 12 customer interviews. Target mix:
- 4 active power users (what are they doing today?)
- 4 churned customers (why did they leave?)
- 4 prospects who chose Competitor X (what specifically did they choose it for?)

**What you find:**

From churned customers: 3 of 4 churned because they needed KPIs specific to their business. "We needed to track days sales outstanding differently than how your standard DSO is calculated. We had to maintain it manually."

From Competitor X adopters: "The custom formula builder is the reason we chose them. It's not pretty but it works."

From power users: "I've hacked around this with calculated columns in Excel that I then import. It's a nightmare."

**JTBD:** *When I need to report on finance metrics specific to our business model, I want to define and consistently calculate those metrics in one place, so I can stop maintaining parallel spreadsheets and trust that everyone is looking at the same numbers.*

**The insight that matters:** The problem is not that they want arbitrary custom reports. It's that they need to define business-specific calculated fields that flow through into all their existing reports.

This is different from "a full custom report builder." It's a KPI definition layer — smaller scope, same outcome.

---

## Month 3: The PRD

### Custom KPI Engine

Working with Priya (tech lead) and Maya (lead designer), you develop the concept:

Users can define custom KPIs with a formula editor (referencing existing data fields), and those KPIs appear as first-class metrics in all standard reports.

**PRD decisions:**

In scope:
- KPI formula editor with field autocomplete
- KPI library (saved, reusable)
- KPIs surfaced in existing report templates
- Team-level KPIs (admin creates, team uses)

Out of scope:
- Cross-company KPI sharing (future)
- AI-generated formulas (future)
- Custom chart types (separate work item)

**Engineering challenge:** Priya flags that the formula validation (preventing circular references, type errors) is complex. Estimate: 14 weeks.

**Negotiation:** You and Priya design a "Phase 1 KPI engine" with a limited formula syntax (arithmetic operations only, no functions), reducing it to 9 weeks. Phase 2 adds functions in Q4.

**The PRD is approved.** Build begins.

---

## Month 4: Working Cross-Functionally

### Sales tension

Marcus (AE) pings you: "We have a deal with a manufacturing company. They need the custom KPI thing. Can we promise it in 8 weeks?"

9-week build, 8-week ask. You do the math: possible if the sprint goes well, risky if it doesn't.

**Your response:** "I can't commit to 8 weeks — it's a 9-week build on a good day. If we hit any technical complexity, it slips. What I can do: get them on a design partner program where they test the beta version. If it's 90% of what they need, does that close the deal?"

Marcus checks with the prospect. They agree to design partner status. Deal closes at $55K.

**This wins two ways:** Revenue now, and valuable beta feedback built into the process.

---

## Month 5: Design Review

Maya shares mockups for the KPI editor. The formula editor UX is complex — a text field with autocomplete and a results preview panel.

**Your feedback process:**

In the first design review, you ask questions before giving opinions:
- "What happens when the formula has a syntax error?"
- "How does a non-technical user know which fields are available?"
- "What does the experience look like for a viewer of a report that uses a custom KPI — do they see any indication it's custom?"

Maya has answers for 2 of 3. The third ("indicator for custom KPIs") she hadn't thought about. You agree it's important but out of scope for MVP — you note it as a Phase 2 item.

**Your one substantive redirect:** The preview panel shows the formula result for the last 30 days of data. You ask: "Can we make the time range configurable? Finance teams often validate by checking a specific month they know the number for." Maya makes it configurable. 2-day change.

---

## Month 6: Launch of Report Scheduling (Parallel Track)

While KPI Engine is in development, Report Scheduling (from the earlier case study) launches. You're managing two trains simultaneously.

**Report scheduling outcome, 4 weeks post-launch:**
- 42% of accounts with an active schedule
- Two deals referenced it in close notes
- NRR for the 40 manual-weekly accounts: up 4% vs. the control group

The churn signal hasn't fully resolved yet, but the leading indicators are positive.

---

## Month 7: Pricing Review

### The business conversation

Your CEO, Sarah, reviews Q3 financials. NRR has improved to 96% (up from 92%). But CAC has increased 30% — sales cycles are longer because prospects need to evaluate customization depth.

Sarah calls a product + finance review. The CFO presents: "We need to either increase ACV or reduce CAC. Our unit economics only work at this growth rate if one of those moves."

**You're asked:** "How does the product support a pricing change?"

You prepare:
- Current pricing: $400/month flat for all tiers
- Custom KPI Engine is launching in 6 weeks
- Competitive positioning: Competitor X charges more for their custom KPI features

**Your analysis:** The Custom KPI Engine creates a natural tier boundary. Basic analytics (current product) suits small finance teams. Custom KPIs + advanced scheduling suits mid-market teams with specific requirements. This is a legitimate value gate.

**Proposed packaging:**

| Tier | Price | What's included |
|------|-------|----------------|
| Starter | $300/month | Core reports, standard KPIs, 3 users |
| Professional | $600/month | + Custom KPIs, scheduled delivery, 10 users |
| Enterprise | Custom | + SSO, audit logs, custom integrations |

**The business case:** Average deal size increases from $400 to $550 (most customers upgrade to Professional). NRR improves because the value gate creates a natural upsell path for growing teams.

Sarah approves. You coordinate with Finance and Sales on the transition plan for existing customers.

---

## Month 8: KPI Engine Launch Prep

### Design partner feedback

Manufacturing company (the Month 4 deal) has been using beta for 3 weeks. Their CFO's feedback: "The formula builder is great but we can't share KPI definitions with our team without them being able to accidentally edit them."

You hadn't scoped read-only KPI access for contributors (non-admins). It's a legitimate gap.

**Decision:** Scope it into launch. Priya estimates 4 days. You add it — it's a table-stakes capability for the B2B use case.

**Second design partner feedback:** "The autocomplete shows too many fields. We need a way to organize them."

This one you push to Phase 2. The feature list organization is useful but not blocking launch.

---

## Month 9: Sales Enablement

You spend a week on sales enablement before the KPI Engine launch:

- One-page battlecard for Competitor X: "What Claros Custom KPIs do vs. what Competitor X's formula builder does"
- Demo script with 3 sample KPIs relevant to different industries
- Email to AEs: "Here's what changed, here's the talking point, here's the deal you can reference"

Marcus runs the first post-launch demo with a new prospect. He reports: "This was the best product demo we've had in six months. Prospect asked to start a trial on the call."

---

## Month 10: Prioritization Under Pressure

### The pressure

Two things happen in the same week:

1. The board asks Sarah to present an enterprise go-to-market plan. This creates pressure to fast-track SSO and audit log capabilities — enterprise prerequisites.

2. A key customer, RetailCo, escalates through their CS manager: "We've hit a limit on how many custom KPIs we can create (you capped it at 50). We're going to churn if this isn't resolved."

**Triaging the two:**

SSO/audit logs: 12-week minimum investment. Not critical to current revenue. Relevant to a market segment (enterprise) you haven't formally entered.

RetailCo limit increase: 3-hour code change. Direct churn risk on a $40K account.

**Decision:** Fix RetailCo immediately (it's 3 hours). SSO/audit logs go on the roadmap for H1 next year with a genuine strategy discussion — not a knee-jerk enterprise pivot.

You write a "what we're not doing in Q4 and why" doc that explicitly documents the enterprise decision with the reasoning. This document is shared with leadership and becomes the anchor for Q4 planning.

---

## Month 11: The Launch Crisis

### Enterprise KPI goes to 100%

KPI Engine is fully rolled out. 58% account adoption (above 40% target). NRR tracking to 104% for the first time in 18 months.

Then: an incident.

**What happened:** A customer's scheduled report failed silently on Monday morning. Their CFO walked into a board meeting without their weekly financials. CS gets an angry call. You hear about it 6 hours after it happened because the support ticket wasn't escalated properly.

**The post-mortem:**
- Silent failure (no notification when scheduled report fails) — this was a known gap you had deferred
- Escalation path was unclear — CS didn't know to loop in PM immediately for a customer of this size
- No monitoring on scheduled report execution failure rate

**Your response:**
1. PM the emergency fix: add failure notifications. Priya ships it in 48 hours.
2. Acknowledge to the customer — you call them personally (not email). They're frustrated but appreciate the directness.
3. Build the monitoring dashboard and set alert thresholds.
4. Write an incident post-mortem that you share with leadership — including what you deprioritized and why.

**The cultural moment:** How you handle this builds trust with the team and leadership. Hiding it or minimizing it would have done the opposite.

---

## Month 12: Data-Driven Course Correction

### The Q3 outcome review

At the quarterly review, you pull the data:

| Metric | Target | Actual |
|--------|--------|--------|
| Custom KPI adoption (accounts) | 40% | 58% |
| NRR | 100% | 104% |
| Deals citing custom KPIs | 15 | 22 |
| Churn reduction (q/q) | 5% | 8% |
| New enterprise leads | 10 | 4 |

Enterprise leads underperformed. The analysis: you haven't done meaningful enterprise marketing, and SSO (not yet built) is blocking deals at a certain size.

**The data-driven conclusion:** The Q3 strategy was right. The next bet is clear: SSO + audit logs to unlock the enterprise segment, with pricing to match. But you're not chasing enterprise until the core mid-market motion is defended.

---

## Month 13: Platform Strategy

### The API conversation

Three customers in the last month have asked: "Can we pull our custom KPI data into our own data warehouse?" They're building internal reporting on top of Claros.

You have a conversation with Priya and your CTO about a public API.

**The analysis:**
- Pro: Customers with API access have 40% lower churn (from competitor's public case study data)
- Pro: Opens a developer ecosystem and partner integrations
- Con: APIs are commitments. Every endpoint you publish is a contract.
- Con: 8–10 weeks of engineering to build a stable, versioned API

**Decision:** Build a private beta API for 5 customers who've explicitly asked. Learn what they actually need before publishing a public API contract.

This is platform strategy done right: validate the use cases before locking in the abstraction.

---

## Month 14–16: Enterprise Motion

SSO and audit logs ship. You close your first three enterprise accounts (500+ employees). Enterprise onboarding is harder — longer sales cycles, security reviews, custom contract terms.

You hire a Customer Success Manager specifically for enterprise — the PM-to-customer ratio at enterprise scale requires dedicated relationship management that CS provides better than PM.

NRR reaches 112% by end of Month 16. New ARR from enterprise is 20% of new bookings.

---

## Month 17: Product Sunset

### The legacy report builder

The original Claros report builder — the one that shipped in V1 — is now being used by fewer than 12% of customers. The new custom KPI + report scheduling combination has superseded it for almost everyone.

But migrating those 12% is complex: they have saved reports in the old format that would break with a migration.

**The sunset decision:**

You do the math:
- Engineering time maintaining legacy builder: ~0.5 engineer-week per month
- Customers on legacy: 22 accounts (~15% of total by count, ~8% of revenue)
- Migration complexity: medium — a migration script exists but requires manual validation per account

**Options:**
1. Keep legacy indefinitely
2. Force migration with 90-day notice
3. Offer assisted migration as a CS project, then deprecate

**Decision:** Option 3. You work with CS to personally reach out to each of the 22 accounts, offer a 1-hour migration call, and set a 6-month deprecation timeline.

Result: 18 of 22 migrate. 3 churn (they were already considering it). 1 gets an extension for a legitimate operational reason.

**The sunset is completed 6 months later.** The legacy codebase is deleted. The team is visibly relieved.

---

## Month 18: Looking Back

### Where Claros is now

- ARR: $18M (3x growth in 18 months)
- NRR: 115%
- Customers: 310
- Team: 35 people

**What moved the needle:**
1. Closing the customization gap before chasing AI features
2. Pricing change that created a natural value gate
3. Enterprise prerequisites (SSO) that opened a new segment
4. Proactive customer communication through the incidents

**What you'd do differently:**
- Earlier discovery on the custom KPI use case (started reactive, should have been proactive)
- The scheduled report silent failure was a known gap — should have been in the original scope
- API decision: should have done the beta sooner

---

## Concept coverage map (revisited)

*Every major concept in the curriculum appeared in this lifecycle:*

| Module | Appeared in |
|--------|------------|
| Product strategy (diagnosis/policy/actions) | Month 1 |
| Market analysis | Month 1–2 |
| Competitive intelligence | Month 1 |
| OKRs & metrics | Month 1, 7, 12 |
| Positioning & differentiation | Month 2 |
| Discovery & validation | Month 2 |
| User research | Month 2 |
| Personas & JTBD | Month 2 |
| PRD writing | Month 3 |
| Working with engineers | Month 3, 5, 8 |
| Working with design | Month 5 |
| Working with sales | Month 4, 9 |
| Working with leadership | Month 7, 10, 13 |
| Negotiation | Month 3, 4 |
| Roadmapping | Month 1, 10 |
| Prioritization | Month 4, 10 |
| Pricing & packaging | Month 7 |
| Launch planning | Month 8, 9 |
| Working with marketing | Month 9 |
| MVPs & experiments | Month 13 (API beta) |
| Metrics & analytics | Month 6, 12 |
| Business models | Month 7 |
| Finance & P&L | Month 7 |
| Unit economics | Month 7 |
| Platform strategy | Month 13 |
| B2B special context | Throughout |
| Common pitfalls (and avoiding them) | Month 4, 7, 10, 11 |

---

*This is what a real product career looks like. Not a clean arc — a series of decisions made with incomplete information, some right, some wrong, all learned from.*
