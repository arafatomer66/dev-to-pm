# Data-Driven Decisions

"Data-driven" is one of the most overused phrases in product management. This page is about what it actually means in practice — and, just as importantly, when data isn't enough.

## Define metrics before you build

The single most important data discipline in PM is defining your success metric *before* you start building. Not after launch. Not during development. Before.

Why: If you define metrics after launch, you'll unconsciously choose metrics that show your feature in the best light. You'll "discover" that the feature increased something — page views, clicks, time on page — and declare success. This is how feature factories survive: they ship features, report positive vanity metrics, and never ask whether the underlying problem got solved.

**The pre-mortem metric question:** Before writing the PRD, ask: "One month after launch, what number would convince me this feature was a success? What number would convince me it was a failure?"

Write both numbers down. Commit to them. Then measure.

## Types of metrics

### Outcome metrics vs. output metrics

| Output metric | Outcome metric |
|---|---|
| Features shipped | User retention |
| Story points completed | Revenue from new cohorts |
| Experiments run | Customer satisfaction score |
| Page views | Time to value for new users |

Output metrics measure activity. Outcome metrics measure impact. PMs should be held accountable for outcome metrics. Output metrics are for the engineering team to track execution health.

The most common failure mode: reporting to leadership on output metrics while framing it as product success.

### Leading vs. lagging indicators

**Lagging indicators** tell you what happened: churn rate, revenue, NPS. They're accurate but slow — by the time they move, you're already past the decision window.

**Leading indicators** predict what will happen: activation rate, feature adoption in the first week, support ticket volume. They're noisier but faster.

Good metric frameworks pair both. Example: Retention (lagging) + Day-7 engagement rate (leading). If Day-7 engagement drops, you can act before it shows up in monthly retention.

### The North Star metric

The North Star is the single metric that best captures whether your product is delivering value to users. It should:
- Reflect actual value created (not just engagement or revenue)
- Be something the team can influence
- Have a clear relationship to business outcomes

Examples:
| Product | North Star |
|---------|-----------|
| Slack | Messages sent per active user |
| Airbnb | Nights booked |
| Spotify | Time spent listening |
| B2B SaaS analytics tool | Weekly active reports created |

The North Star is not your only metric — it's the one you optimize for when metrics conflict.

## AARRR (Pirate Metrics)

Dave McClure's AARRR framework maps metrics to funnel stages:

| Stage | Question | Example metrics |
|-------|----------|-----------------|
| **Acquisition** | How are users finding us? | Traffic, CAC, trial sign-ups |
| **Activation** | Do users have a great first experience? | Activation rate, time to first value |
| **Retention** | Do users come back? | D7/D30 retention, churn rate |
| **Revenue** | Do users pay? | MRR, ARPU, conversion rate |
| **Referral** | Do users tell others? | NPS, referral rate, virality coefficient |

For most B2B SaaS products, the highest-leverage stages are Activation and Retention. Most teams over-invest in Acquisition and underinvest in the rest.

## Avoiding vanity metrics

Vanity metrics look good but don't predict business outcomes:

| Vanity metric | Why it's misleading | Better metric |
|---|---|---|
| Total registered users | Includes inactive accounts | Monthly active users |
| Page views | Users may be lost | Task completion rate |
| App downloads | Doesn't mean used | 7-day active users |
| Emails sent | Doesn't mean read | Reply rate / conversion |
| Features shipped | Doesn't mean valuable | Feature adoption rate |

The test for a vanity metric: "Would this number go up even if the product got worse?" If yes, it's a vanity metric.

## Statistical validity (the basics you need)

You don't need to be a data scientist. But you need to know enough to not fool yourself.

### Sample size matters

An experiment with 50 users in each variant cannot tell you anything reliable. Before running an experiment, calculate whether you have enough traffic to reach statistical significance in a reasonable time.

Rule of thumb: if you're trying to detect a 5% change in a metric with 80% power and 95% confidence, you need roughly 600 users per variant. Tools like Evan Miller's sample size calculator do this automatically.

### Correlation vs. causation

"Users who use Feature X have 2x the retention" does not mean Feature X causes higher retention. It may mean that users who are already highly engaged use Feature X. This is survivorship bias.

To establish causation: run a controlled experiment where users are randomly assigned to have Feature X available or not.

### P-values and significance

A p-value of 0.05 means "if there were no real effect, we'd see results this extreme 5% of the time." It does not mean "there's a 95% chance the effect is real." The distinction matters when you're deciding whether to ship.

Statistical significance is not business significance. A 0.1% improvement in click-through that is statistically significant may not be worth the engineering cost.

## Qualitative data

Quantitative data tells you *what* is happening. Qualitative data tells you *why*.

A drop in activation rate is a what. Customer interviews that reveal users are confused by the onboarding email sequence is a why.

PMs who rely exclusively on dashboards miss the "why" layer. PMs who rely exclusively on qualitative research miss the "how big" layer. The best product decisions combine both: quantitative to identify where problems exist, qualitative to understand them deeply enough to solve them.

## When data isn't enough

Three situations where data should not be the final word:

**1. When you're making a bet on a future that doesn't exist yet.** If you're building a genuinely new product or market, there's no historical data to analyze. Vision and judgment must carry more weight than analytics.

**2. When the sample size is too small.** Early-stage products often have user bases too small for statistical significance. Qualitative insight is more reliable than noisy quantitative signals in this phase.

**3. When the metric you can measure isn't the metric you care about.** Sometimes the outcomes that matter most — trust, brand perception, long-term retention — are hard to measure with the data infrastructure you have. Don't substitute a measurable but irrelevant metric for the one you actually care about.

## Building a data practice

For a PM transitioning from engineering, building data habits is often easier than it sounds — you likely already know SQL or can learn it quickly.

**Basic skills to develop:**
- Writing queries to pull your own usage data (don't always depend on a data analyst)
- Reading a funnel analysis and identifying the highest-leverage drop-off point
- Understanding an A/B test result at basic confidence interval level
- Building a dashboard that tracks your feature's metrics post-launch

**Tools you'll encounter:** Mixpanel, Amplitude, Heap (event analytics), Looker/Mode/Metabase (SQL-based BI), Segment (data pipeline), Google Analytics (web), Braze/Iterable (messaging analytics).

You don't need to master all of them. Know enough to pull your own data, read a report, and ask intelligent questions of your data team.

## Next steps

- [OKRs & Metrics](../03-product-strategy/okrs-and-metrics.md) — building a metric framework for your product
- [MVPs & Experiments](../04-product-discovery/mvp-and-experiments.md) — running experiments that produce valid learning
- [Metrics Framework template](../10-templates/metrics-framework.md)
