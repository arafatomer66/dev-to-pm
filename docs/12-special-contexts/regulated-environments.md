# Regulated Environments

Healthcare, finance, legal, government, and other regulated industries have product requirements that don't apply in consumer tech. This page covers how to PM effectively when compliance is part of the product.

## Compliance as a market requirement

In regulated industries, compliance is not a feature — it's a prerequisite to be in the market at all. HIPAA for healthcare, SOC 2 for general enterprise security, PCI-DSS for payments, GDPR/CCPA for data privacy, FedRAMP for government — each represents a set of non-negotiable requirements.

**The PM mindset shift:** Compliance is not a tax on innovation. It's a market characteristic that defines who can play. If your competitors aren't compliant, you have an asymmetric opportunity. If they are, you need to match them to stay in the game.

**The wrong framing:** "Legal is blocking us." Compliance is a business requirement like any other. Treat it as a product requirement, put it on the roadmap, and resource it appropriately.

## Common compliance frameworks PMs encounter

### SOC 2 (Type I and Type II)
Validates that your systems and processes meet security, availability, processing integrity, confidentiality, and privacy standards. Type I is a point-in-time audit; Type II covers a period (usually 12 months).

**What it means for PM:** Certain security controls (access logging, encryption, incident response) become non-negotiable product requirements. Features that would require changes to these controls need security review.

### HIPAA
Governs how health information is used and protected in the US. If your product touches protected health information (PHI), you need HIPAA-compliant infrastructure and processes.

**What it means for PM:** Strong access controls, audit logs, BAA agreements with vendors — these become product requirements. Features that involve PHI need privacy review before specification.

### GDPR / CCPA
Data privacy regulations governing user rights over their personal data. GDPR (EU), CCPA (California) have similar structures: consent requirements, right to deletion, right to data portability, data minimization.

**What it means for PM:** Features that collect, process, or store personal data need privacy design review. "Delete my account" must actually delete the data (or document why retention is required). Data export must be user-accessible.

### PCI-DSS
Standards for handling payment card data. If your product processes, stores, or transmits card data, PCI-DSS requirements apply.

**What it means for PM:** Use Stripe or a payment processor that handles PCI scope rather than building your own. Scope reduction (not touching the card data) is a product architecture decision that reduces compliance burden.

## Triaging compliance mandates

Not every compliance requirement is urgent. Use a triage framework:

| Category | Priority | Example |
|----------|---------|---------|
| **Blocking revenue** | Critical — do now | Enterprise customer requiring SOC 2 before signing |
| **Blocking market** | High — plan this quarter | HIPAA compliance to enter healthcare vertical |
| **Risk mitigation** | Medium — plan this half | GDPR data deletion to reduce regulatory risk |
| **Nice to have** | Low — backlog | Additional security certifications beyond current customer requirements |

Don't let legal scare you into treating all compliance items as critical. Everything has a risk/cost tradeoff.

## Working with legal and security

Legal and security teams are frequently characterized by PMs as blockers. In practice, they're stakeholders with different risk tolerances and time horizons.

**What works:**
- Bring them in early — "here's what we're thinking, here's the potential privacy/security surface" — not after you've finalized the design
- Ask "what would make this compliant?" not "can we do this?" The first question invites solutions; the second invites vetoes
- Understand their concerns — often there's a specific mechanism they're protecting against, and there are multiple ways to address it
- Escalate when they're blocking legitimate work — this is a business decision, not just a legal decision

**What doesn't work:**
- Ignoring compliance until the legal team finds out anyway
- Treating compliance requirements as legal's problem, not product's problem
- Springing completed designs on legal for review the week before launch

## Compliance as competitive advantage

In regulated industries, being genuinely compliant (not just checking boxes) is a differentiator.

- **Healthcare:** HIPAA-ready out of the box, while competitors require 6-month security reviews
- **Finance:** SOC 2 Type II with clean reports, while competitors have qualifications
- **Government:** FedRAMP authorization, which most commercial SaaS products don't have

If your target market is regulated, invest in genuine compliance ahead of the curve rather than catching up. First-mover compliance advantage is durable.

## What compliance requires from PMs

**Data minimization:** Don't collect data you don't need. The more data you collect, the larger your compliance surface. "Should we track this event?" is a compliance question, not just a product question.

**Privacy design reviews:** For any feature that touches personal data, a privacy review should be standard process. This is not legal's job alone — PM defines what data is collected and why.

**Incident response planning:** What happens when there's a data breach? PM needs to understand the response process well enough to design product features that support it (audit logs, access controls, notification systems).

**Documentation:** Compliance requires evidence. PMs who write clear PRDs and maintain decision logs make compliance audits significantly easier.

## Next steps

- [B2B Products](b2b-products.md) — where regulated industries and enterprise overlap
- [Working with Leadership](../06-working-with-teams/working-with-leadership.md) — escalating compliance decisions appropriately
