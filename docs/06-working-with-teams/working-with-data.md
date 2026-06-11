# Working with Data

Most companies above 30 people have a data function — analysts, data scientists, or a data engineering team. PMs who know how to work with data teams get dramatically better outcomes than PMs who treat analytics as a downstream reporting function.

## What the data team can do for you

**Analyze user behavior:** Cohort analysis, funnel analysis, retention modeling, feature adoption reporting.

**Design and analyze experiments:** A/B test setup, sample size calculation, statistical analysis of results.

**Build dashboards:** Persistent monitoring of your key product metrics.

**Run ad hoc queries:** Answer specific questions on demand ("how many users did X in the past 30 days?")

**Build predictive models:** Churn prediction, conversion propensity, LTV estimation.

**Instrument and validate events:** Ensure your tracking is correct and complete.

## What data teams need from PM

**Clear questions.** "Can you look at our analytics?" is not a question. "I want to understand why activation rate dropped 8% in March — can you help me identify the primary drop-off point and whether there's a correlation with the March cohort's acquisition channel?" is a question.

**Context.** Data analysts don't always know what changed when. Product releases, marketing campaigns, seasonal effects, pricing changes — all of these affect metrics, and the PM is the one who knows the product history. Share it proactively.

**Prioritization signal.** Data teams have multiple PMs requesting analysis simultaneously. Tell them which requests are urgent and why.

**Feedback loop.** If an analysis was incomplete or based on the wrong definition, tell them. They want to produce useful work.

## How to write a good data request

```
Question: [One clear question the analysis should answer]

Context: [Why this matters, what decision it will inform]

Relevant metrics/events: [What data sources are relevant]

Definition clarity: [How "active user" or other key terms should be defined]

Priority: [Urgent / this sprint / this quarter]

Ideal output: [Dashboard, CSV, chart, written summary]

Timeline: [When you need it]
```

Writing this takes 10 minutes and saves the analyst hours of back-and-forth.

## Developing your own SQL skills

If you have a development background, SQL is likely within reach. For PM purposes, you need:

- `SELECT`, `WHERE`, `GROUP BY`, `ORDER BY`
- Basic aggregations: `COUNT`, `SUM`, `AVG`, `MAX`, `MIN`
- `JOIN` (inner and left)
- Date functions (truncating to week/month, date differences)
- `CASE WHEN` for conditional logic

With these, you can answer 80% of your own product questions without waiting for an analyst. The ability to pull your own data is one of the highest-leverage PM skills you can build.

**Learning resource:** Mode Analytics SQL tutorial, Khan Academy's SQL course, or just start writing queries against your real product data with a data team member to review.

## Working on experiments together

The PM-analyst relationship is especially important for experiment design and analysis.

Before running an experiment, align on:
- **Hypothesis:** What are you testing and why?
- **Primary metric:** What is the single metric that determines success?
- **Guardrail metrics:** What metrics should not move negatively?
- **Minimum detectable effect:** What's the smallest improvement worth detecting?
- **Required sample size:** Given your traffic, how long does the experiment need to run?
- **Segment definitions:** Are you running on all users or a specific segment?

After the experiment:
- Review the results together
- Don't let the PM interpret the data alone — analysts often catch subtleties (novelty effects, sample ratio mismatch, confounding variables) that PMs miss
- Document the conclusion and the reasoning — future you will want to know what you learned

## Data integrity: the PM's responsibility

PMs are often the last line of defense on data quality, because they see the outputs and also know the product context.

Common data integrity problems:
- **Missing events:** A feature shipped without tracking
- **Double counting:** Events fired multiple times per action
- **Wrong definitions:** "Active user" means different things in different queries
- **Data pipeline delays:** Dashboard shows 3 days ago, but you're making today's decision
- **Sample ratio mismatch in A/B tests:** Unequal traffic allocation invalidates results

When a metric looks unexpectedly good or bad, your first question should be: "Could this be a data issue?" Check the definition, check the pipeline, and verify with the analyst before reporting to stakeholders.

## Next steps

- [Data-Driven Decisions](../02-core-skills/data-driven-decisions.md) — the PM decision-making framework
- [MVPs & Experiments](../04-product-discovery/mvp-and-experiments.md) — experiment design in practice
- [Metrics & Analytics](../04-product-discovery/metrics-and-analytics.md) — instrumentation and funnel analysis
