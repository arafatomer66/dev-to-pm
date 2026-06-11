# From Request to Outcome: An End-to-End Walkthrough

*One feature followed for four months, from a sales request to a measured outcome. Every concept in the curriculum touched once.*

---

## The setup

**Company:** Claros — a B2B SaaS analytics tool for mid-market finance teams (100–1,000 employees). ~$8M ARR, ~180 customers, 12-person product/engineering team.

**You:** PM for the core analytics product, six months into the role, former backend developer.

**The request arrives on a Tuesday morning.**

---

## Month 1: The Request

An AE named Jordan pings you on Slack:

> "Hey — BigCo prospect (300 person logistics company) wants to know if we can schedule reports to auto-send to their CFO every Monday. Without this, they're probably going with Competitor X. $60K ACV deal."

Your instinct: build it. Scheduled reports sounds simple. You've seen how the backend works.

**Stop.** This is the moment that separates PM thinking from developer thinking.

---

### Step 1: Understand the job, not the feature

You call Jordan: "Walk me through the conversation — what exactly did the CFO say?"

> "He said he's tired of having to remember to log in every Monday morning and pull the same report before his leadership meeting. He just wants it to show up in his inbox."

JTBD emerging: *When I need to stay on top of weekly performance, I want my report to appear without me having to take an action, so I can focus on the actual meeting prep.*

You ask Jordan: "Has anyone else raised this in other deals?"

Jordan checks and comes back: "Actually yeah — two lost deals in Q2 mentioned this. And I have one renewal coming up where the customer said their exec sponsor is frustrated about the same thing."

**Signal check:** Three deals, one renewal risk. Not a one-off. Time to validate the problem more broadly.

---

### Step 2: Discovery

You email five customers who you know are executive stakeholders, inviting them to a 20-minute call on "how they use Claros to prepare for leadership meetings."

Four of five agree. What you find:

- All four log in manually once a week to pull a specific report
- Two have created a recurring calendar reminder to do it
- One says they've missed it twice because of travel, and it caused embarrassment
- None of them knows a scheduled delivery option could exist — they've just accepted it as how it works

**Customer quote:** *"I assumed all analytics tools worked this way. I'd pay just to not have to remember to do it."*

This confirms the problem is real and understated. Support tickets surface zero complaints because customers don't know to ask. But interview research reveals genuine friction.

---

### Step 3: Scope the opportunity

You look at the data. How many current customers fit this pattern?

SQL query (you write it yourself):
```sql
SELECT user_id, COUNT(*) as weekly_logins
FROM sessions
WHERE day_of_week = 1  -- Monday
  AND hour_of_day BETWEEN 7 AND 10
  AND created_at > CURRENT_DATE - INTERVAL '60 days'
GROUP BY user_id
HAVING COUNT(*) >= 4  -- at least 4 of the past 8 Mondays
```

Result: 67 users across 41 accounts match this pattern. That's ~23% of your customer base doing a consistent weekly manual check.

**Business case formed:**
- Feature cost: ~6 engineer-weeks
- Potential impact: support for a $60K deal, one renewal risk, and potential upsell opportunity across 40+ existing accounts

You take this to your VP of Product in your weekly 1:1 and get alignment to prioritize it for Q3.

---

## Month 2: Scoping & Spec

### Step 4: Write the PRD

You draft a PRD. Key decisions:

**Scope — In:**
- Scheduled delivery of any saved report, via email
- Daily / weekly / monthly cadence options
- Multiple recipients per schedule
- Basic email with report attached as PDF

**Scope — Out (and the reasons):**
- Slack integration (valid future request, would double scope)
- Dynamic email body with embedded charts (significant engineering investment for uncertain value)
- Conditional delivery ("only send if revenue is below X") (complex and low signal from research)
- Mobile push notifications (different delivery mechanism entirely)

You review the PRD with engineering. The tech lead, Priya, flags: "PDF generation at scale is actually non-trivial. We'd need a background job system that we don't currently have."

