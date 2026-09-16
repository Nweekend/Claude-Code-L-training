# Change Log: Streakly Comeback Experience

## Day 1 — 2026-09-14 — Discovery phase begins

- Logged the Day-7 retention drop (48% → 39%) as the driving problem, sourced from the #product-growth Slack thread (Monday 9:14am).
- Established project context: role (PM, Engagement squad), product (Streakly), current phase (Discovery), key tension (re-engagement nudges vs. notification fatigue), open decision (how to bring users back after a streak break).
- Created initial artifacts: `project.md` (problem statement, goals, non-goals, success metrics, stakeholders), `strategy.md` (working hypothesis and early Comeback screen direction), `thursday-prep.md` (recap + agenda for team session), and `CLAUDE.md` (persistent session context).
- No decisions made yet on root cause, iterate-vs-rollback, or final direction — all open going into Thursday's team session.

## Day 2 — 2026-09-14 — User interview synthesis

- Synthesized 3 user interviews (Priya S., power user; Tom R., churned user; Amara L., new user) into `research/interview-synthesis.md` — 5 themes, supporting quotes, contradictions, and a key insight.
- New finding: streak-loss anxiety starts almost immediately (by day 4, per Amara) — well before the ~3-week mark it takes to reach the celebration payoff that builds long-term attachment (per Priya). This means week-1 users face the full downside of the all-or-nothing streak with no access yet to the upside.
- Updated `strategy.md`: added a User Research Evidence section, and flagged that the proposed Comeback screen only addresses the post-break moment — not the pre-break anxiety the new research surfaced. Status moved from "unvalidated" to "partially validated by interviews (n=3, directional)."
- Still open: root cause at scale, iterate-vs-rollback, and final direction — unchanged going into Thursday's session.

## Day 3.5 — 2026-09-14 — Competitive research + decision brief

- Researched 5 competitors (Duolingo, Babbel, Elevate, Memrise, Mimo) into `research/competitive-matrix.md` — core features, pricing, target customer, post-week-1 engagement, and recent changes for each, plus a comparison matrix and 2 white-space gaps for Streakly.
- White space identified: no competitor has a true post-break comeback experience (only pre-break insurance like streak repair/shields), and none tailor streak protection to the fragile first-week window specifically.
- Synthesized all research to date into `docs/decision-brief.md` for Marcus: situation, key findings, 3 options considered, a recommended action (iterate + broaden scope to a week-1 safety net, not rollback), and why now.
- Data gap noted: `research/competitive-reddit.md` (requested as a 4th source) was not available, so the Reddit-vs-structured-research cross-check could not be performed this round — flagged as outstanding in the brief.
- Updated `strategy.md`: added competitive research findings, summarized the decision brief and its recommendation, and updated Status to reflect three independent evidence sources plus the outstanding Reddit gap.
- Still open: root cause at scale, iterate-vs-rollback, and final direction — this is now a drafted recommendation, not yet a team decision, going into Thursday's session.

## Day 3.75 — 2026-09-14 — Objection prep for Thursday

- Anticipated Marcus's likely questions/objections and worked through the ones answerable with existing evidence: added an "Anticipated Objections & Our Position" section to `01-orient/thursday-prep.md` covering iterate-vs-rollback, a proposed metrics/target framework, scope-discipline framing, and a power-user (Priya vs. Tom) design consideration.
- Key argument: none of the research describes a v2-specific complaint — pain points read like the fundamental streak design, not a v2 regression — so rollback likely wouldn't fix anything. Caveat: we don't have documentation of what v2 actually changed vs. v1. **Action item before Thursday: confirm this with Raj/eng.**
- Updated `docs/decision-brief.md`: tightened the rollback option with this argument, and reframed "Recommended Action" as conditional on Thursday's root-cause alignment rather than a settled direction. Added the metrics framework and power-user design consideration to the recommendation.
- Left two objections explicitly open (sample-size rigor, causality vs. correlation) — no new data available to resolve them, flagged honestly rather than argued around.
- Updated `strategy.md` to summarize this prep work and surface the v2-diff action item.

## Day 3 — 2026-09-14 — NPS feedback analysis

- Analyzed 10 raw NPS comments into `research/nps-analysis.md` — themes ranked by frequency, praise vs. complaints, and top 3 actionable issues, framed as a findings report for Marcus.
- Corroborating evidence: streak-break moment is the dominant complaint (5 of 10 comments), independent of the interview findings. Praise was reserved for lesson content, not the streak mechanic.
- Two new pain points not previously captured: notification tone/frequency reinforces a "punisher" feel and causes users to disable notifications; home screen gives no visual acknowledgment of a user's actual state (2-day streak vs. returning after 2 weeks).
- Updated `strategy.md`: added NPS corroboration to the User Research Evidence section, noted these two gaps aren't addressed by the current proposed Comeback screen direction, and updated Status to reflect two independent sources of partial validation.
- Still open: root cause at scale, iterate-vs-rollback, and final direction — unchanged going into Thursday's session.
