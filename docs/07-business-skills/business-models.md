# Business Models

Your business model determines what your product needs to do to create *and capture* value. Most PM decisions look different depending on the business model. Understanding yours deeply — and the tradeoffs built into it — is fundamental to good product strategy.

## The main B2B SaaS models

### Subscription (per seat)
**How it works:** Charge per user per month/year.

**Implications for product:**
- Growing seat count is a primary success metric
- Features that increase collaboration (more users in the product) are strategic
- Seat reduction (workflow automation) can hurt revenue even if it's good for users
- Expansion revenue comes from seat growth

**Drawback:** Misaligned with value — a team of 5 that gets enormous value pays the same as a team of 5 that barely uses it.

### Usage-based (consumption)
**How it works:** Charge per API call, transaction, GB processed, email sent, etc.

**Implications for product:**
- Usage volume is a primary revenue driver
- Features that increase legitimate usage are strategic
- Features that help users use less of the product are complex tradeoffs
- Revenue is more variable and harder to predict

**Who uses it:** Stripe, AWS, Snowflake, Twilio.

### Outcome-based
**How it works:** Charge as a percentage of value created (e.g., % of revenue generated, % of cost saved).

**Implications for product:**
- Product must produce measurable, attributable outcomes
- Attribution is a product problem as much as a marketing problem
- Builds natural alignment between vendor and customer

**Drawback:** Revenue is dependent on customer outcomes you don't fully control.

### Freemium
**How it works:** Core product is free; advanced features or usage above a threshold is paid.

**Implications for product:**
- Activation of free users is critical — if they don't activate, they don't convert
- The "aha moment" must happen on the free tier
- The free-to-paid value gate must be obvious and compelling
- Free tier costs (infrastructure, support) must be manageable

**Who uses it:** Slack, Notion, Figma, Linear.

### Marketplace (two-sided)
**How it works:** Platform connects two groups (buyers/sellers, hosts/guests); take a percentage of transactions.

**Implications for product:**
- Chicken-and-egg problem at launch (need both sides to have value)
- Supply quality as much as supply quantity matters
- Trust and safety are product requirements, not features
- Two sets of customers with different needs, both served by the same product

## How the business model shapes your backlog

This is the insight PMs often miss.

**Per seat:** A feature that enables collaboration between teams → directly supports seat expansion → high strategic value. A feature that consolidates workflows, reducing the need for multiple seat holders → dangerous to revenue even if good for users.

**Usage-based:** A feature that increases legitimate, valuable usage → revenue-positive. A feature that reduces redundant usage (e.g., smarter caching) → revenue-negative but value-positive. This creates real tension: build the efficient thing or the revenue-generating thing?

**Freemium:** A feature that's valuable but easy to include in the free tier → might not drive conversion. A feature that serves serious users → put it in the paid tier to create an upgrade moment.

**Marketplace:** A feature that improves trust and safety → foundational; can't be deprioritized. A feature that serves buyers but hurts suppliers → zero-sum; requires careful analysis.

When you're making a prioritization decision, run it through the business model lens: does this feature support or work against our revenue mechanism?

## Platform thinking

Many successful products eventually become platforms — they open APIs and build ecosystems of partners and integrations. This changes the business model fundamentally.

**When to go platform:**
- You have a core product that customers love but can't customize enough
- Third-party developers would build valuable integrations if they could
- The ecosystem itself creates competitive moat (switching costs go up as integrations proliferate)
- You want to leverage external developer capacity you can't hire

**The platform paradox:** Opening a platform accelerates growth but creates dependencies. Partners build on your APIs; you can't change them without breaking partners. APIs are commitments.

**PM implications:** API design is product design. Bad API decisions compound over years. Before opening an API, think carefully about the abstraction, the versioning strategy, and what you're committing to.

## Recurring revenue mechanics

Regardless of business model, most SaaS companies measure health through a set of recurring revenue metrics:

| Metric | What it measures |
|--------|----------------|
| **ARR** | Annual recurring revenue — normalized revenue run rate |
| **MRR** | Monthly recurring revenue |
| **Expansion MRR** | New revenue from existing accounts (upsells, seat adds) |
| **Churn MRR** | Revenue lost from cancellations |
| **Contraction MRR** | Revenue lost from downgrades |
| **NRR (Net Revenue Retention)** | (Starting MRR + Expansion − Churn − Contraction) / Starting MRR |

**NRR is the most important SaaS health metric.** An NRR above 100% means existing customers are growing faster than they're churning — the business grows even without new customer acquisition.

PMs who understand their company's NRR and can connect their product decisions to it are far more influential in strategic conversations.

## Next steps

- [Finance & P&L](finance-and-pl.md) — how these metrics show up in financial planning
- [Unit Economics](unit-economics.md) — the per-customer math
- [Pricing & Packaging](../05-go-to-market/pricing-and-packaging.md) — setting the price that reflects the model