You didn't know this. The 6-week estimate becomes 9 weeks.

**Negotiation:** You and Priya scope a "Phase 1" that uses the existing report export functionality and attaches the file. No new PDF renderer needed. Back to 6 weeks.

**The PRD gets signed off.**

---

### Step 5: Define success metrics before building

You define:

- **Primary:** % of accounts with at least one active schedule within 60 days of launch
- **Secondary:** Weekly login frequency for accounts using scheduled delivery (expect it to decrease — that's good)
- **Counter-metric:** Support tickets mentioning scheduled delivery (watch for edge case failures)
- **Business:** Does the BigCo deal close? Do scheduled delivery mentions appear in other deal notes?

You share these with your manager. They're locked before a line of code is written.

---

## Month 3: Build & Pre-Launch

Engineering builds. You're checking in weekly, not daily. Priya makes an implementation call on retry logic for failed emails — she picks exponential backoff. You don't second-guess it.

You do ask: "What happens if the report errors during generation — what does the user see?" Priya realizes the error state wasn't in the spec. You add it together.

### Step 6: Beta

You enroll 8 customers — including BigCo (still in pilot) and 7 existing accounts who matched the Monday morning usage pattern.

Beta feedback surfaces two things:
1. Users want a "send a test" button before scheduling — they're worried the wrong report will go to their CFO
2. One customer wants to send to 15 recipients. Your UI caps at 5.

You add the test button (small scope). You adjust the cap to 20 (Priya estimates it's 2 hours of work).

BigCo's CFO sends feedback: "This is exactly what I wanted."

The deal closes two weeks later. $60K.

---

## Month 4: Launch & Outcome

### Step 7: Launch

**Tier 2 launch.** You don't need a press release. You do need:
- Email to all customers announcing the feature (your PMM writes it, you review)
- In-app banner with a CTA to set up a schedule
- Sales enablement: Slack message to AEs with a one-paragraph description and the BigCo win story

Launch day goes smoothly. No critical errors. Analytics confirm events are firing correctly.

---

### Step 8: Post-launch measurement

**4 weeks after launch:**

- **Scheduled delivery adoption:** 38% of accounts have at least one active schedule (target was 25%)
- **Monday login frequency:** Down 31% for accounts using scheduled delivery (shows it's replacing the manual check)
- **Support tickets:** 2 tickets about formatting issues (minor, fixed in a patch release)
- **Deal signal:** Jordan mentions 3 prospects have specifically asked for scheduled reports in calls this week — the feature is showing up in sales conversations

**The metric that wasn't measured but should have been:** Renewal health for the 41 accounts you identified as manual-weekly users. You make a note to pull this in next quarter.

---

## What this walkthrough touched

| Concept | Where it appeared |
|---------|------------------|
| JTBD | Month 1 — understanding the job behind the feature request |
| Customer interviews | Month 1 — 4 customer calls |
| Data analysis | Month 1 — SQL query to size the opportunity |
| PRD + scope | Month 2 — writing and reviewing the spec |
| Negotiation | Month 2 — scoping Phase 1 with Priya |
| Success metrics | Month 2 — defined before build |
| Beta / experiment | Month 3 — 8-customer beta |
| Launch tiers | Month 4 — Tier 2 launch decision |
| Post-launch review | Month 4 — 4-week review |
| Stakeholder management | Throughout — Jordan, Priya, VP, BigCo |
| Counter-metrics | Month 2 — support ticket guardrail |

---

## What you'd do differently

- Start the discovery earlier — don't wait for a deal trigger to validate a problem that affects 23% of customers
- Define the renewal impact metric from the start
- Build in-product discovery (tooltip, empty state CTA) alongside the feature so customers find it without waiting for the launch email

---

## Next

For the full 18-month picture — including pricing changes, multi-team builds, a launch crisis, and a product sunset — see [A Full Product Lifecycle](full-product-lifecycle.md).
