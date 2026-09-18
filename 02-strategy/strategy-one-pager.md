**AI Strategy One-Pager · Juno Automated Prioritization**

**RocketShip · Q3 2026 Strategy**

**North Star**

Become the fastest and most reliable analytics platform for mid-market data teams that currently rely on Excel and Salesforce to analyze, report, and act on business data.

Our Q3 priorities are clear: protect reliability, unlock enterprise adoption, and accelerate time-to-insight.

**Strategic Pillars**

**1. Reliability First**

The platform must work—every export, every report, every load.

Reliability issues are creating customer workflow blockers and putting enterprise revenue at risk. P0 issues currently include CSV export crashes, 403 permission errors, and queue overflows on large reports.

Enterprise opportunities, including Pearson Co and Acme, have been affected by platform reliability concerns.

Q3 priority: Resolve critical reliability issues before investing in net-new functionality. No new feature work should ship when the legacy reporting API is operating at critical capacity.

**2. Enterprise Compliance**

Enterprise readiness depends on security, compliance, and access controls.

SAML/SSO, audit logs, and role-based permissions are required capabilities for enterprise customers.

The Acme opportunity represents $200K ARR and depends on Okta SSO being available by October 1.

Q3 priority: Prioritize compliance capabilities that directly unblock committed enterprise opportunities or remove documented barriers to enterprise adoption.

**3. Speed-to-Insight**

Customers choose RocketShip because it helps them get from data to insight quickly.

Mid-market analysts should experience RocketShip as faster and easier than workflows built around Excel and Salesforce.

Performance degradation directly conflicts with this differentiation. Examples include exports taking more than 30 seconds or compute-heavy AI summarization that adds latency to already constrained infrastructure.

Q3 priority: Prioritize improvements that reduce the time required to load, analyze, export, or act on data. Avoid features that materially increase latency without demonstrated customer value.

**What We Are Not Doing This Quarter**

The following are explicitly outside Q3 priorities unless new customer evidence or business conditions justify reconsideration:

Aesthetic-only refreshes, including dark mode, color palette changes, and general "make it pop" UI requests.

Competitor-inspired AI features without demonstrated customer need or measurable value.

TikTok integrations or other social-platform integrations unrelated to the Q3 strategy.

Dashboard summarization requiring significant database sharding or infrastructure work.

Net-new features that materially increase platform instability or degrade export and dashboard performance.

**Prioritization Decision Rules**

Juno uses the following rules when developing a priority recommendation:

P0 — Critical: A documented customer workflow blocker, critical reliability issue, or requirement that directly unblocks an enterprise opportunity with stated ARR.

P1 — High: Strongly supports a strategic pillar and has clear customer evidence, but does not represent an immediate critical failure or revenue blocker.

P2 — Medium: Provides demonstrated customer value and strategic alignment but has lower urgency, impact, or supporting evidence.

P3 — Low: Has limited strategic impact or introduces meaningful reliability, performance, or delivery tradeoffs.

notRecommended: Lacks credible customer evidence, conflicts with the Q3 strategy, or is explicitly identified as work we are not doing this quarter.

**Additional Rules**

If a request reduces reliability or materially slows export/dashboard performance, recommend P3 or notRecommended unless stronger evidence demonstrates that the benefit outweighs the impact.

If a request directly unblocks a documented enterprise opportunity with stated ARR, recommend P0.

If a request is based primarily on executive or stakeholder opinion without supporting customer or business evidence, recommend notRecommended.

If a request resolves a documented customer workflow blocker, such as a CSV crash or permission failure, recommend P0 or P1 based on severity and scope.

If available evidence conflicts or does not clearly support a priority, Juno should surface the uncertainty rather than infer strategic alignment.

**Human Decision Authority**

Juno uses this strategy to retrieve evidence, compare signals, and develop defensible prioritization recommendations.

Juno recommends. The PM decides.

Every recommendation must show the evidence and strategic rationale used so the PM can validate, challenge, or override the recommendation before it affects the roadmap.
