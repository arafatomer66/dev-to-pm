# PM Tooling Landscape

You don't need all of these. You need a small set of tools used well. This page maps the landscape so you can choose appropriately for your context.

## Roadmap & product planning

**Productboard:** Purpose-built product management. Connects user feedback, features, and roadmap. Good for larger teams with a lot of incoming requests.

**Jira Product Discovery (formerly Jira Align / Advanced Roadmaps):** If your engineering team is on Jira, this keeps PM and delivery in the same system.

**Linear:** Fast, developer-friendly issue tracker with good roadmap views. Growing PM adoption, especially at startups.

**Notion:** Flexible docs and databases. Many PMs use Notion for PRDs, strategy docs, and roadmaps when the team doesn't need a dedicated tool.

**Coda:** Similar to Notion, with more powerful formulas. Good for building custom PM workflows.

**Simple spreadsheet:** Don't underestimate Google Sheets for roadmaps at early stage. A well-structured sheet often beats a new tool with a learning curve.

## Analytics & metrics

**Amplitude:** Industry-standard for product analytics. Strong event tracking, funnels, cohort analysis, A/B test analysis.

**Mixpanel:** Similar to Amplitude. Stronger on real-time analytics; slightly steeper learning curve.

**Heap:** Auto-captures all user interactions without pre-instrumentation. Good if you have retroactive analysis needs.

**Pendo:** Combines product analytics with in-app messaging and user guides. Popular in B2B.

**Looker / Mode / Metabase:** SQL-based BI tools. Better for deep custom analysis and connecting product data to business data.

**PostHog:** Open-source product analytics with feature flags and session replay. Popular at startups that want control over their data.

## Customer research & feedback

**Dovetail:** User research repository. Synthesizes interview notes, tags insights, makes research findable across the team.

**Notion:** Many PMs use Notion as a lightweight research repository before graduating to a dedicated tool.

**Hotjar / FullStory / LogRocket:** Session recording and heatmaps. See how users actually use your product.

**UserInterviews / Respondent:** Recruiting panels for user research. Paid access to your target audience for interviews.

**Typeform / Google Forms:** Survey tools. Lightweight, no coding required.

**Zendesk / Intercom:** If your support team uses these, there's usually a way to analyze ticket themes for product insights.

## Prototyping & design

**Figma:** The industry standard. PMs don't design, but you need to be able to read and comment on Figma files.

**Marvel / InVision:** Clickable prototype tools. Useful for quick concept tests.

## Experimentation

**Optimizely:** Mature A/B testing platform for web.

**LaunchDarkly:** Feature flags with experimentation capabilities. More engineering-focused but PMs set experiment parameters.

**GrowthBook:** Open-source experimentation platform.

**Split:** Feature flags + experiment framework.

## Communication & collaboration

**Slack:** Default async communication in most tech companies.

**Loom:** Async video. Useful for walking through specs and roadmaps without requiring a meeting.

**Miro / FigJam:** Digital whiteboards for remote workshops, user story mapping, affinity mapping.

**Confluence:** Documentation wiki. If your engineering team uses Confluence, your PRDs should live there.

## How to choose

The right toolset depends on:

1. **What your team already uses.** The best tool is one your team will actually open. A PM using Productboard while everyone else uses Linear creates a fragmented workflow.

2. **Company stage.** Early stage: use the lightest tools possible. Spending 3 weeks implementing Productboard at a 10-person startup is premature optimization.

3. **Your own skill gaps.** If you're weak on analytics, invest in learning Amplitude or Mixpanel properly, not collecting more tools.

**The minimum PM toolkit:**
- Docs tool (Notion, Confluence, Google Docs)
- Analytics (whatever your company uses — learn it deeply)
- Communication (Slack + whatever your company uses)
- Design (be able to read Figma)

Everything else is enhancement.

## A note on AI tools

AI tools are increasingly part of the PM workflow. Current practical uses:
- Drafting first versions of PRDs and briefs
- Summarizing customer interview transcripts
- Competitive research (ask AI for a quick landscape overview before doing your own deeper research)
- Preparing for stakeholder meetings (use AI to anticipate objections)
- Writing SQL queries if you're not fluent

The caveat: AI tools produce plausible-sounding content that may be wrong or outdated on specifics (competitive landscape, pricing, technical capabilities). Verify any specific claims before putting them in a document you're accountable for.

See [AI for PMs](ai-for-pms.md) for more detail.

## Next steps

- [AI for PMs](ai-for-pms.md) — using AI in your PM workflow
- [Data-Driven Decisions](../02-core-skills/data-driven-decisions.md) — the analytics skills that go with the analytics tools
