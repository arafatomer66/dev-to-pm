# Working with Design

The product triad — PM, design, and engineering — is the atomic unit of product development at most tech companies. How well the triad functions determines the quality of the product more than any individual's skill. PM-design is the axis most likely to have friction, because both roles have opinions about what the product should be.

## What designers actually do

Developers often think design is about making things look nice. That's the smallest part.

Good product designers do:
- **User research:** Understanding user mental models, testing concepts, synthesizing interviews
- **Interaction design:** How the product behaves, not just how it looks
- **Information architecture:** How content and features are organized
- **System design:** Creating design systems that scale consistency across a product
- **Prototyping:** Communicating ideas and testing them before engineering builds
- **Visual design:** The aesthetics — yes, this too

A designer who is only doing visual polish is being underutilized. The PMs who get the most from their design partners treat them as research partners, not pixel pushers.

## The design runway

Engineering typically runs 1–2 sprints behind design. This is intentional — design needs time to explore, iterate, and validate before engineering builds.

The "design runway" is the buffer of designed and validated work ahead of engineering. When the runway collapses, engineers are waiting on designs or (worse) making design decisions themselves.

**PM's role:** Protect the design runway by keeping designers focused on the upcoming sprint work, not current-sprint support. Constant interruptions for small changes to in-flight work kill the runway.

## Giving feedback on design

Feedback is the most common friction point in the PM-design relationship. PMs who give bad feedback:
- **Direct the solution:** "Make the button bigger" instead of "I'm worried users won't see the action here"
- **Use subjective taste:** "I don't like this" without a design principle or user need behind it
- **Pile on late:** Major directional feedback after significant design work is done
- **Give feedback in public without pre-alignment:** Surprising a designer with concerns in front of stakeholders

PMs who give good feedback:
- **Stay in the problem space:** "The goal is for users to quickly see their options — I'm not sure this layout achieves that. What do you think?"
- **Ask questions before giving opinions:** "What were you trying to solve for with this approach?"
- **Front-load the important feedback:** Directional concerns at the concept stage; detail concerns later
- **Differentiate functional requirements from preferences:** "This needs to be accessible" is a requirement. "I'd prefer a cleaner look" is a preference. Separate them.

## When to push back on design

There are legitimate PM reasons to push back on design decisions:

- **Usability concerns:** If testing or research suggests users will struggle
- **Technical constraints:** If the design requires backend changes that weren't scoped
- **Scope concerns:** If the design scope has grown beyond what was planned
- **Accessibility:** If the design doesn't meet accessibility requirements

There are illegitimate reasons:
- **Personal taste:** "I don't like the color"
- **Imaginary user preferences:** "Users will prefer it this way" without evidence
- **Implementation familiarity:** "That's not how it works now" (that's engineering's concern, not yours)

The test: can you connect the concern to a user need, a business requirement, or a technical constraint? If yes, it's a legitimate PM concern. If it's preference, express it as a preference — "I'd personally like to see it look more X, but I'm not sure that's important" — and let the designer decide.

## Design debt

Just like technical debt, there is design debt: accumulated inconsistencies, outdated patterns, and patches that degrade the user experience over time. PMs often don't budget for design debt reduction because it doesn't produce a visible new feature.

A sustainable approach: allocate 10–15% of design capacity per quarter to design system work and cleanup. This is an investment in future velocity — a well-maintained design system makes new features faster and more consistent.

## The design handoff

When design is "done" and being handed to engineering, the handoff should include:
- Annotated specs (not just visual comps) with interaction details
- Edge cases documented (empty states, error states, loading states)
- Component specs linked to the design system
- Design system tokens used (not custom CSS values)

PMs should ensure edge cases are covered before engineering picks up the work. "What happens when the list is empty?" and "What do we show during loading?" are PM questions, not engineering surprises.

## Next steps

- [Working with Engineers](working-with-engineers.md) — the other triad relationship
- [Discovery & Validation](../04-product-discovery/discovery-and-validation.md) — where design research plugs in
