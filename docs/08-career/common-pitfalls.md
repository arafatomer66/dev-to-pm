# Common Pitfalls

These are the failure modes of developer-turned-PMs, listed roughly in the order they appear. Most developers hit at least two of these in their first year. Recognizing them early is the defense.

## 1. Owning the solution, not the problem

**What it looks like:** You get a customer complaint, you immediately know how to fix it, you write a spec for the fix, and you put it on the roadmap. You skip the step of verifying that the problem is real, widespread, and worth solving.

**Why developers fall into it:** Problem-to-solution is the developer workflow. You've spent years fixing things. The impulse is strong.

**The consequence:** You ship features that solve the specific symptom instead of the underlying problem. You build a workaround instead of the right thing. You spend engineering time on a 3-user problem instead of a 300-user problem.

**The fix:** Before writing any spec, write a problem statement. Sit with the problem for at least a few days. Talk to more customers. Ask "is this really the problem?" before you ask "how do we solve it?"

---

## 2. Becoming the team's unofficial tech lead

**What it looks like:** You're in sprint ceremonies offering technical opinions. You're reviewing architecture decisions. You're telling engineers how the feature should be built. The engineering team has stopped making decisions without running them by you.

**Why developers fall into it:** You're competent. You see better approaches. The silence when nobody speaks up is uncomfortable.

**The consequence:** You've created a dependency that doesn't scale. The engineering team stops exercising their own judgment. You're spending energy on the wrong problems. And engineering starts to resent you.

**The fix:** In engineering discussions, ask questions instead of proposing answers. "What are the tradeoffs of those two approaches?" instead of "I think we should use approach A." Explicitly defer: "That's an engineering decision — what does the team think?"

---

## 3. Over-specifying implementation

**What it looks like:** Your PRDs include endpoint names, data models, framework preferences, and specific UI patterns because you can.

**Why developers fall into it:** Precision feels responsible. You've been burned by vague requirements.

**The consequence:** Engineering ignores your spec and builds what makes sense technically. Or they follow your spec and build something technically worse because you specified the wrong approach. Either way, trust erodes.

**The fix:** Write requirements in terms of user outcomes, not implementation. If a technical constraint is genuinely a business decision (vendor choice, compliance requirement), document it with the reason. If it's just a preference, leave it out.

---

## 4. Avoiding customer conversations

**What it looks like:** Your discovery process is: look at analytics, read support tickets, talk to the CS team. You haven't had a direct customer conversation in three weeks.

**Why developers fall into it:** Customer conversations are uncomfortable for people with engineering communication styles. There's no right answer, no spec to verify against. It's ambiguous.

**The consequence:** You build products based on second-hand information filtered through CS and support. You miss the "why" that makes features genuinely useful. Your decisions are educated guesses instead of validated bets.

**The fix:** Block two hours per week for customer conversations. Make them non-negotiable in your calendar. Even 3–4 conversations per month is transformative compared to zero.

---

## 5. Feature factory mode

**What it looks like:** You're shipping a lot of features. The team is productive. The roadmap is moving. But the key metrics — retention, NRR, activation — aren't moving.

**Why developers fall into it:** Output feels like progress. A shipped feature is visible evidence of work.

**The consequence:** You have a growing product with diminishing returns. Each new feature adds complexity without adding proportional value. Users are confused. The product is hard to learn.

**The fix:** For every feature, define the metric it will move before building. Do a post-launch review 4–6 weeks after shipping. If the metric didn't move, investigate why before adding more features.

---

## 6. Underselling strategy, overselling delivery

**What it looks like:** Your roadmap reviews are all about what's being built. You're excellent at getting features through to production. But when asked "why are we building this and not that?" you have a weak answer.

**Why developers fall into it:** Delivery is what you were optimized for. Strategy feels soft and unverifiable compared to shipped code.

**The consequence:** You're a high-quality feature writer, not a product leader. Your career stalls because leadership doesn't see you as someone who can own a product direction.

**The fix:** Spend 2–3 hours per week on strategic work: competitive research, customer conversations, market analysis, strategy documents. This is the part of the job that determines your ceiling.

---

## 7. Saying yes to everything

**What it looks like:** Every stakeholder request gets added to the backlog. You negotiate by adding things, not by choosing between them. Your roadmap is a mile long and nothing gets done fast.

**Why developers fall into it:** Saying no is uncomfortable. As an engineer, you built what was asked. The transition to "sometimes no" is a cultural shift.

**The consequence:** Overloaded engineering team, low morale, disappointed stakeholders when everything takes longer than expected.

**The fix:** Every add is a tradeoff. When someone requests something, make the tradeoff explicit: "We can add this. Here's what would need to move out to make room." This shifts the conversation from "will you build it?" to "what are we trading?"

---

## 8. Hiding bad news

**What it looks like:** The metric is down. The launch didn't go as expected. You're behind schedule. You know, but you haven't told leadership because you're working on fixing it first.

**Why developers fall into it:** Developer culture: fix the bug before you close the ticket. Don't report a problem until you have the solution.

**The consequence:** Leadership is surprised. Decisions are made without information they needed. Trust is damaged far more than if you'd shared the problem early.

**The fix:** Develop a "bad news early" discipline. When something is going wrong, communicate the state + what you're doing + what you need + expected timeline. Always, before you've fixed it.

---

## 9. Confusing activity with progress

**What it looks like:** You're in back-to-back meetings. You're responding quickly to Slack. You're busy all day. But at the end of the week, you can't articulate what decision you made or what moved forward.

**Why developers fall into it:** Developers have clear output metrics (commits, PRs, story points). PM output is less visible, and without a discipline of measuring it, "busy" feels like "productive."

**The consequence:** You make no progress on the things that matter. The strategic work, the customer conversations, the discovery — it all gets crowded out by the urgent but less important.

**The fix:** Time-block the PM work that matters: discovery, strategy, writing. Protect it from meetings. At the end of each week, ask "what decision did I make this week that moved the product forward?"

---

## 10. Thinking the role is an upgrade

**What it looks like:** You approach the transition as a promotion — more status, more influence, more pay. You underestimate the skill gap.

**Why developers fall into it:** PM is perceived as "above" engineering in some org structures. Senior engineers sometimes move to PM because they see it as career advancement.

**The consequence:** You're a weak PM and a former strong engineer. You've traded expertise for a role you haven't yet earned.

**The fix:** Approach the transition as a career change into a junior role in a new discipline. Expect to be competent in 12–18 months. Be humble about what you don't know. The engineering background is a foundation, not a free pass.

---

## Next steps

- [Transition Roadmap](transition-roadmap.md) — the phased plan that avoids these pitfalls
- [Self-Assessment](self-assessment.md) — where you stand
- [Interview Prep](interview-prep.md) — when you're ready
