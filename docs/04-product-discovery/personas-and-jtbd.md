# Personas & Jobs-to-be-Done

"Users" is too vague to make decisions against. When you say "users want X," which users? All of them? The power users who generate 80% of your NPS? The churned users you're trying to win back? The enterprise buyers who never touch the product?

Personas and Jobs-to-be-Done (JTBD) are two frameworks for making "users" small enough and specific enough to guide real decisions.

## Personas

A persona is a composite representation of a user segment based on research. It's not a fictional character — it's a pattern synthesis of real people you've talked to.

A useful persona includes:
- **Demographics:** Job title, company size, industry, seniority
- **Context:** What their typical day looks like; what tools they use; how our product fits in their workflow
- **Goals:** What they're trying to accomplish (professional and personal)
- **Frustrations:** What gets in their way; what they hate about current solutions
- **Behaviors:** How they actually use the product; what they reach for first
- **Quotes:** Real verbatims from interviews that capture their perspective

A persona that nobody uses is a bad sign. If your team can't recall the persona names and core needs, they're decorative research artifacts.

**The test of a useful persona:** Can your engineering team make a scope decision by asking "what would Persona A need from this feature?" If yes, the persona is real and useful. If not, it needs more specificity.

### How many personas?

Two to four is usually right. More than five means you haven't done the synthesis work to find the patterns. One means you're building for yourself.

For a B2B product, separate the **buyer** from the **user**. The VP of Finance who signs the contract has completely different needs from the FP&A analyst who uses the product daily. Both are personas.

## Jobs-to-be-Done (JTBD)

JTBD is a framework from Clayton Christensen and Tony Ulwick: customers "hire" products to do a job in their life. The "job" is the underlying motivation, not the surface-level feature request.

**The classic example:** People don't want a quarter-inch drill. They want a quarter-inch hole. (And actually, they want a shelf on the wall. The drill is one way to get there.)

A jobs-to-be-done statement:

```
When [situation],
I want to [motivation / what they're trying to do],
so I can [expected outcome].
```

**Example:**
> "When I'm presenting our financial results to the board, I want to have a polished, consistent presentation ready without spending hours reformatting data from multiple sources, so I can focus my preparation time on the story, not the mechanics."

This job statement tells you:
- **Situation:** Board presentation prep
- **Motivation:** Polished presentation without manual effort
- **Outcome:** Time freed for strategic thinking

Compare this to a feature request: "Users want better reporting." That's a request. The JTBD is the reason.

## Why JTBD > feature requests

Feature requests tell you what customers think they want. Jobs tell you what they're actually trying to accomplish — and often reveal that there are better ways to accomplish it than the specific feature requested.

**Real example pattern:**
> Customer requests: "Can you add a scheduled email export?"

The obvious response: build scheduled email export.

The JTBD response: understand the job. "When [I need to keep my manager updated on campaign performance], I want to [automatically share the latest numbers without having to remember to do it manually], so I can [focus on analysis rather than reporting mechanics]."

Suddenly you see three possible solutions: scheduled email export, Slack integration, a "share with team" mode, auto-updated embed links. The JTBD opens the solution space; the feature request closes it.

## When to use personas vs. JTBD

Use personas when:
- You need alignment on who you're building for
- Different segments have fundamentally different needs
- Onboarding new team members to the user base

Use JTBD when:
- You're in discovery and need to understand motivation
- A feature request arrives and you want to understand the underlying need
- You're evaluating competing solution approaches
- You're writing a PRD and need to anchor the problem statement

They're complementary. A persona describes who your user is. JTBD describes what they're trying to accomplish. The best product decisions use both.

## Practical JTBD in PRDs

When you write a PRD, anchor the problem statement in a JTBD:

> "Our finance persona (Controller / FP&A Manager at mid-market companies) has the following job: when preparing for monthly leadership reporting, they need to consolidate actuals from three systems into one coherent view, without it taking all day. Today, they spend 3–6 hours manually downloading CSVs and reconciling in Excel. We're building [feature] to do this automatically."

This is more actionable than "users want better reporting" because it specifies who, what situation, what they're trying to do, and why the current experience is painful.

## Next steps

- [User Research](user-research.md) — building the personas and JTBD from real interview data
- [Writing PRDs](../02-core-skills/writing-prds.md) — where persona and JTBD anchoring happens in practice
- [Persona/JTBD worksheet template](../10-templates/user-research-guide.md)
