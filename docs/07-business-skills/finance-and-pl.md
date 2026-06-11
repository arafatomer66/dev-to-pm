# Finance & P&L

PMs who understand the financial picture of their product are dramatically more influential in strategic conversations. You don't need to be a CFO. You need to understand how product decisions show up as numbers that matter to the business.

## The financial metrics that matter for PMs

### Revenue metrics

**ARR (Annual Recurring Revenue):** The normalized annualized value of your subscription contracts. A $500/month contract = $6,000 ARR.

**MRR (Monthly Recurring Revenue):** ARR / 12. The monthly pulse.

**Expansion MRR:** New revenue from existing customers — upsells, seat additions, tier upgrades. Reflects product satisfaction and growth from current base.

**Churn MRR:** Revenue lost from customers who cancel. The most direct product health signal.

**NRR (Net Revenue Retention):** The percentage of last period's revenue retained plus expansion, minus churn and contraction.
```
NRR = (Beginning MRR + Expansion − Churn − Contraction) / Beginning MRR × 100
```
NRR > 100% = you grow even without new customers. NRR < 100% = you're losing ground.

### Customer metrics

**CAC (Customer Acquisition Cost):** Total cost of acquiring one new customer (sales + marketing spend / new customers acquired).

**LTV (Lifetime Value):** Total revenue expected from a customer over their lifetime with you.
```
LTV = Average Revenue Per Account × Gross Margin % / Churn Rate
```

**LTV:CAC ratio:** How efficiently you're acquiring customers. Rule of thumb: LTV:CAC > 3:1 is healthy for a SaaS business. < 1:1 means you lose money on every customer.

**Payback period:** How many months until the CAC is recovered from the customer's gross profit contribution. 12–18 months is typical for healthy SaaS; enterprise products often run longer.

## How product decisions affect the P&L

PMs who can think in these terms have much stronger strategic conversations.

**Improving activation rate:**
Better activation → more customers reach the "aha moment" → higher 30-day retention → lower early churn → higher LTV per acquired customer → better LTV:CAC.

**Adding enterprise features (SSO, audit logs, compliance):**
Enterprise features → larger deal sizes → higher ACV → potentially higher LTV if churn rates are similar → worth the engineering investment if the TAM supports it.

**Building a self-serve motion:**
Lower CAC (no sales involvement) → better unit economics for smaller customers → but potentially lower ACV and different churn profiles. Analyze the math before betting the roadmap on PLG.

**Shipping a workflow automation feature:**
Users save time → higher satisfaction → lower churn → higher LTV. But potentially reduces seat count in per-seat pricing model. Both effects are real; model them explicitly.

## Gross margin

Gross margin = (Revenue − Cost of Goods Sold) / Revenue

For software, COGS includes:
- Hosting and infrastructure
- Third-party SaaS costs (APIs, services)
- Customer support costs directly tied to delivery
- Sometimes: professional services, customer success costs

Healthy B2B SaaS gross margins are 70–85%. Gross margin matters for PMs because:
- Infrastructure-heavy features (large file storage, ML inference, video processing) reduce gross margin
- Support-heavy features (complex workflows, poor UX) increase COGS via support load
- Self-serve features improve gross margin by reducing CS labor

A feature that costs $50K to build but increases monthly infrastructure costs by $5K is a different investment than a feature that costs $50K to build with negligible infrastructure cost.

## How to make a financial product case

When you're requesting resources for a major initiative, frame it financially.

**Template:**
```
Investment required: [Engineering months] × [$avg_engineer_cost] = $[total]

Expected outcome: 
- Increase in NRR from X% to Y% = $[annual_impact_on_revenue]
- OR: Reduction in churn from X% to Y% = $[retained_revenue]
- OR: New segment revenue: [estimated new ARR from new ICP]

Timeline to ROI: [months to break even on investment]

Key assumptions:
- [Assumption 1 and confidence level]
- [Assumption 2 and confidence level]

What would invalidate this:
- [Signal that would tell us the hypothesis was wrong]
```

This is not a business school exercise — it's a practical communication tool that gets PMs taken seriously in resource conversations.

## Working with finance

Finance teams run the planning and budgeting cycle that determines how many engineers your team has. PMs who build a relationship with finance get better outcomes than PMs who see finance as a barrier.

**What finance needs from PM:**
- Honest revenue projections with explicit assumptions (not hockey-stick optimism)
- Upside scenarios with what would need to be true for them to materialize
- Risk identification — what could go wrong and how big is the downside?

**What PM can learn from finance:**
- Which product areas have the best unit economics
- Where the company is burning cash relative to return
- Seasonal patterns in the business
- What metrics the board cares about most

## Next steps

- [Unit Economics](unit-economics.md) — the per-customer math in more detail
- [Business Models](business-models.md) — how the model connects to the P&L
- [Strategy Frameworks](strategy-frameworks.md) — tools for strategic thinking with financial grounding
