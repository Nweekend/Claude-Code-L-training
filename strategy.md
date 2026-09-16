# Strategy: Recovering the Day-7 Retention Drop

> Draft — discovery phase. Source: #product-growth Slack thread, Monday 9:14am, and CLAUDE.md.

## The Gap

Day-7 retention dropped 9 points, from 48% to 39%, since the streak redesign (v2) shipped.

## Working Hypothesis

Users go passive after breaking a streak because the break feels like failure, and there's currently no graceful way back in. Supporting signals from the thread:

- The drop is sharpest among users who break their streak in week 1.
- Once a user misses two days in a row, churn is almost double.
- Today, breaking a streak triggers no acknowledgment in-product — same home screen, counter reset to zero — and the "you lost your streak" push notification has a harsh tone with no offer of a way forward.

If this holds, users need a comeback path with a reason to return that's specific to their own progress — not a generic "keep going!" message.

## User Research Evidence

From 3 interviews (see `research/interview-synthesis.md`; n=3, directional not statistical):

- **The break itself is catastrophic and irreversible for at least one churned user.** Tom R. broke a 12-day streak after 5 weeks, got a "you lost your streak" notification, found no way to recover it, and churned to a competitor with a streak-freeze mechanic.
- **Milestone celebration builds long-term attachment.** Priya S. (14-month power user) says hitting a celebrated 30-day streak — "look what you built" — is what made the habit stick. It took her ~3 weeks to get there, and she believes most users quit before reaching that point.
- **New insight, not previously in scope:** streak-loss anxiety starts almost immediately, before any actual failure. Amara L. (4 days in) is already stressed about losing her streak, and says that pressure is turning the product from "game" into "chore." This means week-1 users face the full downside risk of the all-or-nothing streak long before they could ever reach the celebration payoff that builds devotion.

This shifts the hypothesis: the problem may not be only what happens *after* a break (the original framing), but also the anticipatory pressure the streak mechanic creates *before* any break, specifically in week 1 — a period too early for the positive payoff and fully exposed to the downside.

**Corroborating evidence from NPS feedback (n=10, see `research/nps-analysis.md`):** independent, higher-volume evidence pointing at the same problem:

- The streak-break moment is the dominant complaint (5 of 10 comments), not lesson content or the app's core value — praise was reserved for the lessons themselves.
- Users explicitly ask for a forgiveness mechanism ("coach, not scorekeeper"; "other apps let you freeze a streak, why not this one?") — direct support for the streak-freeze idea already in the proposed direction.
- Two new, previously unconfirmed pain points: notification tone/frequency reinforces a "punisher" feel and causes users to disable notifications entirely, and the home screen gives no visual acknowledgment of a user's actual state (2-day streak vs. returning after 2 weeks away).

**Competitive research (see `research/competitive-matrix.md`; 5 competitors):**

- Duolingo (streak repair) and Mimo (streak shields) both treat streak protection as pre-break insurance — limited-use, often paywalled — not a true post-break comeback experience. No competitor turns the moment after a full loss into active re-engagement, which matches exactly what our own users are asking for.
- No competitor tailors streak protection to the fragile first-week window specifically — protection is generic across tenure and typically gated behind a paid tier, leaving new, free-tier users with zero protection during the period our research shows is riskiest.
- These are the two white-space gaps Streakly could own; neither is currently reflected in the proposed direction below.

## Decision Brief (2026-09-14)

A synthesis of all research to date was compiled for Marcus — see `docs/decision-brief.md`. Recommended action: proceed with iteration, not rollback, and broaden scope beyond the original Comeback screen to include a week-1-specific safety net (tenure-independent streak protection, notification tone/frequency fixes, home-screen state-awareness) — since this is the only option addressing the full evidence base.

**Open validation gap:** `research/competitive-reddit.md` (real-user Reddit sentiment on competitors) was requested but not available, so the cross-check of whether Reddit sentiment confirms or contradicts the structured competitive research has not been done. Flagged in the decision brief as outstanding.

**Objection prep for Thursday (see `01-orient/thursday-prep.md`):** worked through the iterate-vs-rollback question, a proposed metrics/target framework, scope-discipline framing for the recommendation, and a power-user design consideration — all reasoned through with existing evidence, no new data needed. Two objections remain genuinely open (sample-size rigor, causality vs. correlation) and are flagged honestly rather than resolved. One concrete action item surfaced: confirm exactly what the v2 redesign changed vs. v1 before Thursday — this is foundational to the iterate-vs-rollback comparison and we don't currently have it documented.

## Key Tension

Re-engagement nudges vs. notification fatigue — bringing lapsed users back without over-messaging them.

## Open Decision

How to bring users back after they break a streak. Not yet resolved: whether the answer is a product change (e.g., what a streak break shows/offers), a messaging change (notification tone/timing), or both — this is explicitly still an open question raised by the team, not decided.

## Proposed Direction (early, unvalidated)

Floated by Lena: a "Comeback screen" shown when a user breaks a streak, including:

- The user's best-streak stat
- A one 60-second "comeback lesson" to rebuild momentum
- A one-tap streak-freeze to protect a rebuilt streak

Raj noted this is technically doable with existing data — no new data sources needed — pending logic for eligibility and streak-freeze rules.

Not yet reflected in this proposed direction, per the research above: the pre-break anxiety finding (Amara/NPS), notification tone/frequency, and home-screen state-awareness.

## Status

Partially validated by three independent sources — 3 interviews, 10 NPS comments, and competitive research across 5 apps — all pointing at the streak-break moment as the primary retention risk, with the streak-freeze concept directly supported by user asks and absent (in true comeback form) from every competitor reviewed. A recommendation (iterate + broaden scope to a week-1 safety net) has been drafted for Marcus in `docs/decision-brief.md`, but this is not yet a team decision. Gaps remaining: pre-break anxiety and notification tone/frequency aren't reflected in the original proposed direction, and Reddit sentiment on competitors (`research/competitive-reddit.md`) is still missing from the evidence base. Team has not yet confirmed root cause at scale, decided iterate-vs-rollback, or finalized direction. See `thursday-prep.md` for the open questions, and `research/interview-synthesis.md` / `research/nps-analysis.md` / `research/competitive-matrix.md` / `docs/decision-brief.md` for the underlying evidence.
