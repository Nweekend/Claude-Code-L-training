---
name: weekly-status
description: Turn raw bullet-point notes into a formatted leadership status update with Shipped, In Progress, Blockers, and Next Week sections. Use when asked to turn notes into a weekly status report, leadership update, or standup summary.
---

# Weekly Status Update

## Purpose

Convert raw, unstructured bullet notes into a concise, leadership-ready status update.

## Input

Raw bullet-point notes — unstructured, in any order, mixing completed work, ongoing work, blockers, and plans.

## Output Format

Produce exactly four sections, in this order:

1. **Shipped**
2. **In Progress**
3. **Blockers**
4. **Next Week**

Rules:

- Maximum 3 bullets per section.
- Plain declarative language — no jargon, no buzzwords, no acronyms.
- If a section has no relevant input, write "None."
- If more than 3 items qualify for a section, keep the 3 most significant and drop the rest — don't cram extras into one bullet.

## Style

- One sentence per bullet, active voice, stating what happened or will happen — not how it felt.
- No filler qualifiers ("basically," "essentially," "just").
- No editorializing adjectives ("amazing," "huge") — state facts only.

## Process

1. Read all raw notes.
2. Classify each note as Shipped / In Progress / Blockers / Next Week based on content and tense (completed, ongoing, stuck, or planned).
3. Rewrite each into one plain declarative sentence.
4. Trim each section to at most 3 bullets, keeping the most significant items.
5. Output the four sections in order, using "None." for any empty section.

## Example

**Input:**
- finished migrating the auth service to v2, tested in staging
- still working on the payments retry logic, about 60% done
- blocked on legal review for the new terms of service, waiting since Monday
- next week want to start the onboarding redesign
- also shipped the new empty-state illustrations
- fixed a flaky test in CI

**Output:**

**Shipped**
- Migrated the auth service to v2 and tested it in staging.
- Shipped new empty-state illustrations.
- Fixed a flaky test in CI.

**In Progress**
- Building the payments retry logic (about 60% done).

**Blockers**
- Waiting on legal review for the new terms of service since Monday.

**Next Week**
- Start the onboarding redesign.
