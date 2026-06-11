# Platform Products

Platform PM is a distinct specialty. If you're building developer tools, APIs, internal platforms, or anything where your "customers" are other builders, the PM job looks different in important ways.

## What makes a platform different

A platform is a product designed to be built on top of. Its value comes not just from what it does directly, but from what it enables others to build.

**Characteristics:**
- Your customer is often a developer or technical team
- The product's value is partly in the ecosystem it enables
- API design decisions are product decisions with long-term consequences
- "Backward compatibility" becomes a first-class product concern
- Developer experience (DX) matters as much as UX

**Examples:** AWS, Stripe, Twilio, Salesforce AppExchange, Slack API, a company's internal data platform.

## The platform vs. feature decision

One of the most important strategic decisions in a growing product: when does a capability become a platform?

**Build as a feature when:**
- The use case is well-defined and consistent across users
- Deep integration into the product experience is the value
- No external developers would benefit from accessing it independently

**Build as a platform when:**
- Different users want to customize or extend the behavior
- External developers would build things on top that you haven't thought of
- The ecosystem of use cases is broader than you can serve directly

Platform decisions compound over time. A well-designed platform creates a moat (ecosystem lock-in, developer community). A poorly designed platform creates permanent technical debt (you can't change it without breaking users).

## API as product

If you own an API, you own a product. The API is the user interface. Its design affects:
- How easy it is to integrate your platform
- How many mistakes developers make (which become your support load)
- How your product evolves (everything built on the API creates backward-compatibility constraints)

**PM's responsibilities for APIs:**
- Define the developer experience goals (what should be easy? what's acceptable to be hard?)
- Own the API design review alongside engineering (naming conventions, consistency, error messages)
- Define the versioning and deprecation strategy before shipping v1
- Monitor API usage to understand how developers are actually using it

**The most important API principle:** Don't ship an API you're not prepared to maintain. Every endpoint you publish is a commitment.

## Developer experience (DX)

DX is to developer tools what UX is to consumer products. It includes:

- **Time to first success:** How long from sign-up to the first working integration?
- **Documentation quality:** Can a developer figure out what to do without a support ticket?
- **Error messages:** Do they tell developers what to fix or just report a status code?
- **SDK quality:** Is the client library idiomatic in the developer's language?
- **Sandbox/test mode:** Can developers safely test without affecting production?

Stripe is the DX benchmark. Study their documentation and onboarding flow as a PM studying their craft.

## Internal platforms

If you're a PM for an internal developer platform (build tooling, data infrastructure, CI/CD, observability), you have a different context:

**Your customers are engineers.** This means:
- Your "sales" motion is adoption by internal teams
- Churn means teams building alternative solutions or working around you
- Product feedback often comes in the form of PRs, GitHub issues, and Slack complaints

**The unique challenge:** Internal platform customers didn't choose you. They're using you because the company decided on a standard platform. This creates a customer relationship dynamic unlike external products — you can't lose them to a competitor, but you can lose their engagement and respect.

**What makes internal platforms succeed:**
- Teams feel the platform is built for their needs, not mandated on them
- The platform's constraints (what it forces you to do) are understandable and justified
- Feedback loops are fast — teams feel heard when they report issues
- The platform team dogfoods its own platform

## Ecosystem thinking

Platform PMs think about the ecosystem that forms around their product:

- **Developers who build on it:** What's their experience? What do they need to succeed?
- **End users of apps built on it:** The quality of your ecosystem reflects on your platform
- **Partners:** Who has built official integrations? What do those relationships require?
- **Competitors building on your platform:** A complex situation that requires explicit policy

Platform strategy means occasionally making decisions that benefit the ecosystem rather than the immediate product. Example: investing in developer documentation that helps third-party builders create better integrations — not a direct product feature, but a strategic investment in the platform's long-term value.

## The platform PM's unique challenges

**Deprecation:** When you need to remove or change an API endpoint that developers depend on, you're affecting their production systems. The process: announce deprecation, provide a migration path, give adequate time (6–12 months for external APIs), then sunset.

**Backward compatibility:** Every external API you ship, you maintain. The design of v1 constrains v2. This is why "move fast and break things" doesn't apply to platform products in the same way it applies to product features.

**Adoption vs. standardization:** Internal platforms face the tension between "let teams do what works for them" and "standardize so the organization benefits from consistency." PM's job: find the right balance, and be explicit about the decision rather than letting it drift.

## Next steps

- [B2B Products](b2b-products.md) — where platform meets enterprise
- [Business Models](../07-business-skills/business-models.md) — platform business model specifics
- [Working with Engineers](../06-working-with-teams/working-with-engineers.md) — the primary stakeholder for platform PMs
