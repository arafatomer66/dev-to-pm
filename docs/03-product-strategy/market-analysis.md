# Market Analysis

Market analysis is how you build the external view that strategy depends on. As a developer, your view of the world was shaped by the codebase and the team. As a PM, you need to add the market: who buys, why, what alternatives exist, where the trends are going.

## Why developers underinvest in market analysis

Engineers are trained to work with clear inputs and defined systems. Market analysis involves incomplete data, conflicting signals, and judgment calls under uncertainty. This is uncomfortable and often deprioritized in favor of the cleaner, more tractable problems of feature development.

The consequence: PMs who build excellent products for markets that don't exist or in directions the market isn't going. The build was technically impressive; the product strategy was blind.

## TAM, SAM, SOM

These three terms get misused constantly. Here's what they actually mean:

| Term | Stands for | Means |
|------|-----------|-------|
| **TAM** | Total Addressable Market | The entire market opportunity if you had 100% share |
| **SAM** | Serviceable Addressable Market | The portion you could realistically serve with your current model |
| **SOM** | Serviceable Obtainable Market | The portion you can realistically capture in the near term |

**Example:** You're building a B2B HR software product.
- TAM: All spending on HR software globally (~$20B)
- SAM: Mid-market companies (100–1000 employees) in English-speaking markets with budget for HR tech (~$3B)
- SOM: Companies that match your ICP, considering your current sales capacity and go-to-market (~$50M)

**The honest use of TAM:** TAM is useful for investor conversations and go/no-go decisions on entering a market. It's frequently inflated in pitch decks. For day-to-day PM decisions, SOM is more relevant — it's the market you're actually competing in.

## Market sizing approaches

**Top-down:** Start with industry research data, narrow down by segment and geography.
> "The HR software market is $20B globally. Mid-market is approximately 20% of that ($4B). We estimate English-speaking markets are 60% of mid-market ($2.4B)."

**Bottom-up:** Build up from the unit economics.
> "There are approximately 50,000 companies in our ICP in the US. Average deal size is $20K/year. That's a $1B SAM."

Bottom-up is usually more credible and forces you to validate your ICP assumptions. Top-down is faster and works when bottom-up data is hard to get.

## Customer segmentation

A "market" is not a monolithic thing. It's made up of customer segments with different needs, buying behaviors, and willingness to pay.

**How to segment:**

- **By company size:** SMB, mid-market, enterprise — these segments have fundamentally different buying processes and product requirements
- **By industry:** Healthcare software requirements look nothing like retail. Segment if industry creates distinct needs.
- **By user role:** The person who uses the product and the person who buys it may be completely different (especially in B2B). Both need to be understood.
- **By job to be done:** What outcome is the customer trying to achieve? Customers with the same demographic profile may buy for entirely different reasons.

**The underserved segment:** The most strategically valuable analysis is identifying a segment that is large enough to matter, has a real unsatisfied need, and is poorly served by current alternatives. This is your beach head.

## Trend analysis

Markets don't stand still. Understanding where a market is going is as important as understanding where it is.

**Signals to track:**
- **Regulatory changes:** GDPR, SOC2, HIPAA, AI regulation — compliance requirements can create new markets overnight
- **Technology shifts:** A new platform (mobile, cloud, AI) usually opens an opportunity to rebuild incumbents on a better foundation
- **Workforce and demographic changes:** Remote work, generational shifts, urbanization — these change who uses products and how
- **Macroeconomic context:** Expansion and contraction cycles change buyer behavior (risk tolerance, budget availability)
- **Adjacent market behavior:** Watch what's happening in adjacent markets; often a model proven there will arrive in yours

**How to track trends:**
- Read industry analyst reports (Gartner, Forrester, IDC — usually behind paywalls but often cited publicly)
- Follow key journalists and newsletters in your market
- Talk to customers frequently — they see their industry from the inside
- Watch what competitors are investing in
- Monitor funding rounds in your space (a wave of investment signals a market heating up)

## The market map

A market map visualizes the competitive landscape. Simple format:

Choose two axes that matter in your market (e.g., price vs. features; enterprise vs. SMB; breadth vs. depth). Plot yourself and competitors. Look for:
- **Clusters** where lots of competitors are fighting for the same space
- **White spaces** where few competitors operate but customer needs exist
- **Your position** — are you differentiated, or are you one of six similar players?

The market map is most useful for finding a position that isn't already occupied by well-resourced competitors. "We'll build a better version of Salesforce" is a position that ignores the market map.

## Voice of market

Market analysis isn't just quantitative. The "voice of market" — what customers and prospects actually say about their needs, frustrations, and alternatives — is often more actionable than analyst reports.

**Primary research:**
- Customer interviews (see [User Research](../04-product-discovery/user-research.md))
- Win/loss interviews with sales (why did we win? why did we lose?)
- Churn interviews (why did you leave?)
- Prospect interviews (what's your current solution? what would make you switch?)

**Secondary research:**
- Review sites (G2, Capterra, Trustpilot) — read the negative reviews of competitors
- Job postings from competitors (engineering roles signal product direction)
- Public earnings calls (public companies reveal a lot about their market view)
- Community forums and Slack groups where your target users hang out

## Market sizing for internal decisions

You don't need to size the market for every feature decision. But for major strategic bets — entering a new segment, building a new product line, investing in a platform capability — you should be able to answer:

1. How many potential customers would benefit from this?
2. What is the incremental revenue opportunity?
3. What would it take to capture that opportunity?
4. What's the competitive intensity in this space?

If you can't answer these, you're making a strategic bet without knowing the size of the bet.

## Next steps

- [Competitive Intelligence](competitive-intelligence.md) — analyzing specific competitors
- [Positioning & Differentiation](positioning-and-differentiation.md) — using market analysis to define your position
- [Vision & Strategy](vision-and-strategy.md) — turning market insight into strategy
