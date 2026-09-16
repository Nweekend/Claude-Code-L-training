# Thursday Prep: Streakly Comeback Experience

> Recap + agenda for the team session. Source: #product-growth Slack thread, Monday 9:14am, plus project.md.

## Recap

- Day-7 retention dropped from 48% to 39% since the streak redesign shipped.
- The drop is sharpest among users who break their streak in week 1 — missing two days in a row roughly doubles churn.
- Working hypothesis: breaking a streak feels like failure, and there's no graceful way back in. The app gives no acknowledgment when a streak resets (same home screen, counter at zero), and the "you lost your streak" push has a harsh tone with no offer of a way forward.
- Open question from the thread: is the core issue the streak reset mechanic itself, the notification tone/timing, or both?
- Early concept floated (Lena): a "Comeback screen" shown on streak break — best-streak stat, a 60-second comeback lesson, one-tap streak-freeze. Raj noted it's technically doable with existing data (no new data sources needed), pending logic for eligibility and freeze rules.
- Marcus asked for problem alignment before any solution design — this doc + project.md are that alignment starting point.

## Agenda (open questions for the team to work through)

1. **Root cause before fix.** What actually caused the Day-7 drop? Do we have enough evidence (data + user research) to say it's the streak reset, the notification, or both — before we commit to any direction?
2. **Iterate vs. rollback.** Is iterating on the current streak redesign the right move, or should rolling back be seriously considered? What would we need to know to decide?
3. **Outcomes and metrics.** Are we clear on the actual desired outcome here — and do the metrics we're currently watching (Day-7 retention, break-related churn) genuinely reflect that outcome, or are we missing something?

## Prep: Anticipated Objections & Our Position

Marcus is likely to push on evidence rigor, root cause, scope, and metrics — consistent with what he's already asked for. Worked through ahead of time, where we have enough to reason it out without new data:

### Iterate vs. rollback

None of the research (interviews or NPS) describes something specific to the v2 redesign — every complaint (reset to zero, no recovery, harsh notification, no acknowledgment) reads like a description of the fundamental all-or-nothing streak design, not a v2-specific regression. If that's right, rolling back to v1 likely wouldn't fix anything, since the same mechanic probably existed before v2 too.

**Caveat — this argument has a hole:** we don't actually have documented what v2 changed vs. v1. If v2 specifically removed a prior forgiveness mechanic or changed how breaks were handled, the rollback case gets much stronger. **Action item: confirm with Raj/eng exactly what v2 changed before or at Thursday's session** — this is foundational to the iterate-vs-rollback question and we shouldn't guess at it.

Separately, iteration has a practical edge regardless: Raj already confirmed the Comeback screen concept is feasible with existing data, while rollback's engineering cost and scope are unscoped.

### Metrics and targets

Proposed framework, to have ready if asked "is Day-7 retention even the right metric":

- **Primary:** Day-7 retention rate, with 48% (pre-v2 baseline) as the floor target.
- **Diagnostic:** break-related churn ratio (currently ~2x for users who miss 2 days) — watch for this narrowing.
- **New leading indicator (not yet instrumented):** post-break re-engagement rate — % of users who return within N days of a break. This doesn't exist today and would need to be built alongside any comeback feature to actually measure whether it worked.
- **Guardrail:** notification opt-out rate should not increase (NPS already shows users disabling notifications entirely).
- **Durability check:** Day-30 retention — Day-7 is a leading indicator, not the full answer, since Priya's account suggests the habit doesn't solidify until ~3 weeks. A fix that only delays churn by a few days wouldn't show up as a real win here.

### Scope discipline

The decision brief's "Recommended Action" currently reads as a settled direction, which risks looking like we've skipped the problem-alignment step Marcus explicitly asked for. Reframing it as conditional — "if the team confirms the streak-break moment as root cause, the recommended next step would be X" — keeps the sequencing honest: alignment first, solution options second. Edited into `docs/decision-brief.md`.

### Power-user risk (Priya vs. Tom)

Making streak recovery too easy could cheapen the "hard-won" feeling that Priya says made the habit stick at 30 days — we don't want to fix Tom's problem by undermining the exact mechanic that retains long-tenured users like Priya. Design principle to propose: keep any freeze/forgiveness mechanic visible, limited, and effortful (one-tap, not automatic silent protection), and leave milestone celebrations untouched. This is a hypothesis, not validated — worth a lightweight check with power users before broad rollout.

### Still open — no data to resolve these yet

- **Sample size:** n=3 interviews and n=10 NPS comments against 340K MAU is directional, not statistical. Honest answer if pushed: we'd want a larger analytics pull or cohort analysis to confirm this generalizes.
- **Causality:** we haven't ruled out other explanations for the drop coinciding with v2 (bugs, channel mix, seasonality). No shortcut here — flag it as a known limitation rather than overstating confidence.
