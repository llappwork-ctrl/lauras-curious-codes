# QA Investigation Log 🔎

**Project** — The Bug Detective Agency  
**Recovery reviewed** — November 22, 2026

This log preserves 21 investigation entries and leads recovered from code, Git history, learning records, and the portfolio-building conversation. They are not a count of 21 fixed bugs. Entries include intentional exercises, real development defects, a saved-state investigation, visual acceptance work, and incomplete leads.

Overlapping reports are cross-referenced below. Duplicate and misplaced Evidence Index controls share QA-012. The opening lesson's syntax and listener mistakes share QA-014. Early editing mistakes share QA-021. Mystery 003 and The Silent Spine remain one unconfirmed identity lead. R03 loading and R03 positioning remain separate because their symptoms differ; their relationship to the doubled-extension report is unproven.

## Evidence status

- **Verified** — Available code or history and recorded observations support the specific claim. The entry states which part is verified, such as diagnosis or committed correction. It does not imply every test passed.
- **Partially documented** — A meaningful account exists, with important before/after, attribution, commit, or retest details missing.
- **Needs recovery** — The available record cannot yet establish the investigation's cause or outcome.

Current inventory: 7 Verified, 10 Partially documented, and 4 Needs recovery. Code inspection during recovery is distinct from historical browser testing. The recovery process did not replay these investigations in a browser.

## Inventory

