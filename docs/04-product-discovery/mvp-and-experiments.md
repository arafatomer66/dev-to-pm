# MVPs & Experiments

An MVP is not a bad version of your product. It's the minimum experiment needed to test the most important assumption before committing to full development. Most "MVPs" built by developer-turned-PMs are actually full products with a few features cut. That's not an MVP — it's just a smaller scope.

## What an MVP actually is

Eric Ries's definition: "The version of a new product which allows a team to collect the maximum amount of validated learning about customers with the least effort."

The key words: *validated learning* and *least effort*. An MVP is a learning vehicle, not a product. Its purpose is to answer a specific question as cheaply as possible.

This means an MVP might not be software at all. A landing page, a sales pitch, a concierge service, or a wizard-of-oz demo can all be MVPs if they test the assumption you need to validate.

## The experiment mindset

Every feature decision is a hypothesis. Make it explicit:

```
Hypothesis: We believe that [solution]
will achieve [outcome] for [user segment]
because [reason].

We'll know we're right when [metric] moves by [amount]
within [timeframe].

We'll know we're wrong when [counter-signal].
```

Writing this down before building forces two disciplines:
1. You define success before you can see the outcome (prevents retroactive success definition)
2. You make your reasoning visible, so others can challenge it

## The experiment ladder

Not every idea needs the same level of investment to test. Match the experiment type to the assumption risk:

```
Cheapest ←────────────────────────────────────→ Most Expensive

Conversation  →  Fake door  →  Prototype  →  Wizard of Oz  →  Concierge  →  Real build
(1 day)          (1 week)      (1-2 weeks)   (2-4 weeks)      (1 month)     (months)
```

**Conversation:** Does the problem resonate? A 30-minute interview.

**Fake door / Painted door:** Put a button or link for a feature that doesn't exist yet. If users click on it, you've measured demand. Show "coming soon" and capture email.

**Prototype:** A clickable mockup (Figma, Marvel). Tests UX and concept, not functionality. Can be built in days.

**Wizard of Oz:** The user thinks they're using a real product; behind the scenes, humans are manually doing what the software would do. Tests whether the value is real without building the system.

**Concierge MVP:** Manually deliver the service yourself to a small number of customers. They know it's manual; they're paying for the value, not the product.

**Real build:** The actual software. Most expensive. Should only happen after earlier experiments have de-risked the core assumptions.

## A/B testing without self-deception

A/B testing is useful and frequently abused. Common pitfalls:

**Running tests too short.** Statistical significance takes time. Stopping a test early because it "looks good" or "looks bad" is a classic mistake. Calculate your required sample size before starting and don't touch it until you've hit it.

**Testing too many things at once.** If you change the button color, the headline, and the layout in one test, you can't know which change caused the result.

**Optimizing the wrong metric.** A/B tests on click-through rate that ignore downstream conversion or retention are optimizing a proxy, not the outcome that matters.

**The novelty effect.** Users click on new things because they're new. A spike in engagement after a feature launch may be novelty, not value. Wait 2–4 weeks before concluding anything.

**Interpreting "no significant difference" as failure.** A null result is information. If you hypothesized a 15% lift and got 0%, your hypothesis was wrong. That's valuable.

## Pivot, persevere, or kill

After running an experiment, you face three options:

**Persevere:** The experiment validated the hypothesis. Continue building in this direction.

**Pivot:** The experiment revealed something unexpected. The core insight is valid, but the approach needs to change. Build a new hypothesis.

**Kill:** The experiment invalidated the hypothesis. The problem isn't as real, the solution doesn't work, or the market doesn't exist. Stop.

"Kill" is the hardest outcome to accept, especially when you've already invested time in the idea. The sunk cost fallacy is powerful. The discipline to kill a validated dead end is what separates systematic product development from the build trap.

## MVPs for B2B products

Consumer MVPs often involve broad user panels and A/B tests. B2B MVPs look different:

**Design partner:** Sign up 2–5 customers to use a feature in beta. They get early access; you get feedback and a lighthouse reference. The commitment from both sides is light.

**Sales POC:** Include a new feature in a sales proof-of-concept with a willing prospect. If they'll sign based on it, you've validated demand. If they won't, you've saved engineering time.

**Manual delivery:** Promise the outcome to a customer, deliver it manually, and measure whether they actually value it. If they complain when you automate it (because the quality drops), you've learned something.

## The failure PM most common MVP failure

The MVP gets launched, shows some positive signal, and then gets declared "shipped" — no follow-up measurement, no iteration, no "did this actually move the metric?"

An MVP is not done when it ships. It's done when you've answered the question it was designed to answer.

Build a post-MVP review into your process: 4–6 weeks after launch, review the hypothesis, check the metrics, and make a deliberate decision: build out further, iterate, or redirect.

## Next steps

- [Discovery & Validation](discovery-and-validation.md) — the continuous practice that feeds experiment design
- [Metrics & Analytics](metrics-and-analytics.md) — measuring experiment outcomes
- [Experiment Canvas template](../10-templates/experiment-canvas.md)
