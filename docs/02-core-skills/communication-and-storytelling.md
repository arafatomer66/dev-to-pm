# Communication & Storytelling

A PM's work is almost entirely communication. PRDs, roadmap presentations, stakeholder updates, customer interviews, engineering syncs, executive briefings — all of it depends on your ability to be clear, concise, and credible.

This page covers the communication patterns that matter most in the PM role, including BLUF writing, narrative structure for roadmap and strategy conversations, and how to communicate bad news.

## BLUF writing

BLUF — Bottom Line Up Front — is the most important writing discipline for PMs.

Most developers write in problem-first order: set up context, describe the situation, explain the analysis, then reach the conclusion. This is how you'd structure a bug report or a technical design doc.

Executives and stakeholders read in conclusion-first order. They want to know what you're asking or what you've decided, then they'll read the supporting detail if they care.

**BLUF format:**
```
[The conclusion / ask / decision]

[Supporting context — why this decision, what you considered]

[Details / appendix for those who want to go deeper]
```

**Example — before BLUF:**
> "We've been looking at the onboarding flow metrics for the past month. Activation rate has dropped 12% since the July release. We looked at a few possible causes including the new signup form length, the email verification step, and the welcome tour changes. After analyzing drop-off by step, we found that 68% of users who don't activate abandon during email verification. We think we should remove mandatory email verification for trial users."

**Example — with BLUF:**
> "Recommendation: Remove mandatory email verification for trial users. It's causing 68% of activation failures. Details below."

The second version communicates the same information. The reader can stop after the first line if they trust the recommendation, or read on if they want to understand it.

## Narrative structure for roadmap presentations

When presenting a roadmap to leadership or stakeholders, structure matters more than slide count.

A roadmap narrative that works:

1. **Where we've been** — What did we commit to last quarter? What actually happened? (Builds credibility; shows you can be honest about misses)
2. **Where we are** — Current product state; key metrics; what's working and what isn't
3. **The opportunity** — What we've learned from customers, data, and the market; what problem we're uniquely positioned to solve
4. **The strategy** — How we're thinking about the next 6–12 months; what bets we're making and why
5. **The roadmap** — What specifically we're building, in what order
6. **What we need** — Any decisions, resources, or alignment required from this group

This structure works because it earns the right to show the roadmap by building the case first. If you show the roadmap on slide 2, stakeholders will immediately start asking "why not X instead?" — before you've established the reasoning.

## Writing for engineers vs. writing for executives

You will write for both audiences and they need fundamentally different things.

### Writing for engineers

Engineers want:
- Precision — vague requirements create work for them
- Complete context — why are we building this?
- Open questions surfaced — don't pretend you have all the answers
- Explicit scope boundaries — what's out of scope is as important as what's in scope
- Respect for their judgment — requirements describe outcomes, not implementations

### Writing for executives

Executives want:
- The conclusion first
- Business framing — revenue, users, risk, cost
- Confidence calibration — are you sure, or is this a bet?
- What you need from them — is this informational or is there an ask?
- Short — if it takes more than 90 seconds to read, most executives won't

**Translating between the two:** The same PRD should not be sent to both audiences. Write the full PRD for the team. Write a one-paragraph summary + key metrics + key risks for the exec.

## The bad-news protocol

Bad news delivered late is always worse than bad news delivered early. But most PMs learn this the hard way.

**When to escalate bad news:** As soon as you know there's a problem — not after you've figured out the solution.

This runs counter to engineering instinct, which is "I'll fix it before I tell anyone." In a PM role, your stakeholders need to know about risks so they can make decisions too. A deadline slip that affects a customer commitment needs to be known by Sales immediately, not on the day the deadline is missed.

**How to communicate bad news:**

1. **State it clearly** — don't bury the lede or soften it into meaninglessness
2. **Own your contribution** — if PM decisions contributed to the problem, say so
3. **Context, not excuses** — explain what happened; don't over-explain in a defensive way
4. **What you're doing about it** — always have a plan, even if it's "here are three options"
5. **What you need** — if you need a decision from the reader, say so explicitly

**Example:**
> "We're going to miss the Q3 payments launch by approximately three weeks. The integration with Stripe's new API is taking longer than estimated — we underestimated the edge cases in our current payment model. We've scoped two options: (1) launch without the new recurring billing feature and add it in Q4, or (2) delay the full launch to October 15. I recommend option 1 — the core upgrade is still valuable and we don't want to slip the customer communication timeline. I need your input by Friday."

## Making the case for your roadmap

When you present work to leadership or a board, you're making an argument: here's why this bet is worth the engineering time and opportunity cost.

The structure of a credible argument:

**Evidence:** What data, customer quotes, or market observations support the problem?
**Insight:** What's your interpretation of that evidence? What's the non-obvious thing you understand?
**Hypothesis:** If we build X, then Y will happen. Make it falsifiable.
**Investment:** What does this cost in time and people?
**Return:** What's the expected upside? In what timeframe?
**Risk:** What could go wrong? How would you know?

A weak product case: "Customers have been asking for this for a while and I think it would improve retention."

A strong product case: "We've had 43 support tickets and 6 enterprise renewal conversations cite the lack of bulk export as a friction point. Our churn survey shows 18% of churned accounts listed data portability as a top-3 exit reason. We estimate this takes one engineer six weeks and would reduce churn-related export requests by 60%. If that holds, it's worth $X in retained revenue annually."

Not every decision needs this level of rigor. Small decisions need small cases. Big bets need big evidence.

## Communicating product direction to the team

The team should always know:
- What we're building this quarter and why
- What we're NOT building and why
- How success is defined
- What we've learned recently that might change our direction

Run a monthly or quarterly product review with the full cross-functional team. Cover: what we shipped, what we learned, what changed about our understanding of the problem.

This isn't overhead — it's the mechanism that keeps the team aligned and motivated. Engineers who understand why they're building something make better micro-decisions than engineers who are just executing tickets.

## Next steps

- [Stakeholder Management](stakeholder-management.md) — managing the audience for your communication
- [Roadmapping](roadmapping.md) — creating the artifact you'll be communicating
- [Status Update template](../10-templates/status-update.md)
