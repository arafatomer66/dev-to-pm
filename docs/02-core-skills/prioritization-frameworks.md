# Prioritization Frameworks

Every PM faces the same fundamental problem: more good ideas than capacity to build them. Prioritization frameworks are tools for making that decision systematically and defensibly.

This page covers the most widely used frameworks, when each applies, and — critically — what no framework can do for you.

## Why frameworks exist

Without a framework, prioritization becomes:
- **HiPPO-driven** (Highest Paid Person's Opinion) — whoever shouts loudest wins
- **Recency-biased** — the last customer complaint sets the sprint priority
- **Feature-factory thinking** — we ship whatever's easiest to ship

Frameworks force you to make your assumptions explicit. They don't replace judgment — they structure it.

## RICE

**Best for:** Feature-level prioritization across a backlog

RICE scores each item on four dimensions:

```
Score = (Reach × Impact × Confidence) / Effort
```

| Dimension | Definition | Scale |
|-----------|------------|-------|
| **Reach** | How many users affected per quarter? | Absolute number |
| **Impact** | How much does it move your key metric? | 0.25 / 0.5 / 1 / 2 / 3 |
| **Confidence** | How certain are you of the above? | 100% / 80% / 50% |
| **Effort** | Person-months of work | Absolute number |

**Example:**
- Feature A: 1,000 users × 2 impact × 80% confidence / 2 months = **800**
- Feature B: 5,000 users × 0.5 impact × 50% confidence / 1 month = **1,250**

Feature B wins — even though its per-user impact is lower, the breadth and effort efficiency make it higher ROI.

**Pitfall:** People game RICE by inflating Reach and Impact. Require evidence for any score above baseline. "5,000 users — how do you know?" is always a fair question.

## WSJF (Weighted Shortest Job First)

**Best for:** SAFe environments; when you need to account for time-sensitivity and cost of delay

```
WSJF = Cost of Delay / Job Duration
```

Cost of Delay includes:
- **User/business value** — revenue impact, customer satisfaction
- **Time criticality** — does this get less valuable if delayed?
- **Risk reduction / opportunity enablement** — does this unlock future work or reduce risk?

WSJF explicitly rewards shorter work with high time-sensitivity over large projects with stable value. It's particularly useful for compliance items, integrations tied to customer contracts, and platform work that unblocks future features.

**Best used when:** You're in a scaled agile environment or you frequently have items with hard external deadlines competing with open-ended improvements.

## ICE

**Best for:** Fast, informal scoring; growth teams; early-stage

```
Score = Impact × Confidence × Ease
```

Each on a 1–10 scale. Quick to calculate, easy to explain.

ICE is deliberately lightweight. It's great for a growth team running 10 experiments per month and needing a fast way to rank them. It's less suitable for strategic portfolio decisions where rigor matters more than speed.

## MoSCoW

**Best for:** Stakeholder alignment on scope; pre-sprint planning; contract/statement-of-work contexts

| Category | Meaning |
|----------|---------|
| **Must have** | Non-negotiable — launch is blocked without this |
| **Should have** | High value, not critical to launch |
| **Could have** | Nice-to-have, include if capacity allows |
| **Won't have** | Explicitly out of scope for this release |

MoSCoW is less a scoring system and more a communication tool. It's useful for forcing explicit scope conversations with stakeholders, particularly when "everything is a priority" is the default answer.

**Pitfall:** Everything ends up as "Must have." If more than 40% of your backlog is "Must," you're not actually prioritizing — you're documenting wishes.

## Kano Model

**Best for:** Feature classification before prioritization; customer satisfaction research

The Kano model categorizes features by how they affect customer satisfaction:

| Category | Description | Example |
|----------|-------------|---------|
| **Basic** | Expected; absence causes dissatisfaction | Data exports |
| **Performance** | More is better; directly correlates to satisfaction | Search speed |
| **Excitement (Delighters)** | Unexpected; creates delight when present | Smart suggestions |
| **Indifferent** | Presence or absence has little effect | — |
| **Reverse** | Some users dislike when present | Aggressive upsells |

Kano is most useful in discovery — to understand what features are "table stakes" vs. opportunities for differentiation. You can't prioritize without knowing which category a feature belongs to.

**How to use it:** Run a Kano survey asking customers two questions per feature: "How do you feel if this feature IS present?" and "How do you feel if this feature IS NOT present?" The combination of answers reveals the category.

## Opportunity Scoring (Opportunity Solution Tree)

**Best for:** Discovery prioritization; identifying underserved needs

Ask customers to rate each potential feature on:
1. **Importance:** How important is this to you? (1–10)
2. **Satisfaction:** How satisfied are you with current solutions? (1–10)

Opportunity score = Importance + max(Importance − Satisfaction, 0)

High importance + low satisfaction = underserved opportunity. High importance + high satisfaction = already solved, don't waste time.

## What no framework can do

Here's the uncomfortable truth: **prioritization frameworks are decision aids, not decision makers.** They can't:

- Tell you if your impact estimates are real
- Account for strategic bets that look bad in a spreadsheet but are the right long-term moves
- Replace customer conversations
- Resolve genuine disagreement between stakeholders about what matters
- Factor in organizational politics (which are real and not going away)

A RICE score only as good as its inputs. A team that inflates "Reach" estimates will produce a perfectly formatted spreadsheet that leads them toward the wrong decision.

The frameworks are most valuable for:
1. Making your assumptions legible to others
2. Forcing a conversation about inputs, not outputs
3. Documenting why you made the decision you made

## How to actually run prioritization

**Step 1: Agree on the objective first.** What is the primary metric this prioritization cycle is trying to move? Prioritization without an objective produces a local optimum — the highest-scored item across all possible goals, which is usually the wrong answer for any specific goal.

**Step 2: Score collaboratively, not solo.** Involve engineering leads (for effort) and design (for complexity). Solo PM prioritization creates resentment and misses information.

**Step 3: Use the framework to start the conversation, not end it.** The score is a starting point. Discuss the items where scores feel wrong. Often the disagreement surfaces important information.

**Step 4: Make the non-items explicit.** "We are not doing X this quarter, even though it scored well, because it doesn't align with our Q3 objective of reducing churn." That sentence, written down, is worth more than the spreadsheet.

**Step 5: Revisit when inputs change.** A prioritization from three months ago may be wrong now. A customer conversation, a competitor move, or a missed metric can all change the calculus.

## A note on stakeholder-driven prioritization

You will face pressure to reprioritize based on sales deals, executive opinions, and loud customer requests. This is normal and not always wrong — sometimes a large deal really does justify a specific feature.

What you're protecting against is *systematic* stakeholder-driven prioritization, where the PM's job becomes negotiating between stakeholder demands rather than making product decisions.

Your defense: a transparent, documented prioritization process. When you can show stakeholders the tradeoff — "we can build the sales feature, and here's what we're not building as a result" — you convert a power struggle into a business conversation.

## Next steps

- [Roadmapping](roadmapping.md) — where prioritization decisions become a timeline
- [Stakeholder Management](stakeholder-management.md) — handling the political side of prioritization
- [OKRs & Metrics](../03-product-strategy/okrs-and-metrics.md) — setting the objective that prioritization serves
