# Working with Sales

Sales and product have a naturally tense relationship. Sales needs a product that closes deals today. Product needs to build for a market that exists tomorrow. Neither perspective is wrong — they're different time horizons. Managing this tension productively is a core PM skill in B2B companies.

## Understanding the sales motion

Before you can work well with sales, you need to understand how your company sells.

**Sales-led (SLG):** Human-driven deals; AEs, SDRs, and solutions engineers are primary acquisition channel. Long sales cycles, high ACVs. Product plays a supporting role in the sales process.

**Product-led (PLG):** Users try the product and upgrade without (or with minimal) human involvement. Short cycles, lower ACVs, high volume. Product IS the sales channel.

**Hybrid:** Enterprise motion (SLG) plus self-serve or SMB PLG. Complex but increasingly common.

Your relationship with sales looks very different depending on which motion you're in. In SLG, sales has disproportionate product influence because they're in deals daily and can see competitive pressure in real time. In PLG, sales has less influence because product metrics tell most of the story.

## What sales needs from product

**Competitive battlecards:** One-pagers explaining how to position against each major competitor. What do you do better? What do they do better? What objections come up and how do you answer them?

**Demo environments:** Reliable, realistic demo data. A broken demo at a critical deal is a product problem, not a sales problem.

**Honest roadmap communication:** Sales will make commitments to prospects. They need to know what's coming so they don't commit to something that isn't actually coming.

**Feature clarification:** "Can the product do X?" questions before and during deals. PMs who respond quickly build credibility with sales; PMs who are unresponsive create a trust deficit.

## What product needs from sales

**Win/loss data:** Why deals are won and lost is the most valuable market signal a PM can get. Build a system to capture it.

**Deal-specific feedback patterns:** One customer asking for a feature is noise. Ten deals lost to competitors for the same reason is signal.

**Prospect discovery context:** What problems are prospects describing before they've seen the product? What language do they use? This is raw, uninfluenced market signal.

**Customer relationships:** Sales AEs often have deep customer relationships. For customer advisory boards, discovery calls, and design partnerships, a warm intro from an AE is worth more than a cold email.

## The feature request problem

Sales will bring feature requests. Many will be legitimate market signals. Some will be one-off requests from a single deal that don't represent broader demand.

**How to evaluate sales feature requests:**

1. **How many deals have requested this?** One deal is noise. Five or more deals is signal.
2. **What's the underlying problem?** Translate the feature request into a JTBD.
3. **What segment does this serve?** Is this our ICP, or is this a segment we've decided not to serve?
4. **What would we trade to build this?** Always frame additions as tradeoffs.
5. **Is there a lighter version?** Can we solve 80% of the value with 20% of the effort?

Create a lightweight intake process: a Slack channel or form where sales can submit requests, with fields for "how many deals/accounts is this blocking?" This transforms anecdotal requests into structured data you can analyze over time.

## Roadmap communication with sales

Sales needs to know what's coming. But committing to specific features and dates is a trap — engineering doesn't always deliver on time, and market conditions change.

**A sustainable approach:**

- Share quarterly themes, not specific feature dates: "We're focused on enterprise security and SSO this quarter"
- Give a clear "no" on items that aren't on the roadmap, with a reason
- For items that are coming, give a range, not a date: "We're targeting H2 for this"
- Build a deal review process: when a deal is at risk over a roadmap item, involve the PM to make a prioritization decision explicitly — not leave sales to make roadmap commitments unilaterally

## Saying no to a deal feature request

This is uncomfortable but necessary. When you can't build what sales needs for a specific deal:

1. Acknowledge the business value of the deal
2. Explain the opportunity cost ("to build this by your timeline, we'd need to delay X")
3. Offer alternatives: "What if we could give them read-only access to X as a workaround for now?"
4. Involve your VP or CPO if the deal size warrants escalation

"No" is sometimes the right answer even when it costs a deal. A roadmap driven entirely by individual deal requests produces a product with no coherent strategy.

## Sales enablement

Sales enablement is the material and training that helps sales understand and demo your product effectively.

Your contribution as PM:
- **Feature release notes** written for a sales audience: what it does, who it helps, what to say about it
- **Competitive positioning** updates when a competitor launches something relevant
- **Demo script assistance** for major new features
- **Monthly product update** brief to sales: what shipped, what's coming, what changed

PMs who invest 2 hours per month in sales enablement get significantly better market intelligence in return. It's a very high-ROI activity.

## Next steps

- [Pricing & Packaging](pricing-and-packaging.md) — where pricing decisions interact with deal structure
- [Competitive Intelligence](../03-product-strategy/competitive-intelligence.md) — building the competitive knowledge that feeds battlecards
- [Working with Marketing](working-with-marketing.md) — the GTM team that works alongside sales
