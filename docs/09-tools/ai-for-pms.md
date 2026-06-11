# AI for PMs

AI changes the PM job in two ways: it's a tool that makes some PM work faster, and increasingly, it's the product you're building. Both matter.

## AI as a PM tool

### Where AI is genuinely useful

**First drafts.** PRDs, product briefs, status updates, launch emails — AI can produce a credible v0.1 in minutes. You still need to edit heavily, add specific context, and make it accurate. But starting from something is faster than starting from nothing.

**Interview transcript synthesis.** Paste 10 interview transcripts into a model and ask it to identify common themes. It'll catch patterns you'd miss, and it compresses hours of synthesis into minutes. Verify its output — it sometimes over-generalizes — but it's a strong starting point.

**Research acceleration.** "Give me an overview of the competitive landscape for mid-market HR software" gets you a reasonable starting point for a competitive analysis. Follow up with primary research — AI's training data is not always current or accurate on specific product capabilities.

**Brainstorming.** AI is an excellent brainstorming partner for JTBD statements, persona development, positioning options, and potential solution approaches. It doesn't replace judgment, but it generates ideas at speed.

**SQL assistance.** If you're not fluent in SQL, describe the query you need in plain English and iterate. Verify the query output makes sense before using it.

**Communication.** "Help me write a professional but direct email declining this feature request while offering an alternative" is a genuinely useful AI task.

### Where AI is unreliable

**Company-specific context.** AI doesn't know your users, your product, your competitive situation, or your company's strategic constraints. Any AI-generated content about your specific context is invented and should be removed or replaced.

**Current market data.** Pricing, feature lists, and competitive positioning change constantly. AI training data lags reality by months or years. Don't rely on AI for specific competitor capabilities.

**Statistical analysis.** AI can help set up analysis, but it makes errors in quantitative reasoning. Verify any numbers it produces.

**Strategic judgment.** AI can help you think through a decision but cannot replace your judgment about what's right for your specific company, market, and users.

## Being the PM of AI features

Increasingly, PMs own products that include AI/ML capabilities. This requires a different kind of product thinking.

### Defining success for AI features

Classic software features succeed or fail based on whether they work correctly. AI features exist on a distribution — they're sometimes right, sometimes wrong, and the frequency matters.

Define success differently:
- **Accuracy rate:** What % of AI outputs are correct? At what threshold is the feature valuable?
- **Confidence calibration:** Does the model's expressed confidence match its actual accuracy?
- **Failure mode definition:** When the AI is wrong, how wrong is it? A wrong autocomplete suggestion is annoying; a wrong medical diagnosis is dangerous.
- **User recourse:** When the AI is wrong, can users easily identify and correct it?

### Evals (evaluations)

Evals are the PM's answer to "how do we know the AI feature is working?" An eval is a test suite for model behavior:

- A set of inputs and expected outputs
- Measurement of how often the model produces acceptable outputs
- Comparison across model versions or configurations

PMs who build AI features need to own the eval framework — not implement the technical infrastructure, but define what "correct" means and ensure the team is measuring it. This is the AI equivalent of writing acceptance criteria.

### The cost dimension

AI inference has a per-call cost that traditional software doesn't have. A feature that runs a large language model on every keystroke may be technically impressive and economically catastrophic.

As the PM, you own the feature's unit economics. Before building an AI feature, understand:
- What's the per-call cost?
- How many calls per user per day?
- What's the monthly infrastructure cost at current and projected scale?
- What's the gross margin impact?

This is not an engineering question — it's a product strategy question.

### The "prompt engineering is product" insight

For AI products built on large language models, the system prompt and prompt structure are as important as any UI decision. A poorly designed prompt produces bad outputs that damage user trust. A well-designed prompt produces outputs that feel magical.

PMs should be involved in prompt design at a requirements level: what should the AI produce? Under what conditions? What should it not do? What's the failure behavior?

### AI product failure modes

**Overconfident outputs:** AI presents uncertain outputs as certain. Users trust wrong answers.

**Off-policy behavior:** The AI does things it shouldn't (refuses legitimate requests, makes up information, behaves differently with different user groups).

**Regression without notice:** Model upgrades change behavior. Users experience unexplained changes.

**Hallucination:** The AI generates plausible-sounding but incorrect information. Dangerous in contexts where accuracy matters (medical, legal, financial).

**Privacy leakage:** User data in prompts may be used in ways users didn't expect. Understand your model provider's data policies.

For each of these, a PM's job is to define the acceptable threshold and build the monitoring to know when the threshold is crossed.

## Next steps

- [PM Tooling Landscape](pm-tooling-landscape.md) — where AI tools fit in the broader toolkit
- [MVPs & Experiments](../04-product-discovery/mvp-and-experiments.md) — how to run experiments on AI features
- [Data-Driven Decisions](../02-core-skills/data-driven-decisions.md) — measuring AI feature performance
