# Writing PRDs

The Product Requirements Document (PRD) is your primary output artifact as a PM. Not because documents are the goal — they're not — but because a well-written PRD is the clearest signal that you understand the problem, have a validated hypothesis, and have given the team what they need to build confidently.

This page covers what a PRD actually needs, how to write one that engineering teams will read instead of ignore, and when to skip the full PRD entirely.

## The purpose of a PRD

A PRD communicates:

1. **What problem we're solving** and why it matters
2. **Who we're solving it for** (specific user/customer segment)
3. **What success looks like** (measurable outcomes)
4. **What we're building** (scope and constraints)
5. **What we're NOT building** (explicit out-of-scope)

It does NOT communicate:
- How the solution should be implemented (that's engineering's job)
- Pixel-perfect UI specs (that's design's job)
- A complete technical spec (that's a different document)

The single most important principle in PRD writing: **WHAT and WHY, not HOW.**

## When you need a PRD

Not everything needs a PRD. Use one when:

- The feature is large enough to need alignment across multiple people or teams
- There are meaningful scope decisions to be made
- The work spans more than a single sprint
- Business stakeholders need to understand what's being built

Skip or minimize when:
- It's a small bug fix or minor UX improvement
- The team already has full context
- You're in rapid experimentation mode (a one-pager or experiment brief is better)

A two-week experiment doesn't need a 10-page PRD. A six-month platform initiative does.

## PRD anatomy

### The one-pager (for smaller features)

```
Title: [Feature name]
Date: [Date]
Author: [Your name]
Status: [Draft / In Review / Approved]

Problem
-------
[2-3 sentences: what problem does this solve? Who experiences it?]

Hypothesis
----------
[We believe that [solution] will [outcome] for [user segment].
We'll know we're right when [metric] moves by [amount] within [timeframe].]

Scope
-----
In:
- [Specific capability 1]
- [Specific capability 2]

Out:
- [What we're explicitly not doing]

Success Metrics
---------------
- Primary: [metric + target]
- Secondary: [metric + target]

Open Questions
--------------
- [Question 1]
- [Question 2]
```

### The full PRD (for larger initiatives)

```markdown
# [Product/Feature Name]

**Author:** [Name]  
**Last updated:** [Date]  
**Status:** Draft | In Review | Approved | Shipped  
**Stakeholders:** [Names and roles]

---

## Problem Statement

[What is the problem? Who has it? How do we know it exists?
Use data, customer quotes, support ticket volumes — whatever makes this concrete.]

## Background & Context

[What's the history? Has this been tried before? What changed to make it worth solving now?]

## Goals

What success looks like (measurable):
- [Goal 1: metric + target + timeframe]
- [Goal 2: metric + target + timeframe]

## Non-Goals

Explicitly out of scope:
- [Non-goal 1 — and why it's out of scope]
- [Non-goal 2]

## User Stories / Use Cases

Primary persona: [persona name]

As a [user type], I want to [action] so that [outcome].

**Key scenarios:**
1. [Scenario 1: describe the user's journey]
2. [Scenario 2]
3. [Scenario 3: edge case]

## Proposed Solution

[High-level description of what we're building. NOT implementation details.
What does the user experience look like? What does it do?]

**What this is NOT:**
[Be explicit about what you considered and decided not to include]

## Requirements

### Functional Requirements
- [Req 1]
- [Req 2]

### Non-Functional Requirements
- Performance: [e.g., page loads in <2s at P95]
- Security: [e.g., PII handling requirements]
- Accessibility: [e.g., WCAG 2.1 AA]

## Success Metrics

| Metric | Baseline | Target | Timeframe |
|--------|----------|--------|-----------|
| [Primary metric] | [current] | [goal] | [when] |
| [Secondary metric] | [current] | [goal] | [when] |

## Open Questions

| Question | Owner | Due Date |
|----------|-------|----------|
| [Q1] | [Name] | [Date] |

## Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| [Risk 1] | M | H | [How we'd handle it] |

## Dependencies

- [Team/system] — [what we need from them and when]

## Launch Plan

- Alpha: [who, when]
- Beta: [who, when]  
- GA: [when]
- Rollback plan: [how we'd revert if needed]

## Appendix

[Supporting research, customer quotes, data analysis, mockup links]
```

## The "WHAT not HOW" principle in practice

This is worth repeating because developers-turned-PM get it wrong constantly.

**Wrong:**
> "The search box will use Elasticsearch with fuzzy matching and will call the /api/search endpoint with a debounce of 300ms."

**Right:**
> "Users can search across all their documents and see results as they type, with typo tolerance for common misspellings."

You're describing the experience and the constraint ("as they type"), not the implementation. The engineering team will figure out Elasticsearch vs. Postgres full-text search vs. Typesense. That's their job. If you specify it, you've taken ownership of a decision that isn't yours and created a compliance problem — the team now has to follow your spec even if they find a better approach.

The exception: when the *implementation choice is a business decision*. Example: "We must use the existing vendor X for data storage due to our enterprise contract" — that's a constraint worth documenting. But "use Elasticsearch because I've used it before" is not.

## Keeping the PRD alive

A common PRD anti-pattern: spend two weeks writing a beautiful PRD, get it approved, then never update it. The team ships something materially different, and the PRD becomes archaeological record rather than working document.

Good practices:
- **Update the PRD when scope changes.** Don't rely on Slack messages or meeting notes to be the canonical record of what changed and why.
- **Add a "What changed" section** at the top for significant pivots. Engineers and stakeholders should be able to see the evolution.
- **Close the loop on open questions** — when a question gets answered, document the answer and the reasoning.
- **Link the PRD from your Jira/Linear epic** so it's always findable.
- **Mark it "Shipped"** when the feature launches. It's now a historical record.

## PRD reviews: what you're looking for

When you do a PRD review with stakeholders, you're checking:

1. **Problem agreement** — Do we all agree this problem is worth solving?
2. **Scope alignment** — Is the proposed scope appropriate (not too big, not too small)?
3. **Success metric buy-in** — Can we agree on what "success" looks like before we build?
4. **Dependency identification** — Are there people or teams not in the room who will be affected?
5. **Risk surfacing** — What could go wrong that we haven't thought about?

PRD review is not a rubber stamp. If you're running reviews where everyone just nods, you're either showing the PRD too late (after the team has already built it mentally) or you've created a culture where dissent feels unsafe.

## Common PRD mistakes by developer-turned-PMs

**Over-specifying the implementation.** Covered above, but worth reiterating — it's the most common failure.

**Weak problem statement.** "Users want a dashboard" is not a problem statement. "Users spend 3+ hours per week manually exporting data from three systems to create their own reporting view" is a problem statement.

**No success metrics defined.** If you can't articulate how you'll know this worked, you don't understand the problem well enough yet. Go back to discovery.

**Everything is in scope.** The out-of-scope section is as important as the in-scope section. If you can't say no to anything, your PRD isn't making decisions — it's deferring them to engineering.

**Requirements written as UI mockup descriptions.** "The button will be blue and in the top right corner" is not a functional requirement. That's a design decision. Write what the user can *do*, not what the screen looks like.

**No open questions.** Every real PRD has things that aren't fully figured out. Pretending otherwise builds false confidence and leads to surprises during development.

## The one thing

If you write nothing else, write a sharp problem statement and a clear success metric. Those two things are more valuable than five pages of requirements, because they keep the team pointed at the right outcome even when the implementation details change.

A team with a clear problem and a measurable goal will make good implementation decisions. A team with detailed requirements but no clear goal will build to spec and miss the point.

## Next steps

- [Prioritization Frameworks](prioritization-frameworks.md) — deciding which PRDs to write at all
- [Data-Driven Decisions](data-driven-decisions.md) — building the evidence that makes your PRDs credible
- [Product Brief template](../10-templates/product-brief.md) — copy-paste starting point
- [PRD template](../10-templates/prd.md) — full PRD template
