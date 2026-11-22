# QA Case Studies 🔎

These investigations come from The Bug Detective Agency, my hands-on coding and QA learning project.

Some are intentional challenges created by AI collaborators for me to investigate. Others are real development defects or usability problems encountered while building the game. Each write-up distinguishes my contribution from AI diagnosis, implementation, and reported tests.

## Complete investigation log

[Explore all 21 recovered investigation entries and leads](investigation-log.md). The log includes partial repairs, unresolved leads, related reports, and missing evidence. It is not a list of 21 successfully fixed bugs.

## Case studies

| Case study | Type | Evidence and limits |
|---|---|---|
| [Hesitant Signals](hesitant-signals.md) | Intentional QA challenge | Partially documented; see verification limits |
| [Lingering Whisper](lingering-whisper.md) | Intentional QA challenge | Partially documented; see verification limits |
| [Mystery 004: Case Files opens only once](mystery-004.md) | Intentional QA challenge | Verified diagnosis; correction and retest missing |
| [Flower lamp ignored its hidden starting state](flower-lamp-visibility.md) | Real development defect: CSS visibility | Partially documented; see verification limits |
| [Wandering Colors: folder edit recolored other objects](wandering-colors.md) | Real development defect: shared CSS | Partially documented; see verification limits |
| [Chaise already shifted and reload restoration](chaise-saved-state.md) | Saved-state investigation and related persistence correction | Verified; see verification limits |
| [R03 photo positioned below its case sheet](r03-photo-placement.md) | Real development defect: visual placement | Partially documented; see verification limits |
| [Evidence Index duplicate and misplaced controls](evidence-index-controls.md) | Real development defect: HTML and interaction | Verified; see verification limits |
| [Garden butterflies and hand absent](garden-overlay-restoration.md) | Real development regression: missing markup | Verified; see verification limits |
| [Opening lesson syntax errors and listener placement](opening-sequence-debugging.md) | Real development defects during guided editing | Verified; see verification limits |
| [Evidence Board unmatched record controls](evidence-board-repair.md) | Real development defect: data-definition mismatch | Verified committed repair; personal functional confirmation recorded |

## How I describe evidence

- **Verified** — Available code, history, or recorded observations support the specific claim. Verified diagnosis and verified correction are distinguished.
- **Partially documented** — A meaningful account exists, but important details such as the original diff, attribution, or test results are missing.
- **Needs recovery** — More evidence is required to establish the investigation's cause or outcome.

A status does not imply that every possible regression test passed. The [log's source records](investigation-log.md#source-records) explain the difference between committed code, author-held learning accounts, conversation reports, and retained exercise copies.

## Contributions and testing

My guided edits and browser observations are part of my learning experience. Each case study identifies when I independently found a problem, followed a walkthrough, or relied on AI diagnosis and checks. Missing evidence remains visible.

For the Evidence Board, Codex identified the record mismatch. I made guided corrections, committed the repair, and confirmed the board worked. A full keyboard, responsive, and persistence test checklist is not documented.

## Future additions

The remaining leads stay in the log until enough evidence is recovered for individual write-ups. Bridgeway QA experience may be considered later through a separate privacy and evidence review.

[Back to Laura's Curious Codes](../README.md)
