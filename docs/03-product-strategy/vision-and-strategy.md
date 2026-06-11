# Vision & Strategy

Strategy is the most important and least practiced PM skill. Most PMs can run a sprint, write a PRD, and facilitate a backlog review. Far fewer can articulate a clear product strategy — a reasoned argument for why specific bets will produce specific outcomes in a specific market.

This page covers how to think about product vision and strategy and how to communicate them in a way that drives decisions.

## Vision vs. Strategy

These are distinct and both necessary.

**Vision** is aspirational and durable. It describes what the world looks like when your product succeeds — typically 3–5 years out. It doesn't change every quarter. Good vision is:
- Inspiring enough to motivate a team through hard times
- Specific enough to exclude alternatives
- Simple enough to repeat in one sentence

Examples:
- "A world where every small business has access to the same financial tools as a Fortune 500 company."
- "The operating system for healthcare delivery, connecting every part of the care journey."

Bad vision examples: "Be the best platform for X" (too generic), "Grow to $100M ARR" (that's a goal, not a vision).

**Strategy** is concrete and time-bound. It's the plan for making progress toward the vision given current constraints, capabilities, and market conditions. Strategy changes as you learn. It should describe:
- What specific problem you're solving, for whom
- What makes your approach distinctive
- What you're prioritizing and what you're not
- What assumptions you're making and how you'd know if you're wrong

## The strategy stack

Good product strategy exists at multiple levels and each level should be coherent with the others:

```
Company Strategy
    └── Product Strategy
            └── Product Area Strategy
                    └── Quarterly OKRs
                            └── Sprint Goals
```

When these levels are disconnected, you get "strategy theater" — nice presentations that don't actually guide what the team builds day-to-day.

**The PM's job:** Own the product strategy level. Understand the company strategy well enough to derive from it. Set the product area strategies clearly enough that quarterly OKRs are obvious.

## Diagnosis → Guiding Policy → Coherent Actions

This is Richard Rumelt's strategy kernel from *Good Strategy / Bad Strategy* — the most useful framework for actually writing a product strategy.

**Diagnosis:** What is the challenge? What makes the current situation difficult?

The diagnosis names the specific obstacle or opportunity. "The market is competitive" is not a diagnosis. "SMBs in our target market have switched to self-serve tools at 3x the rate we expected, and our enterprise-focused UX is creating activation friction that prevents us from competing" is a diagnosis.

**Guiding Policy:** How are we going to address the diagnosed challenge?

The guiding policy is not a goal ("grow revenue") or a list of features. It's the approach — the constraint on how you'll solve the problem. "We will double down on the enterprise segment where we win, and build the self-serve motion as a separate GTM track" is a guiding policy.

**Coherent Actions:** What specifically are we doing?

Actions are what actually shows up in the roadmap. Each action should connect to the guiding policy. If you're taking an action that doesn't connect, either the action is wrong or the strategy is incomplete.

## Writing a product strategy on one page

A one-page product strategy template:

```
PRODUCT STRATEGY — [Product Name] — [Year/Half]

Diagnosis
---------
[The specific challenge or opportunity we're addressing. 
What makes this moment different? What's working against us or for us?]

Our Bet
-------
[What we believe will happen if we execute this strategy. 
Make it falsifiable: "We believe that [action] will lead to [outcome]
because [reason]. We'll know we're wrong if [signal]."

Guiding Policy
--------------
[How we will and won't compete. What we're prioritizing over other options.
What we're giving up to stay focused.]

This Quarter's Priorities
-------------------------
[3–5 specific initiatives that reflect the strategy. 
Each should connect visibly to the Guiding Policy.]

What We're Not Doing
--------------------
[Explicit out-of-scope areas — and why.]

Key Assumptions
---------------
[What has to be true for this strategy to work?
Which assumptions are most fragile?]
```

## Common strategy failure modes

**Goals masquerading as strategy:** "Grow MAU by 30%" is a goal. It doesn't tell you what to do or what tradeoffs to make.

**Everything is a priority:** A strategy that prioritizes everything prioritizes nothing. If you can't name three things you're explicitly NOT doing, you don't have a strategy.

**Strategy lives in a deck, not in decisions:** The real test of a strategy is whether it guides daily decisions. Can your engineers, when evaluating two approaches, use the product strategy to choose? If not, the strategy is decorative.

**Strategy ignores competitive reality:** "We'll build the best product" is not differentiation. What specifically will you do better, for whom, and why will customers choose you over alternatives?

**Strategy is set and never revisited:** A strategy written in January and not revisited in September is probably wrong — the market doesn't hold still. Set a cadence for strategy review (quarterly is usually right).

## How vision and strategy connect to the team

The vision and strategy should be visible and real to the entire team — not just leadership.

**In practice, this means:**
- Introduce new engineers and designers to the product vision in their first week
- Start roadmap reviews with a one-paragraph strategy reminder
- When you say no to a feature request, connect it to the strategy: "This doesn't fit our current focus on [guiding policy]"
- When you make a hard scope call, reference the strategy: "We're prioritizing the enterprise segment this half, so we're deferring this consumer-facing improvement"

A team that understands the strategy makes better micro-decisions without needing PM input on everything. That's the ROI on the time you spend communicating strategy.

## Next steps

- [Market Analysis](market-analysis.md) — building the external view that informs strategy
- [OKRs & Metrics](okrs-and-metrics.md) — translating strategy into measurable bets
- [Competitive Intelligence](competitive-intelligence.md) — understanding what you're up against
