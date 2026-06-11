# Launch Planning

A feature that ships but nobody knows about is a tree falling in an empty forest. Launch planning is how you convert engineering work into business outcomes.

## Launch tiers

Not every feature deserves the same launch investment. Triage first.

| Tier | What it is | Launch activities |
|------|-----------|------------------|
| **Tier 1** | Major launch — new product, major new capability, strategic announcement | Press release, blog post, email blast, sales enablement, webinar, changelog |
| **Tier 2** | Significant feature — meaningful improvement with broad impact | Blog post or in-product announcement, sales enablement, changelog, customer email |
| **Tier 3** | Incremental improvement — useful but narrow impact | Changelog, in-product tooltip, brief customer segment email |
| **Tier 4** | Bug fix / polish | Changelog only (if that) |

Tier inflation is a real problem — every team wants their work to be a Tier 1 launch. Define the criteria explicitly and stick to them.

## The launch timeline

For a Tier 1 or Tier 2 launch, work backwards from your launch date:

```
T-8 weeks: Feature requirements finalized; launch plan drafted; PMM briefed
T-6 weeks: Marketing messaging and positioning locked
T-4 weeks: Beta/design partner feedback incorporated
T-3 weeks: Sales enablement materials drafted
T-2 weeks: Blog post written; email drafted; internal announcement ready
T-1 week:  Sales trained; CS trained; support docs updated; press briefings if applicable
T-0:       Launch
T+1 week:  Launch metrics review
T+4 weeks: Post-launch outcomes review
```

The most common launch failure: engineering finishes the feature, then the PM scrambles to "do the launch stuff" in the last week. Marketing finds out days before launch and scrambles to write copy with no context. The result is a weak launch that doesn't create the adoption the feature deserves.

## Feature flags and rollout strategies

A hard cutover to 100% of users on Day 1 is rarely the right approach. Feature flags let you roll out gradually and safely.

**Gradual rollout stages:**

1. **Internal alpha:** Team only, catch obvious bugs
2. **Closed beta:** Trusted design partners, 5–20 customers, deep feedback
3. **Open beta / early access:** Self-selected customers, broader feedback
4. **Percentage rollout:** 5% → 20% → 50% → 100%, monitoring for regressions at each stage
5. **General availability:** All customers

At each stage, define: what metric are you watching? What would cause you to pause the rollout?

For high-risk changes (payment flow, authentication, data migration), keep the rollback plan explicitly documented and tested before launch.

## The launch brief

A launch brief aligns marketing, sales, CS, and leadership before launch. It answers:

```
What is launching?
[Short description of the feature/product]

Who is it for?
[Specific customer segment and persona]

What problem does it solve?
[One paragraph on the customer pain]

What's the key message?
[One sentence a customer would repeat to a colleague]

Why is this different from alternatives?
[The differentiation]

What are the key proof points?
[Beta customer quotes, data, metrics]

How does it fit into our pricing?
[What tier, any pricing changes]

What do Sales need to know?
[Objection handling, competitive positioning]

What do CS need to know?
[How to explain it, common support questions]

Launch timeline
[Key dates]

Success metrics
[What we'll measure, what "good" looks like]
```

Share this with all go-to-market stakeholders at T-4 weeks minimum.

## Post-launch review

Most teams spend months building a feature and 10 minutes reviewing what happened after it launched. This is backwards.

**4-week post-launch review agenda:**

1. **Adoption:** What % of target users have tried the feature? Is it what we predicted?
2. **Outcome:** Did the metric we said we'd move, move? By how much?
3. **Qualitative:** What are users saying? What are support tickets saying?
4. **What we'd do differently:** If we were launching this again, what would we change?
5. **Next steps:** Build out more, iterate on this version, or pivot focus?

Make this a real meeting with your team. Document the outcomes. Over time, post-launch reviews build your team's intuition for what actually works and what doesn't.

## Common launch mistakes

**Shipping without sales enablement.** Sales will be asked about the feature tomorrow. If they don't know what it does, they'll guess — and often guess wrong.

**No in-product discovery.** A feature that users can't find has zero adoption. Plan in-product education (tooltip, onboarding modal, empty state) alongside the feature.

**Forgetting existing customers.** If you've been in beta with 10 customers and you now launch to 10,000, make sure those 10 customers know. They're your most important advocates.

**No rollback plan.** "We'll figure it out if something goes wrong" is not a plan. Who makes the call to rollback? How long does it take? What customer communication is required?

**Success theater.** Announcing a launch with press and fanfare, then quietly not measuring whether it worked. This is common and corrosive — it trains the team to optimize for announcements rather than outcomes.

## Next steps

- [Working with Marketing](working-with-marketing.md) — the launch messaging relationship
- [Working with Sales](working-with-sales.md) — sales enablement and competitive positioning
- [Launch Checklist template](../10-templates/launch-checklist.md)
