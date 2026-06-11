# Discovery & Validation

Discovery is the practice of figuring out what to build before you build it. It sounds obvious. It's widely skipped.

## The build trap

The build trap is the organizational condition where output (features shipped) is mistaken for progress. Teams in the build trap:
- Receive feature requests from stakeholders and build them without validating the problem
- Measure success by story points and releases
- Rarely talk to customers except to validate features they've already decided to build
- Have a roadmap that's 80% backlog items, 20% strategy

The build trap is comfortable for developers-turned-PM because it's familiar. You know how to write requirements and ship features. What feels unfamiliar — and is therefore avoided — is sitting with a problem before jumping to solutions.

## Continuous discovery

Teresa Torres's continuous discovery framework: maintain a weekly cadence of customer contact, learn systematically, and connect learning to decisions in a structured way.

The key word is *continuous*. Discovery is not a phase that happens before development. It's an ongoing practice that runs in parallel with delivery.

**Minimum viable discovery practice:**
- 2–3 customer interviews per week (you, or someone on the team)
- A shared opportunity-solution tree that's updated as you learn
- A habit of asking "what would change our mind?" before building something

You don't need a dedicated research team to do this. PMs at small companies can maintain a Notion doc with interview notes, tagged by theme, reviewed monthly.

## Escaping the build trap: the assumption test

Before building any significant feature, list the assumptions it rests on:

1. Users have this problem
2. This problem is important enough to solve
3. Our solution would solve it
4. Users would adopt our solution
5. Adopting it would create business value

Then ask: which of these is most likely to be wrong? Which, if wrong, would waste the most engineering time?

Test that assumption first — with the cheapest possible experiment.

**Assumption testing formats:**

| Method | Tests | Cost |
|--------|-------|------|
| Customer interview | Problem severity, current workarounds | Low |
| Fake door test | Whether users click on a feature before it exists | Low |
| Landing page test | Whether a new product/feature has enough demand | Low |
| Prototype test | Whether the UX works | Medium |
| Wizard of Oz | Whether the value is real (manual process pretending to be automated) | Medium |
| Concierge MVP | Whether customers will use/pay for a service | Medium |
| Painted door (sales) | Whether prospects would include it in a deal | Low |

The goal: fail fast and cheaply before expensive engineering time is committed.

## Opportunity-solution trees

An opportunity-solution tree (from Teresa Torres) is a visual structure that maps:
- **Desired outcome** at the top (your OKR)
- **Opportunities** (unmet customer needs) in the middle
- **Solutions** (potential features) below each opportunity
- **Experiments** (tests of the solutions) at the leaves

This structure prevents solution-first thinking by forcing you to name the opportunity (problem) before proposing a solution. It also makes the relationship between solutions and outcomes visible — if a solution doesn't connect to a real opportunity, it shouldn't be in the tree.

## Discovery for B2B vs. consumer products

**Consumer:** Broad user base, often can't talk to most users. Quantitative data is rich. User and buyer are usually the same person. Discovery through analytics + targeted interview panels.

**B2B:** Smaller, more accessible user base. Can (and should) talk to real customers. Buyer and user are often different people with different needs. Win/loss data is discoverable. Discovery often starts with customer calls, not analytics.

As a developer moving into PM, B2B discovery is more tractable early on. You can have five customer calls and get more signal than most analytics dashboards.

## The discovery habit stack

What good discovery looks like as a weekly practice:

| Activity | Frequency | Time |
|----------|-----------|------|
| Customer interview | 2–3x/week | 30–45 min each |
| Interview synthesis + tagging | Weekly | 30 min |
| Team share-out of learnings | Bi-weekly | 30 min |
| Opportunity tree update | Weekly | 20 min |
| Assumption test design | Monthly | 1 hour |

This is not a lot of time. 3–4 hours per week of disciplined discovery changes the quality of every roadmap decision you make.

## Next steps

- [User Research](user-research.md) — how to actually run customer interviews
- [MVPs & Experiments](mvp-and-experiments.md) — the experiment side of discovery
- [Personas & Jobs-to-be-Done](personas-and-jtbd.md) — making discovery insights usable
