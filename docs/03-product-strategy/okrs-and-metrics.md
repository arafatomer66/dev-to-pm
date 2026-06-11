# OKRs & Metrics

OKRs (Objectives and Key Results) are the most widely used goal-setting framework in tech. They're also widely misused. This page covers how to write OKRs that actually guide decisions, and how to build a metrics framework that doesn't measure things for the sake of measuring them.

## What OKRs are for

OKRs answer two questions:
1. Where are we going? (Objective)
2. How will we know we're getting there? (Key Results)

They're meant to create alignment (everyone knows what matters this quarter), focus (explicit about what we're NOT doing), and accountability (measurable commitments).

**What they're not:**
- A task list (KRs are outcomes, not outputs)
- A performance review tool (though many companies misuse them this way)
- A complete product strategy (OKRs translate strategy into measurable bets; they don't replace strategy)

## Writing good Objectives

A good Objective is:
- **Qualitative and inspirational** — it describes a direction worth pursuing
- **Time-bound** — typically one quarter
- **Actionable** — the team can influence it
- **Clear** — no jargon that requires interpretation

**Weak Objectives:**
- "Improve product quality" (too vague)
- "Ship the authentication overhaul" (output, not outcome)
- "Be the best analytics platform" (unmeasurable, generic)

**Strong Objectives:**
- "Make our product the obvious choice for mid-market finance teams"
- "Dramatically improve how quickly new customers reach first value"
- "Build the trust and security capabilities enterprise buyers require"

## Writing good Key Results

A good Key Result is:
- **Measurable** — you can unambiguously determine whether you hit it
- **Outcome-focused** — it describes what changes, not what you do
- **Challenging but achievable** — Google's 70% as a "good" score guideline is useful
- **Paired with context** — baseline and target, not just a number

**Weak Key Results:**
- "Launch the new onboarding flow" (output)
- "Improve NPS" (which direction? by how much?)
- "Complete 10 customer interviews" (activity, not outcome)

**Strong Key Results:**
- "Increase 7-day activation rate from 42% to 60%"
- "Reduce time-to-first-dashboard from 4 days to 1 day for new accounts"
- "Achieve NPS of 40+ (from current 28) with enterprise accounts"

## OKR cadences

| Cadence | Typical use |
|---------|------------|
| **Annual** | Company-level OKRs, directional; reviewed at mid-year |
| **Quarterly** | Team and product OKRs; the primary operational unit |
| **Monthly** | Check-ins on quarterly OKRs; not new OKR cycles |
| **Weekly** | Key result updates; status signals, not goal-setting |

Quarterly OKRs are the most useful for PMs. They're long enough to make meaningful progress on outcomes, short enough to adapt when you learn something.

## How many OKRs?

Less is more. Recommended:
- 3–5 Objectives per team per quarter
- 2–4 Key Results per Objective
- 1–2 "company-committed" OKRs + 1–2 team-discretionary OKRs

If you have 8 Objectives, you don't have a strategy — you have a wish list.

## Grading OKRs

At the end of the quarter, grade each KR:
- 0.0–0.3: Missed
- 0.4–0.6: Made partial progress
- 0.7–0.9: Hit or nearly hit
- 1.0: Fully achieved

Google's original OKR philosophy: if you're consistently hitting 1.0 on everything, your OKRs are too easy. Aim for ~0.7 average. If you're consistently hitting 0.3, they're too ambitious or the team is too under-resourced.

The grading conversation is as valuable as the OKR-setting conversation. What did we learn? What would we change? What got in the way?

## Product metrics framework

OKRs are quarterly bets. A metrics framework is the ongoing system for understanding product health.

**Hierarchy:**

```
North Star Metric
    ↑
Input Metrics (levers that drive the North Star)
    ↑
Feature/Experiment Metrics (granular, short-term)
```

**Example for a B2B SaaS analytics tool:**

| Level | Metric |
|-------|--------|
| North Star | Weekly active users who create a report |
| Input — Acquisition | Trial sign-ups, qualified pipeline from product-led motion |
| Input — Activation | % of trials who create their first report within 7 days |
| Input — Retention | 60-day retention of accounts that activated |
| Input — Expansion | Accounts that upgrade to higher tier within 90 days |
| Feature metric | % of active users who've used the new auto-refresh feature |

## Counter-metrics

Every metric you optimize should have a counter-metric that prevents you from gaming it at the expense of something important.

| Primary metric | Counter-metric |
|----------------|---------------|
| Activation rate | Day-30 retention (high activation that churns fast is bad) |
| Feature adoption | Support ticket volume (adoption via confusion is bad) |
| Time-to-close deals | Deal size / ICP match (faster closing bad customers is bad) |
| NPS | Usage frequency (users who love you but don't use you aren't saved) |

Without counter-metrics, teams find the path of least resistance to the target metric, which usually produces bad outcomes.

## OKR anti-patterns

**The cascade tax:** Every level of the org adding OKRs that are just decompositions of the level above. By the time you get to teams, the OKRs are task lists.

**OKRs as performance review inputs:** When people fear being graded on OKRs, they sand-bag targets and claim credit for things they didn't control. OKRs should be team goals, not individual performance.

**Set and forget:** OKRs that are written in January and reviewed in December. If you're not looking at your OKRs monthly, they're not guiding decisions.

**Metric proliferation:** "We track 47 metrics." If you track everything, you optimize nothing. Three to five key results per quarter is the right number. Everything else is a diagnostic metric you check when something moves unexpectedly.

**Lagging-only OKRs:** "Increase quarterly revenue by 15%" is a lagging metric — by the time you know you've missed it, the quarter is over. Pair lagging KRs with leading indicators that tell you sooner.

## Next steps

- [Vision & Strategy](vision-and-strategy.md) — the strategy your OKRs should express
- [Data-Driven Decisions](../02-core-skills/data-driven-decisions.md) — building the measurement infrastructure
- [Metrics Framework template](../10-templates/metrics-framework.md)
