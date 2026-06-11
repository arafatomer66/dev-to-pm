# B2B Products

B2B product management has distinct challenges that consumer PM experience doesn't prepare you for. If your background is in developer tools, enterprise software, or any product sold to businesses, this page covers the specific dynamics you'll navigate.

## Buyer ≠ User

In B2B, the person who decides to buy your product is often not the person who uses it every day.

**The buyer:** VP, Director, or C-level. Evaluates business outcomes: ROI, risk reduction, competitive advantage. Doesn't care about the UI in detail.

**The user:** Individual contributor or team lead. Evaluates day-to-day usability: does this save time, does it reduce friction, can I do my job better?

**The champion:** Often a power user who advocated for purchasing your product internally. They have organizational credibility and want your product to succeed.

**The economic buyer:** The person who controls budget. May have no opinion on features but decides whether to renew.

Your product must serve all of these people simultaneously — but they have different needs and different levers:
- If users hate the product, they'll lobby the buyer to switch
- If buyers don't see ROI, they won't renew regardless of user satisfaction
- If champions lose credibility, your renewal becomes a fight

This is the most important strategic difference between B2B and consumer PM.

## Long sales cycles

Enterprise sales cycles can run 6–18 months. This has product implications:

**Features needed for evaluation:** Prospects evaluate your product against alternatives. Features that matter during evaluation (demos, POC capabilities, security certifications) are different from features that matter in daily use.

**The POC (proof of concept):** Many enterprise deals require a POC — a limited engagement where the prospect tests your product against their real requirements. PM responsibility: understand what POC criteria look like and ensure the product can demonstrate value in constrained conditions.

**References:** Enterprise buyers want to talk to similar customers. Your product's ability to serve a specific vertical well enough to generate reference customers matters more than broad horizontal capabilities.

## Customization pressure

Enterprise customers will ask you to customize the product for their specific needs. This pressure is constant and dangerous if not managed carefully.

**The trap:** You build custom features for large deals. The features are specific to one customer. The next customer needs something different. You end up with a product that's partially generalized and partially a spaghetti of one-off customizations. The codebase becomes a nightmare. Every new deal creates technical debt.

**The discipline:**
- Evaluate every customization request through the lens: "Would 5+ other customers benefit from this?"
- If yes: build it as a general capability
- If no: push it to professional services, don't include it in the core product
- If the deal requires the customization: negotiate a professional services contract

The PM who can't say no to customization requests becomes a feature factory for enterprise deals.

## Configuration vs. customization

A useful distinction:
- **Configuration:** The customer sets a parameter (timezone, currency, admin permissions). The product supports it natively. No engineering work per customer.
- **Customization:** Engineering builds something for one customer. Every customization is technical debt.

Design your product for configuration, not customization. When enterprise customers ask for something "custom," explore whether it could be solved with configurable options.

## Enterprise features: the table stakes

Certain features are required to even be evaluated by enterprise buyers:

| Feature | Why it matters |
|---------|---------------|
| **SSO (SAML/OIDC)** | IT won't allow an app that doesn't integrate with their identity provider |
| **Audit logs** | Security and compliance teams need to know who did what |
| **Role-based access control (RBAC)** | Different users need different permissions |
| **Data export** | Legal and data governance require the ability to retrieve data |
| **SLA and uptime commitment** | Enterprise contracts include SLA terms |
| **SOC 2 Type II (or equivalent)** | Security audit certification that IT requires |

You can't sell to serious enterprise buyers without most of these. If they're not on your roadmap, they should be before you pursue enterprise deals aggressively.

## Customer success at B2B scale

B2B products need a Customer Success function. CS teams do:
- Onboarding for new accounts
- Ongoing relationship management for key accounts
- Renewal conversations
- Escalation management when things go wrong

**PM-CS relationship:** CS is your most important source of customer insight at scale. They're in the product daily with customers. Build a strong working relationship:
- Weekly PM-CS sync to surface emerging patterns
- Joint customer calls where both PM and CS participate
- CS as a first-pass filter for feature requests (they can tell you which requests are widespread vs. one-off)

## Working with enterprise champions

Your enterprise champions are customers who invested personal credibility in advocating for your product. They deserve special attention:

- Include them in advisory boards and design partnerships
- Give them advance notice of major changes that affect their workflow
- Respond to their escalations personally and quickly
- Don't change things that affect them without a heads-up

A champion who feels burned by your product becomes a detractor who may sabotage renewals.

## Next steps

- [Working with Sales](../05-go-to-market/working-with-sales.md) — the sales motion in enterprise
- [Pricing & Packaging](../05-go-to-market/pricing-and-packaging.md) — enterprise tier design
- [Regulated Environments](regulated-environments.md) — where enterprise meets compliance