| ID | Investigation | Type | Evidence status | Detail |
|---|---|---|---|---|
| [QA-001](#qa-001) | Hesitant Signals | Intentional QA challenge | Partially documented | [Case study](hesitant-signals.md) |
| [QA-002](#qa-002) | Lingering Whisper | Intentional QA challenge | Partially documented | [Case study](lingering-whisper.md) |
| [QA-003](#qa-003) | Mystery 004: Case Files opens only once | Intentional QA challenge | Verified | [Case study](mystery-004.md) |
| [QA-004](#qa-004) | Mystery 003 and The Silent Spine recovery lead | Challenge identity and completion lead | Needs recovery | Recovery lead |
| [QA-005](#qa-005) | Flower lamp ignored its hidden starting state | Real development defect: CSS visibility | Partially documented | [Case study](flower-lamp-visibility.md) |
| [QA-006](#qa-006) | Image loading failed with a doubled extension | Real development defect: filename/path | Partially documented | Recovery lead |
| [QA-007](#qa-007) | Wandering Colors: folder edit recolored other objects | Real development defect: shared CSS | Partially documented | [Case study](wandering-colors.md) |
| [QA-008](#qa-008) | Chaise already shifted and reload restoration | Saved-state investigation and related persistence correction | Verified | [Case study](chaise-saved-state.md) |
| [QA-009](#qa-009) | Office layout conflicts and furniture overlaps | Real development regression: layout | Partially documented | Recovery lead |
| [QA-010](#qa-010) | R03 photo positioned below its case sheet | Real development defect: visual placement | Partially documented | [Case study](r03-photo-placement.md) |
| [QA-011](#qa-011) | R03 broken-image report | Real development defect: asset reference | Needs recovery | Recovery lead |
| [QA-012](#qa-012) | Evidence Index duplicate and misplaced controls | Real development defect: HTML and interaction | Verified | [Case study](evidence-index-controls.md) |
| [QA-013](#qa-013) | Garden butterflies and hand absent | Real development regression: missing markup | Verified | [Case study](garden-overlay-restoration.md) |
| [QA-014](#qa-014) | Opening lesson syntax errors and listener placement | Real development defects during guided editing | Verified | [Case study](opening-sequence-debugging.md) |
| [QA-015](#qa-015) | Evidence Board unmatched record controls | Real development defect: data-definition mismatch | Verified | [Case study](evidence-board-repair.md) |
| [QA-016](#qa-016) | Animated tea steam visually ineffective | Visual acceptance issue and feature retirement | Verified | Recovery lead |
| [QA-017](#qa-017) | R01 absent from collected evidence | Real development report: discovery/notebook integration | Needs recovery | Recovery lead |
| [QA-018](#qa-018) | Initial R02 reward failure | Real development investigation lead | Needs recovery | Recovery lead |
| [QA-019](#qa-019) | R05 displayed both a case sheet and a receipt | Real development defect: duplicate visual content | Partially documented | Recovery lead |
| [QA-020](#qa-020) | Large scenes made navigation difficult to reach | Real development report: responsive sizing and usability | Partially documented | Recovery lead |
| [QA-021](#qa-021) | Early duplicate IDs and CSS syntax mistakes | Guided markup and stylesheet corrections | Partially documented | Recovery lead |

## QA-001

**Hesitant Signals**  
**Type** — Intentional QA challenge  
**Evidence status** — Partially documented

**Problem investigated** — The Case Files panel, its button wording, and aria-expanded should agree after a click. They disagreed because the open state was calculated before the panel was toggled.

**Laura's contribution** — Laura used DevTools and hints, worked through the correction, and checked that the label and accessibility attribute matched the resulting state.

**AI collaborator contribution** — AI guidance is recorded. The available account does not reliably identify the challenge author or reproduce the exact hints.

**Correction and testing evidence** — The retained mystery-001 script toggles the panel before calculating isOpen. The learning account records correction and checking. No separate fix commit, original faulty snapshot, or detailed regression checklist was recovered.

**Supporting sources** — Learning record L1, section 18; exercise record E1.

**Missing evidence** — Original broken snippet, exact assistance, dated test steps, and a correction commit.

**Overlap and scope** — The practice Case #001 is distinct from the game's story Case #001.

[Read the case study](hesitant-signals.md)

## QA-002

**Lingering Whisper**  
**Type** — Intentional QA challenge  
**Evidence status** — Partially documented

**Problem investigated** — Mabel's dialogue should follow its hidden state. A display: block declaration kept it visible.

**Laura's contribution** — Laura investigated HTML, JavaScript, and CSS, temporarily disabled the declaration, observed the result, and removed it. The learning record says she applied the lesson in the real game.

**AI collaborator contribution** — The exercise was AI assisted. Exact hint wording and the individual challenge author were not recovered.

**Correction and testing evidence** — The current mystery-002 dialogue rule has no display declaration. L1 records the temporary experiment and correction. A distinct fix commit and original faulty version are missing.

**Supporting sources** — L1, section 18; E2.

**Missing evidence** — Original faulty CSS, correction date, and detailed keyboard or neighboring-feature retests.

**Overlap and scope** — QA-005 applies this same CSS visibility lesson to a different object.

[Read the case study](lingering-whisper.md)

## QA-003

**Mystery 004: Case Files opens only once**  
**Type** — Intentional QA challenge  
**Evidence status** — Verified

**Problem investigated** — The Case Files button should reopen after closing. The stored challenge uses { once: true }, which removes the opening listener after its first activation.

**Laura's contribution** — Laura identified { once: true } without hints and explicitly celebrated finding it in the conversation.

**AI collaborator contribution** — Codex planted the exercise. The technical explanation and later evidence recovery were AI assisted.

**Correction and testing evidence** — The retained mystery-004 script still contains the planted option. L1 and the conversation support Laura's independent diagnosis. No completed correction or retest is documented.

**Supporting sources** — L1, section 21; E4; conversation C1.

**Missing evidence** — Evidence of removing the option and retesting repeated opening and closing. No Git history exists in the challenge directory.

**Overlap and scope** — Verified applies to the stored cause and documented diagnosis. It does not mean the challenge was fixed.

[Read the case study](mystery-004.md)

## QA-004

**Mystery 003 and The Silent Spine recovery lead**  
**Type** — Challenge identity and completion lead  
**Evidence status** — Needs recovery

**Problem investigated** — A mystery-003 exercise directory, a pre-exercise recovery snapshot, and a separate training copy titled The Silent Spine exist. Their relationship and investigation outcome are unconfirmed.

**Laura's contribution** — No specific diagnosis, correction, or retest can be attributed to Laura from the recovered records.

**AI collaborator contribution** — AI assistance or challenge preparation may be involved, but the available evidence does not establish its exact contribution.

**Correction and testing evidence** — Existence of exercise and recovery copies is established. No completed investigation account was recovered.

**Supporting sources** — E3; recovery snapshot R1.

**Missing evidence** — Challenge title mapping, expected failure, completion status, and test record.

**Overlap and scope** — Grouped as one recovery lead to avoid counting two copies as two completed investigations. Any still-active hidden solution is omitted.

## QA-005

**Flower lamp ignored its hidden starting state**  
**Type** — Real development defect: CSS visibility  
**Evidence status** — Partially documented

**Problem investigated** — The orange flower lamp should begin hidden. Laura observed it remaining visible after adding hidden and suspected a conflicting display rule.

**Laura's contribution** — Laura predicted the CSS interaction, tried display: auto, removed the display declaration, and verified that the lamp stayed hidden.

**AI collaborator contribution** — AI explained that display: auto is invalid. The diagnosis drew on earlier guidance and the Lingering Whisper exercise.

**Correction and testing evidence** — L1 records prediction, experiment, correction, and personal retest. Commit ef549d4 contains a flower-lamp rule without display: block, but it is not a recovered isolated fix.

**Supporting sources** — L1, sections 20 and 21; [ef549d4](https://github.com/llappwork-ctrl/bug-detective-agency/commit/ef549d4).

**Missing evidence** — Original faulty rule, exact correction diff, and broader reset/reload test results.

**Overlap and scope** — Related to QA-002, but a separate real-game application.

[Read the case study](flower-lamp-visibility.md)

## QA-006

**Image loading failed with a doubled extension**  
**Type** — Real development defect: filename/path  
**Evidence status** — Partially documented

**Problem investigated** — An illustration failed to load because the referenced filename had a doubled .png extension.

**Laura's contribution** — The learning account credits Laura with finding and correcting the filename issue and distinguishing it from opacity, container styling, and placement.

**AI collaborator contribution** — Illustrations and broader integration were AI assisted. The record does not establish who suggested each troubleshooting step.

**Correction and testing evidence** — L1 records the personal finding and correction. The exact asset, faulty path, correction commit, and explicit post-fix reload result were not recovered.

**Supporting sources** — L1, section 18.

**Missing evidence** — Exact affected asset, before/after reference, and test evidence.

**Overlap and scope** — Do not merge with QA-011 unless the original references show they were the same incident.

## QA-007

**Wandering Colors: folder edit recolored other objects**  
**Type** — Real development defect: shared CSS  
**Evidence status** — Partially documented

**Problem investigated** — Laura intended to recolor the case folder. The window and bookcase also turned purple after editing a shared rule.

**Laura's contribution** — Laura inspected the stylesheet, located the separate .desk-folder rule, and corrected the mistake before ChatGPT supplied the diagnosis.

**AI collaborator contribution** — ChatGPT supported the surrounding learning session. The learning account explicitly distinguishes this independent correction from nearby AI-diagnosed mistakes.

**Correction and testing evidence** — L1 and L2 record the unexpected effects and Laura's correction. The exact offending diff and a named list of retested neighbors are missing.

**Supporting sources** — L1, section 14A; L2.

**Missing evidence** — Before/after CSS diff and a specific regression test record.

**Overlap and scope** — Wandering Colors is the portfolio title for this recorded incident, not a second investigation.

[Read the case study](wandering-colors.md)

## QA-008

**Chaise already shifted and reload restoration**  
**Type** — Saved-state investigation and related persistence correction  
**Evidence status** — Verified

**Problem investigated** — A repeat clue click seemed not to move the chaise because it was already shifted. A related persistence change restores the shifted class after reload.

**Laura's contribution** — Laura checked the saved clue value, class membership, and computed transform in DevTools, then temporarily removed and restored the class and observed movement.

**AI collaborator contribution** — AI helped implement restoring the visual class from saved progress. The exact author of the initial restoration snippet is not established by the commit alone.

**Correction and testing evidence** — L1 records the browser investigation. Commit 88bb7f4 adds restoration of chaise-shifted when begoniaClueFound is saved.

**Supporting sources** — L1, section 18; [88bb7f4](https://github.com/llappwork-ctrl/bug-detective-agency/commit/88bb7f4); [restoration code](https://github.com/llappwork-ctrl/bug-detective-agency/blob/88bb7f4/script.js).

**Missing evidence** — A dated full before-clue, after-clue, and after-refresh test record.

**Overlap and scope** — The apparent non-movement was an already-completed state. Do not describe it as proof the movement handler failed.

[Read the case study](chaise-saved-state.md)

## QA-009

**Office layout conflicts and furniture overlaps**  
**Type** — Real development regression: layout  
**Evidence status** — Partially documented

**Problem investigated** — Repeated coordinate changes led to furniture overlaps and conflicting placement. Claude reported malformed or conflicting selectors, duplicate overrides, and percentage/fixed-size mismatches.

**Laura's contribution** — Laura observed the layout problems, stopped changing coordinates, requested a bounded inspection, and browser-reviewed the repair.

**AI collaborator contribution** — Claude diagnosed, repaired, and reported testing the layout. Laura's report of the symptoms is distinct from Claude's technical diagnosis.

**Correction and testing evidence** — L1 records the repair and acceptance. Recovery snapshots preserve earlier layouts, and 88bb7f4 contains a substantial layout update. Exact defect-to-hunk mapping is incomplete.

**Supporting sources** — L1, section 18; R1; [88bb7f4](https://github.com/llappwork-ctrl/bug-detective-agency/commit/88bb7f4).

**Missing evidence** — Original repair report, individually mapped selectors, and exact regression checklist.

**Overlap and scope** — Broader layout episode; the R03 and later garden incidents have their own entries.

## QA-010

**R03 photo positioned below its case sheet**  
**Type** — Real development defect: visual placement  
**Evidence status** — Partially documented

**Problem investigated** — The approved soil photo should cover the incorrect photo printed on the case sheet. It appeared separately underneath.

**Laura's contribution** — Laura reported the mismatch, personally located the positioning code, and adjusted the R03 photograph with guidance.

**AI collaborator contribution** — Codex explained relative and absolute positioning and supplied placement guidance.

**Correction and testing evidence** — L1 records Laura's adjustment. Commit 7660038 contains .r03-sheet and .r03-photo-overlay with percentage positioning.

**Supporting sources** — L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038); [overlay CSS](https://github.com/llappwork-ctrl/bug-detective-agency/blob/7660038/style.css).

**Missing evidence** — A specific post-adjustment screenshot or browser result and a resize regression test.

**Overlap and scope** — Different from QA-011, which concerns image loading.

[Read the case study](r03-photo-placement.md)

## QA-011

**R03 broken-image report**  
**Type** — Real development defect: asset reference  
**Evidence status** — Needs recovery

**Problem investigated** — Laura supplied a screenshot showing the R03 photograph failing to load, leaving a broken-image icon and alt text.

**Laura's contribution** — Laura noticed the failed image and supplied visual evidence.

**AI collaborator contribution** — Codex later integrated the approved soil photograph. The original diagnostic response was not recovered.

**Correction and testing evidence** — Commit 7660038 contains R03 East Begonia Bed - Approved.png and its HTML reference. The exact earlier broken reference is unavailable.

**Supporting sources** — C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038).

**Missing evidence** — Original bad path, exact root cause, and post-fix image-loading test.

**Overlap and scope** — Keep separate from QA-006 and QA-010 until evidence proves overlap.

## QA-012

**Evidence Index duplicate and misplaced controls**  
**Type** — Real development defect: HTML and interaction  
**Evidence status** — Verified

**Problem investigated** — Printed record names should be the interactive targets. Laura observed duplicate R01/R02 controls beneath the artwork and misplaced controls over the index.

**Laura's contribution** — Laura reported the unwanted layout with screenshots and requested clickable printed names.

**AI collaborator contribution** — Codex identified duplicate markup and IDs, removed redundant controls, restored transparent R01-R05 targets, and reported ID and syntax checks.

**Correction and testing evidence** — The repair is preserved in commit 7660038. The conversation records the observed symptoms and the edit. A complete keyboard or resize retest is not documented.

**Supporting sources** — L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038); [index HTML](https://github.com/llappwork-ctrl/bug-detective-agency/blob/7660038/index.html).

**Missing evidence** — Documented mouse, keyboard, and resizing regression results.

**Overlap and scope** — Grouped the duplicate-control and misplaced-target reports as one index repair episode. Later photo-index wiring is a separate unfinished feature.

[Read the case study](evidence-index-controls.md)

## QA-013

**Garden butterflies and hand absent**  
**Type** — Real development regression: missing markup  
**Evidence status** — Verified

**Problem investigated** — Collected records should change the garden. The saved HTML contained only the background, while overlay assets, CSS, and flag-reading logic remained.

**Laura's contribution** — Laura reported the unchanged garden and missing hand and supplied Claude's earlier garden handoff.

**AI collaborator contribution** — Codex traced the missing elements, restored Claude's approved overlay positions, and reported simulated fresh, partial, all-five, and cleared-state checks.

**Correction and testing evidence** — C1 records the diagnosis and restoration. Commit 7660038 contains the restored garden structure; 46b4b9f later adds the reveal and another baseline butterfly.

**Supporting sources** — L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038); [46b4b9f](https://github.com/llappwork-ctrl/bug-detective-agency/commit/46b4b9f).

**Missing evidence** — Laura's detailed post-restoration visual and keyboard retest.

**Overlap and scope** — The earlier restoration had seven butterflies. The later version has eight, so baseline counts must be tied to a version.

[Read the case study](garden-overlay-restoration.md)

## QA-014

**Opening lesson syntax errors and listener placement**  
**Type** — Real development defects during guided editing  
**Evidence status** — Verified

**Problem investigated** — The script stopped with an illegal top-level return, then a duplicate const button declaration. A garden listener was also placed inside the function it was meant to activate.

**Laura's contribution** — Laura edited in VS Code, reported the errors, and moved or removed the identified lines with exact guidance.

**AI collaborator contribution** — Codex reproduced the syntax errors and identified the listener placement. Codex provided the correction instructions.

**Correction and testing evidence** — C1 records the actual parser errors and follow-up inspection. Corrected code is preserved in 7660038. A complete browser pass for the opening sequence is unrecorded.

**Supporting sources** — L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038).

**Missing evidence** — Full browser regression results after the guided corrections.

**Overlap and scope** — Kept together as one opening-sequence editing episode rather than three independent case-study claims.

[Read the case study](opening-sequence-debugging.md)

## QA-015

**Evidence Board unmatched record controls**  
**Type** — Real development defect: data-definition mismatch  
**Evidence status** — Verified

**Problem investigated** — The board checked ten pin controls, but boardRecords defined only R01-R05. The five unmatched controls caused a read of .key on undefined.

**Laura's contribution** — Laura selected temporary deferral, required data preservation, made guided edits in VS Code, committed the correction, and later confirmed the board worked.

**AI collaborator contribution** — Codex identified and reproduced the mismatch, supplied the walkthrough, and reported an in-memory supported-card, loose-magnet, and deferred-card save simulation.

**Correction and testing evidence** — Commit 03a9dfe filters supported controls, holds unknown saved records separately, and includes them in later saves. C1 contains Laura's functional confirmation.

**Supporting sources** — C1; [03a9dfe](https://github.com/llappwork-ctrl/bug-detective-agency/commit/03a9dfe); [board code](https://github.com/llappwork-ctrl/bug-detective-agency/blob/03a9dfe/evidence-board.js).

**Missing evidence** — A detailed personal keyboard, responsive, and persistence regression checklist.

**Overlap and scope** — The deferred controls retain planned functionality. This is the existing case study.

[Read the case study](evidence-board-repair.md)

## QA-016

**Animated tea steam visually ineffective**  
**Type** — Visual acceptance issue and feature retirement  
**Evidence status** — Verified

**Problem investigated** — The added steam did not produce the intended visible effect against the steam painted into the desk artwork.

**Laura's contribution** — Laura reported dissatisfaction and chose to remove the animated steam after a dependency check.

**AI collaborator contribution** — Codex removed the steam markup, styles, and reward reference and reported simulated checks of the remaining R02 plant/table conditions.

**Correction and testing evidence** — Commit 46b4b9f removes the animation. The record does not establish whether the original animation failed technically or was obscured by the artwork.

**Supporting sources** — C1; [46b4b9f](https://github.com/llappwork-ctrl/bug-detective-agency/commit/46b4b9f).

**Missing evidence** — Original computed animation state and a specific final visual retest.

**Overlap and scope** — A verified acceptance decision and retirement, not a claim that the animation's original failure was fully diagnosed.

## QA-017

**R01 absent from collected evidence**  
**Type** — Real development report: discovery/notebook integration  
**Evidence status** — Needs recovery

**Problem investigated** — Laura repeatedly reported that R01 did not appear in collected evidence while adding it alongside R02.

**Laura's contribution** — Laura attempted the edits, reported the missing entry, and requested code checks.

**AI collaborator contribution** — Guidance and review were AI assisted. The exact diagnosis for each reported failure is not present.

**Correction and testing evidence** — Commit 88195ce adds R01 discovery, notebook visibility, reset, and reopening support. This does not establish the cause of every later report.

**Supporting sources** — C1; [88195ce](https://github.com/llappwork-ctrl/bug-detective-agency/commit/88195ce).

**Missing evidence** — Exact faulty version, final correction, and personally documented discovery/reopening retest.

**Overlap and scope** — Scope or placement concerns in a screenshot are not enough to establish a confirmed root cause.

## QA-018

**Initial R02 reward failure**  
**Type** — Real development investigation lead  
**Evidence status** — Needs recovery

**Problem investigated** — An early report asked why R02 steam and plant rewards were not behaving correctly, including after refresh and reset.

**Laura's contribution** — Laura requested an independent investigation and later said she corrected the reward JavaScript using its findings.

**AI collaborator contribution** — The original inspection and correction guidance were AI assisted, but the full diagnostic response is absent.

**Correction and testing evidence** — C1 includes the investigation request and the later account of a correction. Commit de049a0 contains reward code, but a faulty-to-fixed pair is not recovered.

**Supporting sources** — C1; [de049a0](https://github.com/llappwork-ctrl/bug-detective-agency/commit/de049a0).

**Missing evidence** — Faulty function, established root cause, actual correction diff, and test results.

**Overlap and scope** — Recursion, startup calls, and hidden-state conflicts were questions to investigate, not confirmed causes. Distinct from QA-016.

## QA-019

**R05 displayed both a case sheet and a receipt**  
**Type** — Real development defect: duplicate visual content  
**Evidence status** — Partially documented

**Problem investigated** — Laura wanted the actual delivery-slip copy. The pop-up displayed an additional outdated case sheet above it.

**Laura's contribution** — Laura supplied a screenshot, identified the unwanted top image, and requested receipt-only display.

**AI collaborator contribution** — Codex removed the case-sheet image and adjusted the accessible transcript to describe the retained receipt.

**Correction and testing evidence** — Commit 7660038 preserves the receipt-only R05 markup. No specific post-removal browser retest was recorded.

**Supporting sources** — C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038).

**Missing evidence** — Explicit receipt-only browser acceptance and sizing/keyboard checks.

**Overlap and scope** — This display decision does not change R05 discovery or settle unrelated story details.

## QA-020

**Large scenes made navigation difficult to reach**  
**Type** — Real development report: responsive sizing and usability  
**Evidence status** — Partially documented

**Problem investigated** — The Office and Garden could fill most of a desktop window, requiring scrolling to reach controls.

**Laura's contribution** — Laura supplied screenshots, described navigation being cut off or inconvenient, and selected a viewport-fit goal. A later screenshot showed the garden fitting while the Office remained large.

**AI collaborator contribution** — Codex inspected full-width aspect-ratio sizing and supplied a desktop garden sizing lesson using min(), calc(), and dvh.

**Correction and testing evidence** — Commit 46b4b9f contains the garden height-budget rule. Office/shared-navigation cleanup remained unfinished at review.

**Supporting sources** — C1; [46b4b9f](https://github.com/llappwork-ctrl/bug-detective-agency/commit/46b4b9f).

**Missing evidence** — A complete multi-scene, mobile, zoom, and keyboard regression record.

**Overlap and scope** — Documented as partial improvement rather than a completed shared-layout redesign.

## QA-021

**Early duplicate IDs and CSS syntax mistakes**  
**Type** — Guided markup and stylesheet corrections  
**Evidence status** — Partially documented

**Problem investigated** — Early editing introduced missing/extra CSS braces, duplicate Case File IDs, nested duplicate window IDs, and a stray character.

**Laura's contribution** — The learning records say Laura made guided corrections and browser-tested them.

**AI collaborator contribution** — ChatGPT identified these mistakes. The records explicitly distinguish them from Laura's independent Wandering Colors diagnosis.

**Correction and testing evidence** — L1 and L2 document the corrections. Commit 65d71cf is titled as removing a duplicate, but its resulting HTML still contains two case-file-button IDs. The title cannot serve as proof of resolution.

**Supporting sources** — L1, section 14A; L2; [65d71cf](https://github.com/llappwork-ctrl/bug-detective-agency/commit/65d71cf).

**Missing evidence** — Exact final corrective commits and per-defect before/after evidence.

**Overlap and scope** — Grouped early editing issues remain a recovery lead. Distinct from the later index duplicates (QA-012) and opening syntax episode (QA-014).

## Source records

Public code links point to specific commits where possible, because current files evolve. A commit confirms what was saved, not who personally diagnosed a defect or what browser tests were performed. Learning accounts and conversation records supply attribution and reported observations.

- **L1** — AI and Coding Learning Notebook, November 14, 2026 edition. Relevant sections are 14A (early CSS and markup), 18 (illustrated Office, saved state, Hesitant Signals and Lingering Whisper), 20 (flower lamp), and 21 (Mystery 004, R03, index, garden, and opening lesson). This is an author-held secondary account. Its unrelated project content is not reproduced or linked publicly.
- **L2** — Claude/Laura Learning Handoff, October 27, 2026. The author-held account distinguishes Laura's independent shared-selector correction from ChatGPT-diagnosed braces and duplicate IDs. It is not a public test artifact.
- **C1** — The Bug Detective Agency / Laura's Curious Codes Codex conversation available during recovery. It contains Laura's reports and screenshots, AI inspection findings, guided edits, and later acceptance statements. Full private chat history is not published here. AI-reported tests remain labeled as such.
- **E1, E2, E3, E4** — Local isolated challenge copies named mystery-001 through mystery-004. Their containing directory has no recovered Git history. E1 and E2 retain corrected-looking code; E4 still contains the one-use listener. File state alone cannot prove the full sequence of a learner's actions.
- **R1** — Author-held Bug Detective recovery snapshots from November 1–6, 2026, including a pre-Mystery-003 copy and earlier layout copies. Snapshot existence is supporting context, not proof of completion or acceptance.
- **Public game history** — [Repository](https://github.com/llappwork-ctrl/bug-detective-agency), including [88bb7f4](https://github.com/llappwork-ctrl/bug-detective-agency/commit/88bb7f4), [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038), [03a9dfe](https://github.com/llappwork-ctrl/bug-detective-agency/commit/03a9dfe), and [46b4b9f](https://github.com/llappwork-ctrl/bug-detective-agency/commit/46b4b9f). QA-021 records why the message on 65d71cf is insufficient by itself.

The practice names Hesitant Signals and Lingering Whisper are separate from the story's Case #000 and Case #001. A fictional record or story case is not itself evidence that a software investigation was completed.

## Recovery priorities

For Mystery 004, recover a correction and repeated-open retest. For Wandering Colors and the flower lamp, recover exact before/after CSS. For R03, recover both the original bad image path and a post-placement screenshot. For the completed board repair, add a dated personal regression checklist if one exists. A future test can add current evidence, but cannot be presented as a historical test.

Bridgeway QA experience is a possible future portfolio addition after a separate review. This log covers The Bug Detective Agency; private code, security details, and internal records from other projects are excluded.

[Back to QA Case Studies](README.md) · [Back to Laura's Curious Codes](../README.md)
