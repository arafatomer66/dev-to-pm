# Unit Economics

Unit economics is the analysis of revenue and costs at the per-customer (or per-transaction) level. It answers the fundamental question: does each customer make us money, and how much?

## The core equation

```
Unit Economics = LTV − CAC

Healthy if: LTV > 3× CAC, and CAC payback < 18 months
```

If LTV < CAC, you lose money on every customer. No amount of growth fixes this without fundamentally changing the product, pricing, or cost structure.

## LTV in detail

**LTV = Average Revenue Per Account (ARPA) × Gross Margin % ÷ Churn Rate**

Example:
- ARPA: $500/month
- Gross margin: 75%
- Monthly churn: 2%

LTV = $500 × 0.75 ÷ 0.02 = **$18,750**

**Key drivers PMs can influence:**

| Driver | Product levers |
|--------|---------------|
| ↑ ARPA | Features that enable upsell; tier design that creates upgrade moments |
| ↑ Gross margin | Self-serve features; reduced support load; efficient infrastructure |
| ↓ Churn rate | Core value delivery; onboarding quality; feature stickiness |

The most powerful LTV lever is **churn reduction**. Because churn appears in the denominator, even a small improvement has outsized impact:
- 2% monthly churn → LTV = ARPA × GM% ÷ 0.02 = 50× monthly ARPA
- 1% monthly churn → LTV = ARPA × GM% ÷ 0.01 = 100× monthly ARPA

Cutting churn in half doubles LTV.

## CAC in detail

**CAC = (Total Sales + Marketing Spend) ÷ New Customers Acquired**

Example:
- Monthly sales + marketing spend: $100,000
- New customers acquired: 50

CAC = $100,000 ÷ 50 = **$2,000**

**Blended vs. segmented CAC:** Blended CAC averages across all channels. Segmented CAC reveals which channels are efficient (organic, product-led) vs. expensive (outbound sales, paid ads).

Product-led growth (PLG) dramatically lowers CAC by having users self-discover and self-serve through the product. The engineering investment in PLG is justified by the CAC reduction.

## CAC payback period

```
CAC Payback = CAC ÷ (ARPA × Gross Margin %)
```

Using our example:
- CAC: $2,000
- ARPA: $500
- GM: 75%

CAC Payback = $2,000 ÷ ($500 × 0.75) = **5.3 months**

This is excellent. If payback were 24 months, the business would need to survive 2 years before seeing a return on each customer.

## How to use unit economics in product decisions

### Evaluating a new customer segment

If you're considering a downmarket move (targeting smaller customers at lower price points):

Current: ARPA $1,000, CAC $5,000, churn 1.5% → LTV = $50,000, Payback 6.7 months
Proposed SMB: ARPA $200, CAC $500, churn 4% → LTV = $3,750, Payback 3.1 months

The SMB has worse LTV but better payback period. Whether it's worth doing depends on volume — can you get enough SMB customers to make the revenue meaningful without drowning CS and support?

### Evaluating a self-serve investment

Engineering investment: $200K (2 engineers × 3 months)
Expected impact: 50% reduction in CAC for bottom half of ACV range (from $3K to $1.5K) for 100 customers/month

Monthly CAC savings: 100 customers × $1,500 saved = $150,000/month
ROI: $200K investment paid back in 1.3 months

This is an easy case. Most aren't this clean, but the framework applies.

### Evaluating a churn reduction feature

Feature investment: $150K
Expected impact: Reduce monthly churn from 2.5% to 2.0% on a base of 500 customers paying $600/month average

Revenue saved per month = 0.5% × 500 × $600 = $1,500/month
Time to payback = $150K ÷ $1,500/month = 100 months

At this scale, not a compelling financial case. But at 5,000 customers:
Revenue saved per month = 0.5% × 5,000 × $600 = $15,000/month
Time to payback = $150K ÷ $15,000/month = 10 months

Scale changes the math significantly. Unit economics arguments for churn reduction often strengthen as the customer base grows.

## NRR: the aggregate unit economics signal

Net Revenue Retention (NRR) is the most important summary metric for B2B SaaS unit economics. It captures churn, expansion, and contraction in a single number.

| NRR | What it signals |
|-----|----------------|
| > 130% | Exceptional — expansion far outpaces churn; world-class |
| 110–130% | Strong — healthy expansion engine |
| 100–110% | Adequate — modest expansion, low churn |
| 90–100% | Concerning — churn is eating into base |
| < 90% | Crisis — losing the base faster than expansion covers it |

PMs can move NRR through:
- **Expansion features:** Tier upgrades, seat additions, usage growth
- **Churn reduction:** Better activation, stickier core workflows, proactive health monitoring
- **Contraction prevention:** Better tier design so downgrades are less common

## Next steps

- [Finance & P&L](finance-and-pl.md) — the income statement context
- [Business Models](business-models.md) — how the model determines which unit economics levers you have
- [Pricing & Packaging](../05-go-to-market/pricing-and-packaging.md) — the direct ARPA lever
