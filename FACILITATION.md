# Facilitation Guide — Navigating Difficult Conversations

Every activity carries a learner-visible **"Why this matters"** line, and
every teaching section has (1) an **interactive tool or practice moment**,
(2) a **labeled, timed activity** — *As a group* or *On your own* — and
(3) a **validation point** that tells you whether learning landed.

The full runbook lives in [`facilitator/notes.json`](facilitator/notes.json)
and follows the **ATD facilitator-guide framework**: per section a verbatim
**Say** script, **Do** choreography, an **Ask** with anticipated responses
and how to respond, a **Debrief** line, and a scripted **Transition** —
plus session front matter (materials, prep checklists, contingencies, and a
tough-questions bank). A first-time facilitator should be able to deliver
the class from the guide alone.

The **facilitator edition is live at `/facilitator/`** — regenerate after
any change to `index.html` or `notes.json`:

```bash
python3 tools/build-facilitator.py
```

## Run of show — two paths

| Slide | Full (90 min) | Core (60 min) |
|---|---|---|
| Welcome / QR | 3 | 2 |
| Objectives | 2 | 1 |
| Agenda | 1 | — |
| 01 The cost of avoiding | 6 | 4 |
| Manifesto | 1 | — |
| 02 The three conversations | 10 | 7 |
| 03 SBI feedback | 7 | 5 |
| Feedback Lab | 8 | 6 |
| 04 Opening with STATE | 8 | 4 |
| 05 Trust & BRAVING | 8 | 4 |
| 06 Radical Candor | 9 | 6 |
| 07 The first 30 seconds | 6 | 4 |
| 08 When it goes sideways | 5 | 3 |
| Recap quiz | 4 | 4 |
| My conversation plan (capstone) | 8 | 7 |
| Glossary | 1 | — |
| Closing / commitment | 3 | 3 |
| **Total** | **90** | **60** |

**Core-path rules:** every interactive tool, every check, the Feedback Lab,
the STATE rep (one round), and the capstone stay. Skip the agenda, manifesto,
glossary, and in-class videos; assign videos and skipped debriefs as
follow-ups. Per-section cuts live in each `coreNote`.

**Timing discipline:** the pair practices (STATE, sideways) stretch in
talkative rooms. Protect the last 15 minutes (recap, capstone, commitment)
by cutting group debriefs first, never the capstone.

**Privacy norms (load-bearing):** roles, never names, in every example; the
avoidance meter, BRAVING scorecard, and conversation plan are private and
never collected. If a disclosure involves policy violations, harassment, or
safety, route to HR — that's in the contingency table.

## Validation model

- **In the moment:** inline quick checks (01, 03, 04, 07, 08), the labeler
  score (02), Lab outcome tier (Lab), quadrant-sort score (06), BRAVING
  completion (05), and the out-loud STATE rep verdicts (04).
- **End of session:** the 6-question scored recap maps 1:1 to the learning
  objectives; the capstone plan and the commitment round are the transfer
  artifacts.
- **After:** the 7-day pulse ("Did you have the conversation? Which tool?
  What happened?") is the Kirkpatrick Level 3 evidence; 30/60/90-day check
  on SBI language appearing in 1:1s.
- **Deliberately not validated:** avoidance meter and BRAVING scores are
  private by design — facilitators must not collect them.
