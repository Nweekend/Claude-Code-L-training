# Project: Streakly Comeback Experience

> Draft PRD skeleton — starting point only, not a finished document.
> Source: #product-growth Slack thread, Monday 9:14am.

## Company / Product Context

- Streakly is a consumer habit + micro-learning app: users pick a track, complete a short daily lesson (5 minutes), and build a streak. The streak is the core habit loop.
- Launched 4 years ago. Series B funded ($42M).
- 2.1M registered users; 340K monthly active users (MAU).
- Growing at 28% YoY on MAU.

## Squad & Current Phase

- **Squad:** Engagement squad
- **My role:** PM, Engagement squad
- **Current phase:** Discovery

## Key Stakeholders

From the #product-growth Slack thread:

- **Marcus (Head of Product)** — surfaced the Day-7 retention drop, called the Thursday alignment meeting, asked for the problem write-up before solutioning.
- **Raj (Senior Engineer)** — brought the retention data analysis (week-1 streak breaks, 2x churn after two missed days); assessed technical feasibility of the Comeback screen concept.
- **Lena (Product Designer)** — brought user research context on how the streak reset feels to users; sketched the initial Comeback screen concept.
- **You (Natalia)** — PM, Engagement squad; framed the "graceful comeback" hypothesis in the thread.

## Problem Statement

Day-7 retention has dropped from 48% to 39% since the streak redesign shipped. The drop is sharpest among users who break their streak in week 1 — once someone misses two days in a row, churn is almost double.

Working hypothesis: users go passive because breaking a streak feels like failure, and there's currently no graceful way back in. When a streak resets, the app shows no acknowledgment — same home screen, counter back at zero — and the "you lost your streak" push notification has a harsh tone with no offer of a way forward. Users need a comeback path with a reason to return that's specific to their own progress, not a generic "keep going!" message.

Open question raised by the team: is the core issue the streak reset mechanic itself, the notification tone/timing, or both?

## Goals

- Align the team on the problem before designing solutions (target: before Thursday's meeting).
- Explore a "Comeback screen" concept shown when a user breaks a streak, which would include:
  - Their best-streak stat
  - A one 60-second "comeback lesson" to rebuild momentum
  - A one-tap streak-freeze to protect a rebuilt streak

## Non-Goals

- No new data sources are required for the Comeback screen concept (per Raj) — this is a scope constraint, not confirmed non-goals list.
- TBD — not yet discussed in the thread.

## Success Metrics

- Day-7 retention rate (currently 39%, down from 48% pre-redesign) — the metric prompting this work.
- Churn rate for users who break their streak / miss two days in a row (noted as ~2x higher) — relevant but no target defined yet.
- No specific target numbers or additional metrics (e.g., engagement with the Comeback screen itself) have been defined in the thread yet — TBD.
