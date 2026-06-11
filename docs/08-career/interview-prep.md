# Interview Prep

PM interviews test different skills than engineering interviews. There's no LeetCode equivalent. Instead, you'll be assessed on product thinking, communication, business judgment, and behavioral patterns. This page covers what to expect and how to prepare.

## The PM interview loop

A typical PM interview loop (4–6 rounds) includes:

| Round | What it tests |
|-------|--------------|
| Recruiter screen | Basic fit, compensation, timeline |
| Product sense / design exercise | How you think about product problems |
| Analytical / metrics round | How you use data; how you think about metrics |
| Strategy / vision | How you think about market, competition, product direction |
| Behavioral (STAR) | Past experience, how you handle specific situations |
| Cross-functional (with design, eng, or sales) | How you'd actually work with these teams |

At smaller companies, some rounds combine. At FAANG, there may be more and they're more rigorous.

## Product sense questions

These test your product instinct — how you think about design, user experience, and product decisions.

**Common formats:**
- "Design a [product/feature] for [user/context]"
- "How would you improve [known product]?"
- "Your PM calls you and says [metric] dropped 20% overnight — what do you do?"

**Framework for design questions:**

1. **Clarify the goal** — "What is the product trying to achieve?" Don't accept an ambiguous prompt at face value.
2. **Define the user** — Name a specific persona or segment. "Users" is too vague.
3. **Identify the user's goal** — What job are they trying to do?
4. **Propose solutions** — Typically 2–3 options.
5. **Evaluate tradeoffs** — Pick one and explain why.
6. **Define success** — What metric would you track?

**For metric diagnostic questions** (the "metric dropped 20%" type):

1. **Verify the data** — Is this a real drop or a measurement artifact? Data pipeline issue?
2. **Segment the drop** — Is this across all users or specific segments? Geographic? Platform?
3. **Correlate with changes** — Did we ship something? Did a marketing campaign launch? External event?
4. **Form hypotheses** — 3–4 possible root causes, ranked by likelihood
5. **Propose investigation steps** — How would you validate each hypothesis?

## Analytical questions

These test your metrics fluency and how you'd use data to make product decisions.

**Common formats:**
- "What metrics would you track for [product/feature]?"
- "How would you measure success for [feature launch]?"
- "Design an A/B test to validate [hypothesis]"

**Preparation:** Know the AARRR framework, understand the difference between leading and lagging indicators, and be able to define a North Star metric and input metrics for 2–3 products you know well.

## Strategy questions

These test whether you can think about the full competitive and business picture.

**Common formats:**
- "What would you build next for [product]?"
- "How would you enter [new market/segment]?"
- "What is [company]'s biggest product risk?"

**How to answer:** Use a structured approach — understand the market, the competition, the user, and the business model before recommending a direction. Show that your recommendation connects to strategy, not just product taste.

## Behavioral questions

PM behavioral questions follow the STAR format: Situation, Task, Action, Result.

**Must-have stories prepared:**

| Scenario | Story structure |
|----------|----------------|
| Made a decision with incomplete data | Situation + how you decided + what happened + what you learned |
| Influenced someone without authority | Who, how, what the outcome was |
| Said no to a stakeholder | What was requested, why you said no, how the relationship survived |
| Product failed or missed a goal | What happened, your contribution, what you'd do differently |
| Cross-functional conflict | What the conflict was, how you resolved it, what changed |
| Shipped something you were proud of | The full story from problem to outcome |

**The developer-to-PM story:** You will be asked "why do you want to leave engineering?" Have a positive, forward-looking answer about what you want to do in PM — not "I hated code reviews" or "I want more influence." Something like: "I've found I'm most energized when I'm thinking about what problem to solve and for whom. I want to spend more time in that problem space."

## Turning "ex-developer" into an unfair advantage

Many interviewers see your engineering background as a positive in PM interviews. Use it:

- **Feasibility instinct:** "As an engineer, I've seen specs like this come in and the first question would be... My instinct is the complexity is actually in [X], not [Y]."
- **Credibility with technical teams:** "I've been on the receiving end of unclear requirements, so I write specs with [specific practices] in mind."
- **Data comfort:** "I can pull my own queries, which means I'm not waiting on a data analyst for every product question."
- **Build trap awareness:** "I've shipped features that nobody used — I know what that feels like, and I'm deliberate about discovery before committing to build."

These are genuine differentiators. Use them, but don't lean on them so hard that you seem like you're still an engineer who "just wants to give directions."

## The take-home exercise

Many PM interviews include a take-home exercise — typically a mock PRD, a product strategy memo, or a case analysis.

**What makes a great take-home:**
- Clear, structured writing — no fluff, BLUF format
- A sharp problem statement that shows you understand the root cause
- Success metrics defined up front
- Explicit scope (in and out of scope)
- Evidence of product thinking — not just feature listing

**What hurts take-home submissions:**
- Too long (aim for the reader finishing in 15–20 min)
- No clear recommendation — presenting options without committing to one
- Vague success metrics ("improve user satisfaction")
- Implementation details instead of product thinking
- Typos and formatting errors (signals you don't care about communication quality)

## Questions to ask interviewers

Asking good questions signals product thinking:

- "What does a successful first year in this role look like?"
- "What's the most significant strategic challenge the product is facing right now?"
- "How does this team make prioritization decisions when there's stakeholder disagreement?"
- "What do you wish you'd known before joining in a PM role?"

Avoid: "What's the culture like?" (too generic) and "What's the roadmap?" (puts them in a sensitive spot).

## Next steps

- [Self-Assessment](self-assessment.md) — before preparing for interviews
- [Transition Roadmap](transition-roadmap.md) — the path to getting interview-ready
- [PRD template](../10-templates/prd.md) — practice ground for take-home exercises
