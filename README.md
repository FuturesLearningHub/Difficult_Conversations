# Navigating Difficult Conversations — A Manager's Toolkit

An interactive, single-page teaching site for **people managers, team leads,
and HR/talent partners** at Vanderbilt. Built as a **Learning on Demand**
program: the facilitator projects it in class while learners scan a QR code
and work the exercises on their own devices, or share the link for
self-paced review.

Part of the Vanderbilt Learning Series, in the FLH visual system (black &
gold, Libre Caslon / Inter / Antonio, one idea per screen), alongside
[AI Basics](https://futureslearninghub.github.io/AI_Classroom/).

- **Learner edition:** https://futureslearninghub.github.io/Difficult_Conversations/
- **Facilitator edition:** https://futureslearninghub.github.io/Difficult_Conversations/facilitator/

## Running it

Plain HTML/CSS/JS, no build step:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## What it teaches (8 sections)

1. The cost of avoiding — McKinsey's "obligation to dissent"
2. The three conversations — Stone, Patton & Heen (Harvard Negotiation Project)
3. SBI feedback — Center for Creative Leadership
4. Opening with STATE — Crucial Conversations
5. Trust and BRAVING — Brené Brown, plus Sinek's circle of safety
6. Radical Candor — Kim Scott's two-axis grid
7. The first 30 seconds — SHRM's three questions, the assembled opener
8. When it goes sideways — tears, anger, silence, and the contrast statement

Ends with a scored recap quiz, a **capstone conversation plan** (opener,
counter-move, recovery line, listening plan, and a date within 7 days), a
flip-card glossary, and a public commitment close. A printable
`worksheet.html` mirrors the capstone for no-device rooms, and
`cheatsheet.html` is the take-home reference.

## The interactive tools

| Slide | Tool | What learners do |
|---|---|---|
| The cost | **Avoidance meter** | Slide to how long they've been avoiding it; the cost readout updates |
| Three conversations | **Name that conversation** | Label five real lines as What Happened / Feelings / Identity |
| SBI | **Anatomy highlighter** | Tap Situation · Behavior · Impact to find each in a real example |
| Feedback Lab | **Graded builder** | Assemble feedback from options and watch how the reaction changes |
| STATE | **Anatomy highlighter** | Tap the five STATE moves in a full opener |
| Trust | **BRAVING scorecard** | Privately rate seven trust behaviors; get a growth edge |
| Radical Candor | **Quadrant sort** | Sort four scenarios into the 2×2 grid |
| Recap | **Scored quiz** | 6 questions mapped 1:1 to the objectives |
| Capstone | **My Conversation Plan** | Build and copy a dated plan for a real conversation |

All interactions are keyboard-accessible, use `aria-live` for dynamic
content, and honor `prefers-reduced-motion`. Private exercises (avoidance,
BRAVING, the plan) never leave the learner's screen.

## The facilitator edition

Generated at `/facilitator/` by:

```bash
python3 tools/build-facilitator.py
```

It mirrors the learner deck with an **ATD-style scripted rail** on every
slide — Say / Do / Ask (with anticipated responses) / Debrief / Transition,
plus Full-vs-Core timing — and opens with a **Facilitator Briefing** slide
(prep checklists, materials, contingencies, tough-questions bank). Its QR
encodes the **learner** URL. Regenerate after editing `index.html` or
`facilitator/notes.json`. See FACILITATION.md for the run of show
(Full 90 min / Core 60 min).

## Presenting

The page is a scrollable site and a keyboard-driven deck: arrows / Space /
PageUp/Down to move, Home/End to jump, dot rail and bottom pill to navigate.
Hero background is a Higgsfield-generated 3-clip montage streamed from CDN;
if it fails, a gold particle canvas takes over.

## Editing map

- Copy: `index.html` (one `<section class="slide">` per screen)
- Recap questions: `QUESTIONS` array in `assets/js/main.js`
- Trainers (labeler, quadrant sort): `makeTrainer` configs in `main.js`
- Feedback Lab options: `SLOTS` array in `main.js`
- Facilitator runbook: `facilitator/notes.json`
- Publish: `git push origin main && git branch -f gh-pages main && git push -f origin gh-pages`
