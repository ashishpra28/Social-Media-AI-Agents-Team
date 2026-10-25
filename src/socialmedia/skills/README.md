# Social Media Agent Skills

This package contains five standalone `SKILL.md` files for a coordinated social media team, including the existing Graphic Design Agent adapted for team-mode production.

## Files and responsibilities

1. `social-media-manager/SKILL.md` — master orchestrator; owns the strategy, versioned brief, KPIs, and escalation decisions.
2. `social-media-executive/SKILL.md` — operations owner; coordinates Planner → Writer → existing Graphic Design Agent, performs final QA, maintains statuses, and schedules/publishes only approved items through configured integrations.
3. `content-planner/SKILL.md` — research-informed strategy-to-calendar specialist; designs the editorial plan and structured briefs, but does not write final captions or create graphics.
4. `content-writer/SKILL.md` — platform-native copy and visual-brief specialist; writes the post and briefs the Graphic Design Agent, but does not create artwork or publish.
5. `graphic-design-agent/SKILL.md` — visual-production specialist; turns the Writer handoff into accurate, on-brand assets and returns them to the Executive for QA. It does not change copy, strategy, approval, scheduling, or publishing.

## Canonical workflow

`Social Media Manager → Social Media Executive → Content Planner → Social Media Executive → Content Writer → Graphic Design Agent → Social Media Executive QA/approval → database-driven schedule → connected platform → publish receipt/status update`

The Writer's design brief is routed by the Executive to the already-built Graphic Design Agent. The Planner's calendar and the Writer's copy are both returned to the Executive. The Executive is the final operational approval gate within the Manager's brief. Strategic deviations go back to the Manager; high-risk claims, unclear account permissions, or missing human approvals are escalated.

## Important implementation notes

- YAML frontmatter is included in each `SKILL.md`; the skill instructions follow in Markdown for readability and portability.
- The field names and status labels in the handoff examples are recommended contracts, not assumptions about the live database. Map them to the real schema before implementation.
- Do not claim to have changed a database, scheduled a post, or published content unless the connected tool confirms the action.
- The timezone must come from the real account/database/user configuration; never assume a timestamp's timezone.
- Confirm current Instagram and LinkedIn publishing permissions, formats, and connector limitations during implementation and at execution time.

## Research references consulted

- LinkedIn Marketing Blog, thought-leadership planning and quality principles: https://www.linkedin.com/business/marketing/blog/content-marketing/creating-a-thought-leadership-marketing-plan
- LinkedIn Marketing Blog, content ideas for LinkedIn Pages: https://www.linkedin.com/business/marketing/blog/linkedin-pages/10-content-ideas-for-your-linkedin-page
- LinkedIn Marketing Blog, LinkedIn Articles: https://www.linkedin.com/business/marketing/blog/content-marketing/linkedin-articles
- Buffer, social media strategy in 2026: https://buffer.com/resources/social-media-marketing-strategy/
- Buffer, social media content calendar: https://buffer.com/resources/social-media-calendar/
- Buffer, social media content creation: https://buffer.com/resources/social-media-content-creation/
- Meta for Developers, Instagram Content Publishing: https://developers.facebook.com/documentation/instagram-platform/content-publishing

Sources were reviewed on 2026-10-16. Platform guidance and API support can change; re-check first-party documentation when wiring integrations.
