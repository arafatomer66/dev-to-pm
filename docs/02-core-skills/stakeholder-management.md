# Stakeholder Management

PMs have accountability without authority. Stakeholder management is the discipline of getting things done in that condition. It's not about being political — it's about building the relationships and communication systems that let you make good decisions at speed.

## Who are your stakeholders?

A stakeholder is anyone who has an interest in or influence over your product decisions.

**Internal stakeholders typically include:**
- Engineering leadership (what's feasible and at what cost)
- Design (UX quality and user experience)
- Sales (deals, customer commitments, competitive positioning)
- Customer Success / Support (what's breaking, what customers complain about)
- Marketing / PMM (positioning, launch timing, messaging)
- Finance (budget, revenue impact)
- Legal / Compliance (risk, regulatory constraints)
- Executive leadership (strategy alignment, resource allocation)

**External stakeholders may include:**
- Key customers (especially enterprise accounts with product influence)
- Partners / integrators
- Regulators (in regulated industries)

## The stakeholder map

Before managing stakeholders, map them. The classic 2x2: **Influence vs. Interest**

```
High Influence │ Manage Closely    │ Keep Satisfied
               │ (high interest)   │ (low interest)
               ├───────────────────┼───────────────
Low Influence  │ Keep Informed     │ Monitor
               │ (high interest)   │ (low interest)
               └───────────────────────────────────
                   High Interest       Low Interest
```

**Manage closely:** These people can block or accelerate your roadmap. They care and they have power. Invest in regular 1:1s, bring them into decisions early.

**Keep satisfied:** They can block you but aren't watching closely. Make sure they never feel surprised. A brief update email is often enough.

**Keep informed:** They care but can't move levers. They're often your champions — internal advocates who spread good word. Treat them well; don't neglect them.

**Monitor:** Low interest, low influence now — but status can change. Keep tabs without investing heavily.

The [Stakeholder Map template](../10-templates/stakeholder-map.md) gives you a working version of this.

## The trust economy

Stakeholder management runs on trust. Trust is built by:

1. **Doing what you say you'll do.** If you commit to a date or a feature, hit it. If you can't, communicate early — never let a miss come as a surprise.
2. **Being transparent about tradeoffs.** Don't hide bad news. Share it directly, with context and a plan.
3. **Making decisions their team can rely on.** When your stakeholders tell their team "PM said X," that should be accurate and stable.
4. **Acknowledging when you're wrong.** Stakeholders who've seen you change your mind based on evidence trust you more than those who've seen you stubbornly defend bad decisions.

Trust takes months to build and hours to destroy. A single "I didn't know that was happening" from a senior stakeholder is expensive.

## Saying no

This is the skill that separates PMs who stay sane from PMs who burn out.

The requests will never stop. Sales wants a feature for a deal. The CEO has a "great idea." A customer complained and their CS manager is escalating. You will never build everything people ask for. Learning to say no without destroying relationships is non-negotiable.

### The anatomy of a good "no"

A bad no: *"That's not a priority."*

A good no:
1. **Acknowledge** the underlying need (not just the request)
2. **Explain** the tradeoff in business terms, not PM preference
3. **Offer an alternative** if one exists
4. **Close the loop** — don't leave them wondering

**Example:**
> "I understand this matters for the Acme deal — that's a real business signal. Right now we've committed our Q3 engineering capacity to the payments overhaul, which unblocks five other enterprise accounts. If we redirect to this feature, those accounts slip. I'd love to revisit this for Q4 — can you help me understand the timeline pressure so I can make the case for prioritizing it?"

This "no" does several things: it acknowledges the business reason, explains the opportunity cost, and invites the stakeholder to help solve the problem rather than treating them as an adversary.

### When stakeholder pressure is actually a signal

Not all stakeholder requests should be declined. Sometimes:
- A sales team persistently asking for the same feature is valid market signal you're underweighting
- An engineering lead saying "this is more complex than you think" is preventing a future disaster
- A CS team escalating the same complaint repeatedly indicates a real usability problem

The discipline is distinguishing signal from noise. One-off requests are noise. Patterns across multiple stakeholders are signal.

## Managing up

"Managing up" means keeping your manager and leadership chain informed in ways that build trust and protect your team's ability to do good work.

### The weekly status update

Most PMs underinvest in proactive upward communication and pay for it with reactive requests for updates. A short weekly status update (email, Slack, or brief doc) that answers:
- What shipped or major decision was made this week
- What's at risk or blocked
- What I need from leadership

... prevents most "why didn't I know about this?" conversations.

### How to escalate

When something is genuinely blocked by a stakeholder conflict, escalation is appropriate. How to do it well:

1. Attempt to resolve at the working level first (you tried to get alignment and couldn't)
2. Frame it as a business decision, not a conflict (don't make it personal)
3. Present the options and your recommendation — don't just dump the problem
4. Be clear about the deadline (why does this need to be resolved now?)

Escalate too often and you lose credibility ("can't handle their own problems"). Never escalate and some things stay blocked forever. Calibrate.

## Handling difficult stakeholders

### The HiPPO (Highest Paid Person's Opinion)

The CEO / VP who overrides your prioritization based on gut feel.

**Strategy:** Build your decision-making process into a system they respect. When the HiPPO makes a request, walk them through the tradeoff: "We can do this. Here's what we'd need to not do. Which do you prefer?" Often, the HiPPO just wants to feel heard — they're not actually demanding you drop everything.

### The sales team that owns your roadmap

Sales teams are incentivized to close deals. Your roadmap should not be their feature list.

**Strategy:** Create a structured intake process for sales-driven feature requests. Classify them: is this a one-off deal request, or is multiple customers asking for the same thing? One-offs should be evaluated as custom work or professional services. Patterns belong in discovery.

### The engineering team that says "no" to everything

This usually isn't stubbornness — it's either legitimate technical concern or a symptom of capacity over-commitment.

**Strategy:** Understand what specifically they're pushing back on. Is it the scope? The timeline? The technical approach? Separate these. Often "we can't build this" means "we can't build this by your date" or "we can't build it the way you specified."

### The stakeholder who keeps changing requirements

**Strategy:** Distinguish between requests that are new information vs. scope creep vs. changing minds. New information (customer research, market shift) should update the spec. Scope creep and changing minds need a structured change process — document the change, the reason, and the impact.

## Communication cadences

A sustainable stakeholder communication system:

| Audience | Cadence | Format | Content |
|----------|---------|--------|---------|
| Direct team | Daily/weekly | Standup / async | Blockers, decisions, day-to-day |
| Engineering lead | Weekly 1:1 | Conversation | Technical tradeoffs, team health, upcoming work |
| Design lead | Weekly 1:1 | Conversation | Runway, feedback quality, design debt |
| Marketing / PMM | Bi-weekly | Sync or written | Launch timing, messaging, positioning |
| Sales | Monthly or as-needed | Written | Roadmap updates, feature timelines |
| Leadership | Weekly | Status update | Progress, risks, decisions needed |
| Key customers | Quarterly (or ongoing for enterprise) | Call | Feedback, product direction, relationship |

Adjust based on your context. The point is that these cadences are *proactive* — you're not waiting for someone to ask.

## Next steps

- [Communication & Storytelling](communication-and-storytelling.md) — how to present your decisions compellingly
- [Negotiation](negotiation.md) — the mechanics of reaching agreement
- [Stakeholder Map template](../10-templates/stakeholder-map.md)
