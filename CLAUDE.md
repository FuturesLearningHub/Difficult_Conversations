# Navigating Difficult Conversations — Vanderbilt Learning Series

Single-page interactive classroom experience (Learning on Demand). Live at
https://me5231979.github.io/Difficult_Conversations/ (GitHub Pages, served
from the `gh-pages` branch — publish with
`git branch -f gh-pages main && git push -f origin gh-pages`).

Sister program: AI Basics (me5231979/AI_Classroom) — same engine, same
design system, same standing principles.

## Standing design principles (do not regress these)

1. **Simulators, practice, and play opportunities throughout.** Every
   teaching section lets the learner DO something: an interactive tool, a
   practice exercise, or a knowledge check. When adding a section, add its
   interaction.
2. **A reason and facilitation behind every activity.** Learner-visible
   "Why this matters" lines on every exercise; activities labeled
   **As a group** or **On your own** with numbered steps and timings.
3. **Every section facilitatable, learning validatable.** Per-section
   validation points (inline checks, tool completions, recap coverage).
   The ATD runbook lives in `facilitator/notes.json` (Say / Do / Ask with
   anticipated responses / Debrief / Transition + briefing front matter).
4. **Facilitator edition is generated, never hand-edited** — run
   `python3 tools/build-facilitator.py` after ANY change to index.html or
   notes.json. Its QR encodes the LEARNER url.
5. **Privacy by design.** This course touches real conflicts: the
   avoidance meter, BRAVING scorecard, and conversation plan are private,
   never collected, and the no-names norm (roles, not names) is stated on
   the welcome slide and enforced in the runbook.
6. **Brand: Vanderbilt FLH system.** Black #1C1C1C / white / flat gold
   #CFAE70; metallic gradient once or twice per page; Libre Caslon Display
   headlines (one italic word), Inter body, Antonio eyebrows; motion ≤400ms,
   engraved not bubbly; real VU lockups in assets/img (authorized use only).
7. **No frameworks.** One CSS file, one JS file, vendored QR lib,
   self-hosted fonts. Works offline except the hero montage (Higgsfield
   CDN, falls back to the particle canvas).

## Layout (17 slides)

Welcome/QR → Hero (objectives + montage) → Agenda →
01 Cost of avoiding (avoidance meter) → manifesto →
02 Three Conversations (labeler + Heen video) →
03 SBI (anatomy) → Feedback Lab (graded builder) →
04 STATE (anatomy + video) → 05 BRAVING (scorecard) →
06 Radical Candor (quadrant sort + video) → 07 First 30 seconds →
08 When it goes sideways → Recap quiz (scored) →
Capstone conversation plan → Glossary (flip cards) → Closing (commitment).

## Editing map

- Copy: `index.html` (one `<section class="slide">` per screen)
- Recap questions: `QUESTIONS` array in `assets/js/main.js`
- Inline checks: `.quiz` blocks with `data-correct`/`data-why` in index.html
- Trainers: `makeTrainer` configs in main.js; Lab: `SLOTS`; BRAVING: `ROWS`
- Facilitator runbook: `facilitator/notes.json` (timing must sum: Full 90 / Core 60)
- Source design doc: the course was built from a framework-mapped design
  (SHRM, McKinsey, ATD, Brown, Sinek, Crucial Conversations, Stone/Patton/
  Heen, Radical Candor, CCL) — keep citations honest when editing.
