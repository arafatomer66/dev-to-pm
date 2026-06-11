# Negotiation

PMs negotiate constantly: with engineering over scope and timelines, with design over polish vs. speed, with sales over feature commitments, with leadership over resources. Most of this doesn't look like formal negotiation — it looks like ordinary conversation. But the principles are the same.

## Interests vs. positions

The most important concept in negotiation, from the Harvard Negotiation Project:

**Position:** What someone says they want.
**Interest:** Why they want it.

Positions conflict. Interests often don't.

**Example:**
- Sales position: "We need the bulk export feature by next month to close this deal."
- PM position: "We can't do that — the team is committed to the authentication overhaul."

These positions are incompatible. But look at the interests:
- Sales interest: Close a deal; hit their quarterly number; not lose to a competitor.
- PM interest: Ship the auth overhaul that unblocks three other customers; avoid scope churn.

Once you surface interests, you can find solutions positions can't: Can we provide a manual CSV export as a stopgap? Can we commit the feature to Q4 with a signed deal? Can we get a 60-day extension on the deal close?

**The practice:** When you hit a wall in a negotiation, ask "why" until you hit bedrock. "Why do you need it by next month?" → "Because the prospect wants to see it before signing." → "What specifically do they want to see?" → "That their team can get their data out." Now you have an interest, and interests have solutions.

## BATNA

BATNA — Best Alternative to a Negotiated Agreement — is your walkaway point. It's what you'll do if this negotiation fails.

Knowing your BATNA gives you leverage. Going into a negotiation without knowing it leaves you in a weak position — you'll concede more than you should because you're afraid of the alternative.

**PM application:**
Before a negotiation, ask: "If we can't reach agreement, what do I do?" 

- If Sales won't accept a Q4 delivery: your BATNA might be escalating to the VP of Sales to make the tradeoff decision.
- If Engineering says a feature will take 3 months: your BATNA might be scoping it down to 4 weeks of work.
- If a stakeholder keeps blocking your roadmap: your BATNA might be a structured escalation to leadership.

Knowing your BATNA lets you negotiate confidently. If your BATNA is good, you don't need to accept a bad deal.

## Anchoring

The first number offered in a negotiation has outsized influence on the final outcome. This is anchoring.

**In timeline negotiations:** If engineering says "this will take 3 months" and you don't anchor, you'll negotiate down from 3 months. If you anchor at 4 weeks, the negotiation is about whether it's closer to 4 weeks or 8 weeks — not 3 months.

This isn't about being unreasonable. It's about framing. "What would a 4-week version of this feature look like?" is an anchor. It forces the conversation to start from a smaller frame.

**Counter-anchoring:** When someone opens with an extreme anchor, don't immediately respond with a counter-offer. First, question the anchor: "Help me understand how you got to 3 months — what's the most complex piece?" This breaks the anchor's psychological hold and gives you information.

## Trades, not concessions

Concessions (giving something for nothing) erode your position. Trades (giving something in exchange for something) protect it.

**Concession:** "OK, we'll build the feature by next month." (you gave up timeline for nothing)

**Trade:** "We can pull that feature forward if we can drop the reporting dashboard from this sprint. Does that work for the deal?" (you traded scope for timeline)

Every time you give something, get something. Even if it's small — a commitment, a process change, a piece of information. This isn't about being difficult; it's about making sure both sides are moving together.

## Scope negotiation with engineering

This is the negotiation you'll do most often.

**The common scenario:** You've written a spec. Engineering has estimated it at 8 weeks. Your roadmap has 4 weeks. Now what?

Start with curiosity, not pressure. "Help me understand what makes this 8 weeks." Often this reveals:
- A technical constraint you didn't know about (adapt your spec)
- An assumption about feature completeness that's negotiable (scope the MVP)
- Legitimate complexity you need to respect and defend to stakeholders

**Scope-splitting tactics:**
- **Thin slicing:** What's the smallest version that gives users real value?
- **Phasing:** Can we ship 60% of the feature now and the rest in the next cycle?
- **Constraint relaxation:** "What if we dropped [specific requirement] — how much does that change the estimate?"

Never demand a faster estimate. "Can you do it in 4 weeks?" is not a negotiation; it's pressure. Pressure produces false commitments that blow up later. Work with the constraints that are real.

## Saying no while keeping the relationship

Being the person who says no is uncomfortable for developers-turned-PM. But "yes to everything" is a failure mode — it makes commitments you can't keep and trains stakeholders to keep pushing.

**Framework for a no that preserves the relationship:**
1. Hear them out completely before responding
2. Acknowledge the legitimate business reason behind the request
3. Be clear and direct — don't soft-pedal it into ambiguity
4. Explain the tradeoff (not "I don't want to" but "if we do this, we don't do that")
5. Offer what you can offer (a later date, a reduced scope, a workaround)
6. Invite them into the solution

"No" delivered with transparency and a genuine reason is almost always accepted better than a soft "we'll see" that turns into a hard no two weeks later.

## Negotiating with your own team

Negotiations aren't only with stakeholders outside the product team. You also negotiate with your engineers, designers, and your manager.

**With engineers:** The scope/time/quality tradeoff is constant. Be explicit about which constraints are hard and which are flexible. Earn the right to say "this deadline is hard" by being honest when deadlines are soft.

**With designers:** Design wants more polish time; PM wants to ship. The negotiation is about what level of quality is "good enough" for this specific release and user segment.

**With your manager:** Negotiate for the resources, time, and authority you need. If you're consistently under-resourced, that's a conversation to have explicitly — not a condition to silently work around.

## Next steps

- [Stakeholder Management](stakeholder-management.md) — the relationship context around negotiation
- [Working with Engineers](../06-working-with-teams/working-with-engineers.md) — where most scope negotiations happen
