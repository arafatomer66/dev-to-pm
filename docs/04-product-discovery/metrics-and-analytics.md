# Metrics & Analytics

Analytics is the infrastructure that makes data-driven product decisions possible. This page covers what PMs need to know about instrumentation, how to read a funnel, and how to build the analytics habits that make you a better product leader over time.

## Instrumentation discipline

The most common analytics failure: building features without tracking whether they're used.

Every feature you ship should have events tracked before launch — not after. The "we'll add tracking later" promise is almost never kept, and you end up with features where you genuinely don't know if anyone uses them.

**Events to track for every feature:**
- Feature surface viewed / page loaded
- Primary action taken (the thing the feature is meant to do)
- Completion / success event (did the user accomplish what they came to do?)
- Error events (what went wrong?)

**The PM's role:** Include analytics requirements in the PRD. Don't leave it to engineering to guess what you need. Example:

```
Analytics Requirements:
- Event: report_builder_opened (properties: user_id, team_id, source)
- Event: report_saved (properties: user_id, report_type, field_count)
- Event: report_shared (properties: user_id, recipient_count, report_id)
- Funnel: report_builder_opened → report_saved → report_shared
```

## Reading a funnel

A funnel shows the step-by-step drop-off between stages of a user journey. Example for an onboarding funnel:

```
Sign up         100% (1,000 users)
   ↓ 70%
Verify email     70% (700 users)
   ↓ 80%
Complete profile  56% (560 users)
   ↓ 60%
First action      34% (340 users)
   ↓ 50%
7-day return      17% (170 users)
```

**Where to focus:** The biggest absolute drop-off is usually the highest-leverage intervention. In this example, the email verification step loses 300 users — more than any other step. That's where to start.

**Cohort analysis:** Compare funnels for different user cohorts (signed up via different channels, different time periods, different plans). Often the aggregate funnel hides significant variation between segments.

**Attribution:** Don't just look at where users drop off — look at where the users who *succeeded* came from. If 80% of users who complete the funnel came through one acquisition channel, that's signal.

## Leading vs. lagging indicators

**Leading indicators:** Predict future outcomes. Faster feedback. Noisier.
- Day-7 retention predicts Day-30 retention
- Feature adoption in week 1 predicts long-term engagement
- Support ticket volume predicts churn risk

**Lagging indicators:** Measure actual outcomes. Slow but accurate.
- Revenue
- Churn rate
- Net Promoter Score (if measured quarterly)

Build a dashboard with both. Check leading indicators weekly to catch problems early. Review lagging indicators monthly to confirm your direction.

## Cohort retention analysis

Retention is the most important metric for most products. A retention curve shows: of users who started in a given period (cohort), what percentage are still active N periods later?

A healthy retention curve levels off (flattens) — users who stay past a certain point are "sticky" and unlikely to churn. A retention curve that continues sloping downward has no floor — you're losing everyone eventually.

Reading a cohort grid:

```
         Week 1  Week 2  Week 3  Week 4
Jan cohort  100%    60%     45%     40%
Feb cohort  100%    55%     42%     38%
Mar cohort  100%    70%     58%     55%
```

The March cohort is significantly better — something changed. What was different for March users? Was there a product change? A different acquisition channel? Onboarding improvement? Investigating this is how you find what's actually working.

## The PM's analytics toolkit

You don't need to be a data scientist. But you should be able to:

**Pull your own data.** Basic SQL is the most valuable skill for a PM who works with databases. A query like:
```sql
SELECT 
  DATE_TRUNC('week', created_at) as week,
  COUNT(DISTINCT user_id) as new_users,
  COUNT(DISTINCT CASE WHEN returned_within_7_days THEN user_id END) as retained
FROM users
GROUP BY 1
ORDER BY 1;
```
... is not advanced SQL. It's a retention calculation that you should be able to write yourself rather than waiting for a data analyst.

**Read an analytics dashboard.** Tools like Mixpanel, Amplitude, Heap, Looker. Know how to build a basic funnel, a retention chart, and an event trend.

**Interpret an A/B test result.** Know what p-value means, why sample size matters, and how to read a confidence interval.

**Communicate data to stakeholders.** Know how to take a complex dashboard and reduce it to the three numbers that matter for a given decision.

## When numbers lie

Data dashboards can mislead. Common traps:

**Selection bias:** You're measuring active users, but churn happens among users who stop being active. Your "happy user" data is systematically excluding the people most likely to churn.

**Survivorship bias:** Features used by long-term users appear successful. But maybe only users who were already going to stay long-term ever discovered those features.

**Correlation ≠ causation:** Users who use Feature X have higher retention. But maybe users with high intent use both Feature X and stick around — Feature X didn't cause the retention.

**Metric definition drift:** "Active user" meant one thing six months ago and means something different now. Comparing current numbers to historical numbers without checking the definition change is misleading.

The discipline: whenever you see a striking number, ask "why might this be misleading before I report it?"

## Next steps

- [Data-Driven Decisions](../02-core-skills/data-driven-decisions.md) — building the decision-making culture
- [OKRs & Metrics](../03-product-strategy/okrs-and-metrics.md) — connecting analytics to strategy
- [Metrics Framework template](../10-templates/metrics-framework.md)
