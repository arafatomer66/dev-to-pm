# Pricing & Packaging

Pricing is one of the highest-leverage product decisions you'll make. A 1% improvement in pricing drives more revenue than a 1% improvement in acquisition or retention. Yet most PMs treat pricing as a finance or sales problem and stay away from it.

This is a mistake. How your product is priced directly shapes what you build, who buys it, and what outcomes users seek. Pricing is product strategy.

## The three pricing philosophies

### Cost-plus pricing
Price = your costs + desired margin.

Used by: manufacturers, services businesses, commoditized products.

Problem for software: once you've built the software, the marginal cost per user is nearly zero. Cost-plus produces artificially low prices that leave value on the table.

### Competitive pricing
Price = what competitors charge, roughly.

Used by: market entrants, commodity markets.

Problem: anchors you to competitors' positioning. If you're differentiated, you're underselling. If you're not differentiated, you're in a race to the bottom.

### Value-based pricing
Price = what the value is worth to the buyer.

This is the right model for software products with differentiated value. It requires understanding what outcomes your product produces and what those outcomes are worth.

**How to do it:** Interview customers and ask what alternatives they're comparing against. What would they pay for those alternatives? What additional value does your product provide above that baseline? What would they lose if your product went away tomorrow?

This is uncomfortable because it requires talking to customers about money. Do it anyway.

## Pricing models

| Model | How it works | Best for |
|-------|-------------|----------|
| **Per seat** | Charge per user/month | Collaboration tools; predictable for buyers |
| **Usage-based** | Charge per API call, GB, event, etc. | Infrastructure, APIs, data products |
| **Flat subscription** | One price for all users | Internal tools; simple products |
| **Tiered** | Different packages at different price points | Most B2B SaaS |
| **Freemium** | Free tier + paid upgrade | PLG products with network effects |
| **Outcome-based** | Charge as a % of value created | Services, some new AI products |

The model that's right for you depends on: how value scales for customers, how predictable revenue you need, and what your competition has anchored buyers to expect.

## Packaging tiers

Most B2B SaaS uses tiered packaging (Free/Starter/Pro/Enterprise or similar). How to design tiers:

**Step 1: Identify your buyer segments.** An individual freelancer, an SMB, and an enterprise have very different needs and very different ability to pay. Build tiers around these segments, not arbitrary feature bundles.

**Step 2: Design each tier around a value gate.** Each tier upgrade should unlock a category of value — not just more seats or more storage. Example: the Starter plan lets you do X. The Pro plan unlocks Y, which is only valuable once you've outgrown Starter.

**Step 3: Make the upgrade path natural.** Users in the Starter plan should hit a natural ceiling that makes the Pro plan obviously worth the upgrade. If users can run their entire use case forever on the free tier, you don't have a business.

**Step 4: Put things behind tiers deliberately.** Don't just put your "nice" features behind higher tiers. Put the features that matter most to your growth customers behind higher tiers. This is counterintuitive but drives upgrades.

## Freemium economics

Freemium works when:
- The product has network effects (more users → more value)
- There's a natural viral loop (free users expose the product to others)
- The marginal cost per free user is low
- You can convert enough free users to paid to cover the cost of the free tier

Freemium fails when:
- The free tier is so good that users never need to upgrade
- There's no viral loop to drive acquisition from the free base
- Free user costs are high (customer support, infrastructure, compliance)
- Your typical buyer is an enterprise that won't let employees sign up for free tiers

For most B2B products, freemium is not the right default. A free trial (time-limited) often works better than a free tier (feature-limited) for enterprise-motion products.

## How pricing shapes your backlog

This is the insight most PMs miss: your pricing model creates incentives that shape what features are worth building.

**Per-seat pricing:** Every feature that makes the product more valuable per user is worth building. Features that reduce seat count are dangerous.

**Usage-based pricing:** Features that increase usage volume are strategic. Features that help users use less are dangerous (even if users love them).

**Flat subscription:** No feature has a direct revenue relationship — you have to connect features to retention and expansion, which requires more indirect reasoning.

**Freemium:** Features that create network effects and drive viral growth are strategic. Features that serve power users but don't expose new users to the product are lower priority.

Understanding your pricing model helps you have more principled roadmap arguments. "This feature increases per-seat value" is a stronger argument under per-seat pricing than "this feature saves users time" with no revenue connection.

## Talking to customers about pricing

This is the part most developers-turned-PM avoid. Have the conversation.

Ask prospects during sales cycles: "What budget are you expecting to allocate for this?" Ask customers in QBRs: "What would need to be true for you to spend 2x what you're spending today?" Ask churned customers: "Was pricing a factor?"

You'll be surprised how much information is available if you just ask. Customers who pay for your product have thought about its value. They'll usually tell you.

## Next steps

- [Business Models](../07-business-skills/business-models.md) — how the business model shapes pricing
- [Finance & P&L](../07-business-skills/finance-and-pl.md) — the revenue metrics that flow from pricing decisions
- [Working with Sales](working-with-sales.md) — how pricing interacts with the sales motion
