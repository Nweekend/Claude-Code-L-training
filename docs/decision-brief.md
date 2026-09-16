# Decision Brief: Streakly Comeback Experience

> For: Marcus (Head of Product). Prepared by: Natalia, PM, Engagement squad.
> Sources: `research/interview-synthesis.md` (n=3), `research/nps-analysis.md` (n=10), `research/competitive-matrix.md` (5 competitors).
> **Data gap:** `research/competitive-reddit.md` was not available for this synthesis — the requested check of whether real-user Reddit sentiment confirms or contradicts the structured competitive research could not be performed this round. Recommend closing this gap before finalizing direction.

## Situation

Day-7 retention has dropped 9 points (48% → 39%) since the v2 streak redesign shipped, driven almost entirely by users who break their streak in week 1. Three independent research efforts — user interviews, NPS feedback, and competitive research — now converge on the same conclusion: the all-or-nothing streak mechanic itself, not lesson content, is the primary driver of this drop.

## Key Findings

- **Streak break is the dominant churn trigger, confirmed by two independent sources.** Interviews (Tom R.'s churn story) and NPS data (5 of 10 comments) both independently point to the reset-to-zero moment, not content quality, as the reason users leave.
- **Anxiety starts before any failure, specifically in week 1** — a finding unique to the interviews (Amara L., day 4) and not something the NPS or competitive data could confirm or contradict directly, since neither source probes pre-break sentiment. This is a live, unvalidated risk factor.
- **Competitors treat streak protection as pre-break insurance, not a true post-break comeback.** Duolingo's streak repair and Mimo's streak shields are both limited, often paywalled undo mechanisms — none turns the moment after a full loss into active re-engagement. This matches what NPS/interview users are explicitly asking for ("coach, not scorekeeper").
- **Users can name the feature they want, and it exists elsewhere.** NPS respondents cite competitor streak-freeze functionality by name; competitive research confirms Duolingo and Mimo both offer some version of it. Streakly currently offers none.
- **Notification tone and lack of state-awareness compound the problem.** Both interviews and NPS flag a harsh "you lost your streak" notification and a home screen that doesn't distinguish a 2-day streak from a 2-week return — secondary but reinforcing issues, not the root cause.

## Options Considered

1. **Ship the Comeback screen as originally scoped** (best-streak stat, 60-second comeback lesson, one-tap streak freeze) — addresses the post-break moment only. Technically feasible with existing data (per Raj); doesn't address the pre-break anxiety Amara's interview surfaced.
2. **Roll back the v2 streak redesign.** Fastest path to the pre-drop baseline if the redesign itself is the root cause — but none of the research describes a complaint specific to v2; every pain point (reset to zero, no recovery, harsh notification) reads like the fundamental all-or-nothing streak design, which likely predates v2. If so, rollback wouldn't fix it. **Open item: we don't have documentation of exactly what v2 changed vs. v1 — need to confirm this before or at Thursday's session, since it's foundational to this comparison.**
3. **Broaden scope to a "week-1 safety net"**: the Comeback screen plus tenure-independent (not just paid-tier) streak protection in week 1, notification tone/frequency fixes, and home-screen state-awareness. Directly targets the competitive white space (no competitor protects new, free-tier users specifically) but is a larger scope to validate and build.

## Recommended Action

Conditional on Thursday's root-cause alignment, not a settled direction: if the team confirms the streak-break moment as root cause, proceed with iteration, not rollback, starting with Option 3 (Comeback screen plus a week-1-specific safety net) — the only option addressing the full evidence base, including the pre-break anxiety finding. Success should be measured against Day-7 retention (floor: 48% baseline) plus a new post-break re-engagement rate (not yet instrumented) and a Day-30 durability check, not Day-7 alone. Any freeze/forgiveness mechanic should stay visible and effortful (not silent/automatic) to avoid cheapening the milestone-earned feeling that retains power users like Priya.

## Why Now

The Day-7 drop is active and compounding every week; the competitive white space (a true comeback experience, not just pre-break insurance) is currently unclaimed but Duolingo's 2026 shift toward friendlier, less punitive mechanics suggests that window may close; and Thursday's team session is the natural checkpoint to align on root cause and direction before committing engineering time.
