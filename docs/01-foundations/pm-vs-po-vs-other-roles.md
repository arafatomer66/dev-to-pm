# PM vs PO vs Other Roles

The product/tech org has accumulated a lot of job titles. This page maps the landscape honestly — what each role actually does, where they overlap, and how to figure out which one you're actually moving toward.

## The landscape

| Role | Owns | Reports to |
|---|---|---|
| Product Manager (PM) | Product strategy, discovery, roadmap, GTM | VP Product / CPO |
| Product Owner (PO) | Backlog, sprint delivery, acceptance | PM or directly to Scrum team |
| Project Manager | Timeline, budget, delivery coordination | PMO / Engineering Manager |
| Program Manager (TPM/EPM) | Cross-team initiative coordination | VP Engineering or VP Product |
| UX Designer | User experience, interaction design | Design Lead |
| Tech Lead / Staff Engineer | Technical direction, architecture | Engineering Manager |

## PM vs Product Owner

This is the most confusing distinction, and it's made worse by the fact that many companies use the titles interchangeably.

### The textbook version

In a mature Scrum organization:

- **PM** works at the strategy layer: sets the product vision, owns the roadmap, makes build/buy/partner decisions, talks to customers, does competitive analysis, defines success metrics.
- **PO** works at the delivery layer: owns and orders the product backlog, writes and refines user stories, participates in all Scrum ceremonies, accepts or rejects sprint output.

The PM feeds the PO's backlog with validated, prioritized work. The PO translates that work into sprint-ready stories and keeps the engineering team unblocked.

### The reality

Most companies blend these roles. What you'll actually encounter:

**Startup (1–50 people):** One person does both. Title varies — often "PM" or "Head of Product." They do everything from user interviews to story-pointing.

**Mid-size (50–500 people):** Often one PM per product area who does light backlog management themselves. "PO" title rare. PMs are responsible for delivery quality without a dedicated PO beneath them.

**Large enterprise (500+ people):** Dedicated POs embedded in Scrum teams, with PMs one level up owning strategy and roadmap. This is where the PM/PO split is cleanest.

**Consulting / IT services firms:** "PO" is very common; "PM" less so. The PO in these contexts often acts as a client proxy on an outsourced team.

### Which path should you take?

If you want to stay close to Agile delivery and work most tightly with an engineering team day-to-day, PO is a natural developer transition. See [dev-to-po](https://github.com/arafatomer66/dev-to-po) for that path.

If you want to own product strategy, roadmap, GTM, and business outcomes — and are comfortable operating more independently from the sprint — PM is the path. This repo is for that path.

Neither is better. They're different jobs. At many companies, PO is a stepping stone to PM, but that's not universal.

## PM vs Project Manager

**Project Manager:** Owns scope, timeline, and budget for a defined project. Success = on time, in scope, within budget. They execute a plan someone else defined.

**Product Manager:** Defines what the scope should be. Doesn't manage timelines; influences them. Success = value delivered to users and business. They set the direction and make the tradeoffs.

The easiest way to distinguish: a Project Manager asks "are we on track?" A PM asks "should we still be building this?"

At many traditional enterprises, what they call "PM" is actually a Project Manager who happens to work on software. If you're interviewing, ask: "Does the PM define the product vision and roadmap, or are those handed down from above?" If it's the latter, it may be closer to a Project Manager role than a product strategy role.

## PM vs Program Manager / TPM / EPM

Program Managers, Technical Program Managers (TPM), and Engineering Program Managers (EPM) coordinate across teams to land large initiatives. They're not accountable for product strategy — they're accountable for the coordination machinery.

A typical split on a large launch:
- **PM:** What is being built and why; what does success look like?
- **TPM/EPM:** Who is doing what and when; what are the dependencies; what could block the launch?

At FAANG companies, TPMs are a distinct, high-status career path. At smaller companies, the PM often absorbs this work, and it's the part they like least.

## PM vs Tech Lead / Staff Engineer

This is the relationship that has the most potential for friction when a developer becomes a PM.

**Tech Lead / Staff Engineer:** Owns technical direction, architecture decisions, code quality standards, and engineering team health. Answers: "How should we build this?"

**PM:** Owns what gets built and why. Answers: "What should we build?"

The critical principle: **PMs do not own technical decisions.** When you move from engineering into PM, you give up your vote on architecture. You can express a preference, share a business constraint, ask about tradeoffs — but the final technical call belongs to engineering.

Developer-turned-PMs violate this constantly in their first year. It damages trust with the engineering team and creates dependency where there should be empowerment.

The healthy relationship: deep mutual respect, honest disagreement on scope and timeline, and clear role boundaries.

## How the titles vary by company

| Company type | What "PM" usually means |
|---|---|
| Early-stage startup | Everything: strategy, delivery, sometimes coding, customer calls, pricing |
| Growth-stage startup | Clear product strategy ownership; delivery support but not full PO |
| Big tech (FAANG) | Defined scope, lots of process, heavy on data and experimentation |
| Enterprise software | Mix of strategy and business requirements; often large customer-facing component |
| Consulting/agency | Usually project-delivery focused; limited discovery and strategy |
| Platform/infrastructure | Very technical; close to engineering; often involves developer experience |

## Before accepting a PM role: questions to ask

When you're evaluating a PM role, these questions reveal what the job actually is:

1. "Who sets the product vision and roadmap?" (If it's not the PM, understand why)
2. "How much time does the PM spend with customers per month?"
3. "What does the PM own vs. the engineering team on launch decisions?"
4. "Is there a separate PO role, or does the PM manage the backlog directly?"
5. "How is PM success measured?"

The answers will tell you whether you're signing up for a strategy-and-discovery role or a well-dressed project coordinator role.

## Summary

| If you want to… | Go toward… |
|---|---|
| Own product vision, strategy, and business outcomes | PM |
| Stay close to the Scrum team and sprint delivery | PO |
| Coordinate complex cross-team deliveries | TPM/EPM |
| Keep deep technical ownership | Staff Engineer / Tech Lead |
| Manage scope and timelines for defined projects | Project Manager |

Next: [From Dev Mindset to PM Mindset](dev-vs-pm-mindset.md) — the mental shifts that actually matter.
