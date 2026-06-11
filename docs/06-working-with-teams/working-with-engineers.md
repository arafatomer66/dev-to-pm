# Working with Engineers

This is the relationship that developer-turned-PMs think they have an advantage in. Sometimes they do. Sometimes the transition creates new friction because your former peers don't see you the way they did when you were one of them.

## The power shift

When you were an engineer, you had authority over your code. When you become a PM, you have accountability for outcomes but no authority over engineering decisions. This is a fundamental change that most developer-turned-PMs underestimate.

Your instincts will tell you:
- "I know how this should be built"
- "That estimate seems too high"
- "We should use [technology X] here"

These instincts are not gone because you're now a PM. But acting on them as if you're the tech lead will undermine the team's autonomy, damage trust, and make you a bad PM.

**The rule:** You own the problem and the success metrics. Engineering owns the solution and the implementation. This is the boundary. Cross it sparingly and explicitly.

## What ex-developer PMs get right

**Technical credibility:** You understand feasibility. You can have real conversations about tradeoffs without the engineer having to explain what an API is.

**Spec quality:** You've been on the receiving end of bad requirements. You write clearer, more precise specs.

**Pushback literacy:** You can tell when "that's complicated" means "genuinely hard" vs. "I'd prefer not to." You can ask "what's the hardest part?" and understand the answer.

**Debugging instinct:** When a metric moves unexpectedly, you think about root cause, not just the symptom.

## What ex-developer PMs get wrong

**Micromanaging implementation:** The most common failure. You see the code, see a better approach, and can't help yourself. Resist.

**Undermining the tech lead:** Expressing opinions on architecture in sprint ceremonies, contradicting the tech lead in front of the team.

**Lowball estimates:** "This should only take two days" from a PM who used to code is demoralizing. You no longer have the context to estimate. Trust the team.

**Reliving the "good old days":** Telling engineers what you'd do if you were coding. This signals that you think PM is less important than engineering. It's dismissive and counterproductive.

## Writing requirements engineers will actually read

Requirements that get ignored are usually:
- Too vague ("make it user-friendly")
- Too prescriptive ("use a red #FF0000 button with 8px border radius")
- Missing context (no explanation of why, just what)
- Missing success criteria (no way to know when done means done)

Requirements that work:
- Name the user and the scenario
- Describe the desired outcome (what changes for the user)
- Include the constraints that are real (performance targets, security requirements, browser support)
- Explicitly list what's out of scope
- Link to supporting context (customer quotes, research notes, design files)

## Handling "that will take 3 months"

This estimate will happen. Reactions that don't work:
- "Can you do it faster?" (pressure, not problem-solving)
- "That seems too long" (undermining without information)
- "Fine, we'll just scope it down" (unilateral without conversation)

Reactions that do work:
- "Help me understand what makes this 3 months — what's the hardest part?"
- "What would a 4-week version of this look like? What would we drop?"
- "What's the biggest unknown that makes this uncertain?"

This surfaces information. Often the 3-month estimate has a specific driver (a technical constraint, an unknown dependency, a legacy system quirk) that can be addressed. Sometimes it reveals that you've over-specified the solution. Sometimes 3 months is genuinely right and you need to adjust the roadmap.

## Protecting the team

One of the PM's most important jobs is saying no to requests from outside the team that would derail the work in progress.

You are the shield between the engineering team and:
- The executive who wants to add something to "this sprint"
- The sales rep who needs a demo environment fixed immediately
- The CEO's "quick idea"

This doesn't mean all outside requests are wrong. Some are legitimate and should be addressed. But it means the PM evaluates them, makes a tradeoff decision, and communicates clearly — rather than all outside requests landing directly on engineers as random interruptions.

## PM-ing your former peers

If you transition into PM from within the same engineering team, you have a specific challenge: your peers now need to see you in a different role.

Practical things that help:
- Be explicit with your manager and team lead about the transition and your new responsibilities
- Stop attending engineering standups and technical planning meetings as a participant — attend as a PM (a very different posture)
- Avoid opinions on implementation unless directly asked
- In your first 30 days, listen more than you direct — let the team see you in the new role before forming opinions

The transition takes time. Some colleagues will adapt quickly; others will still see you as "the developer who moved over." Keep behaving like a PM and the perception will follow.

## Next steps

- [Writing PRDs](../02-core-skills/writing-prds.md) — the artifact that most defines the PM-engineering interface
- [Negotiation](../02-core-skills/negotiation.md) — scope conversations done well
- [Working with Design](working-with-design.md) — the other half of the product triad
