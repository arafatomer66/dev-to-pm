# User Research

User research is how you close the gap between what you assume about your users and what is actually true. As a developer, you've been building software based on specs — the "user" was often abstract. As a PM, talking to real users is the job.

## The interview > the survey

Surveys are tempting because they scale. You can get 500 responses in a day with no scheduling overhead.

The problem: surveys tell you what people say they want, which is often different from what they actually need, do, or would pay for. "Would you use X feature?" responses are optimistic and unreliable. Human behavior in real situations is the truth; survey responses are aspirational fictions.

Interviews are harder to scale but incomparably richer. One honest interview with a real customer often contains more signal than 200 survey responses.

Use surveys for: quantifying something you already understand qualitatively (e.g., after interviews reveal a pain point, a survey measures its prevalence).

Use interviews for: understanding problems, behaviors, decision-making, and context.

## Recruiting interview participants

The most common failure is talking to the same five friendly power users every month. They're convenient and they like you — but they're not representative.

**Who to talk to:**

| Segment | Why |
|---------|-----|
| Active power users | What's working; what could be better |
| New users (0–30 days) | Activation friction; first impressions |
| Churned users | What broke; what alternatives they chose |
| Non-users who tried but didn't adopt | Where you're losing before they even start |
| Prospects who chose a competitor | Real competitive differentiation |
| Prospects in your target ICP who aren't customers yet | Unsolved problems; discovery for new segments |

**How to recruit:**
- Email from CS or your account team (warm, high response rate)
- In-product intercept (survey asking if they'd take a 20-min call)
- User community or Slack (if you have one)
- LinkedIn + user research panel services (Respondent.io, User Interviews) for non-customers
- Customer calls — ask "who else should I talk to?" at the end of every interview

## Running the interview

### Preparation
- Write a discussion guide (not a rigid script)
- Define 2–3 learning objectives: "I want to understand how they currently handle X"
- Block time for notes immediately after

### Interview structure

**Opening (5 min)**
> "Thanks for taking the time. I want to understand your experience with [problem area] — not pitch you anything. There are no right or wrong answers. It's more valuable if you tell me something negative than if you say what you think I want to hear."

Set this expectation explicitly. Interviewees default to being polite.

**Context setting (10 min)**
> "Can you tell me about your role and how [problem area] fits into your day-to-day work?"

Understand their world before asking about the product.

**Current behavior (15 min)**
> "Walk me through the last time you had to [do the thing you're researching]."

This is the most valuable part. Specific past behavior is more honest than hypothetical future behavior. "What did you actually do last Tuesday?" beats "What would you do if we built X?"

**Specific problems (10 min)**
Dig into the pain points that surfaced in the behavior walkthrough.
> "You mentioned X was frustrating — can you tell me more about that?"

**Alternatives and workarounds (5 min)**
> "What do you use today to solve this? What don't you like about it?"

**Closing (5 min)**
> "Is there anything about this problem space I didn't ask about that you think is important?"

Often the most interesting things come out here.

### What not to do

**Don't ask "would you use X?" questions.** The answer is almost always yes, which tells you nothing.

**Don't describe your solution.** You're doing discovery, not validation. If you describe the feature, you'll get feedback on your feature rather than insight into their problem.

**Don't lead the witness.** "Don't you find it frustrating when...?" is a leading question. "How does that make you feel?" is neutral.

**Don't interrupt silence.** Pause after their answer. Count to three. Often the most honest and interesting answer comes in the silence after they've finished their initial response.

## Synthesis

Interviews without synthesis are wasted time. Synthesis converts raw notes into insights.

**Basic synthesis process:**

1. Immediately after each interview, write 3–5 "I noticed that..." statements
2. Weekly, review all interview notes from that week and tag themes
3. Monthly, look for patterns across themes: what's appearing repeatedly?

**Affinity mapping (for groups):**
Write each observation on a sticky note (physical or digital). Cluster similar observations. Name each cluster. Discuss the clusters as a team.

**Jobs-to-be-Done synthesis:**
Convert behavioral observations into "when [situation], I want to [motivation], so I can [expected outcome]" statements. These become your design requirements.

## Avoiding confirmation bias

Confirmation bias is the enemy of good research. You'll go into interviews with a hypothesis about what to build. Your brain will selectively attend to evidence that confirms it.

**Countermeasures:**
- Write your hypothesis down before the interview, so you notice when you're seeking to confirm it
- Have a second person on each interview — they'll catch things you miss
- Actively look for disconfirming evidence: "What would make this worse?" or "What would make you stop using this?"
- At synthesis time, give extra weight to evidence that surprised you

## Qual vs. quant

| Qualitative research | Quantitative research |
|---|---|
| Why something happens | What/how much/how often something happens |
| Rich context and nuance | Statistical reliability at scale |
| Small samples (5–15 usually enough) | Large samples (hundreds to thousands) |
| Interviews, diary studies, usability tests | Analytics, surveys, A/B tests |
| Best early in discovery | Best later in validation |

The mistake is using one when you need the other. Analytics can tell you that 40% of users drop off at Step 3. Interviews tell you why. You need both.

## When you have limited research budget

Start with existing data:
- Support tickets and feature requests (already categorized customer pain)
- NPS verbatims (the open-text responses are often the most useful part)
- Churn survey responses
- Sales call recordings

This won't replace primary research, but it's often good enough to formulate hypotheses before you invest time in interviews.

## Next steps

- [Personas & Jobs-to-be-Done](personas-and-jtbd.md) — turning research insights into design inputs
- [Discovery & Validation](discovery-and-validation.md) — the broader discovery practice
- [User Research Guide template](../10-templates/user-research-guide.md)
