# Evidence Index duplicate and misplaced controls

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-012  
**Type** — Real development defect: HTML and interaction  
**Evidence status** — Verified

## Expected and observed behavior

Printed record names should be the interactive targets. Laura observed duplicate R01/R02 controls beneath the artwork and misplaced controls over the index.

## Laura's contribution

Laura reported the unwanted layout with screenshots and requested clickable printed names.

## AI collaboration

Codex identified duplicate markup and IDs, removed redundant controls, restored transparent R01-R05 targets, and reported ID and syntax checks.

## Correction and verification

The repair is preserved in commit 7660038. The conversation records the observed symptoms and the edit. A complete keyboard or resize retest is not documented.

## Evidence still missing

Documented mouse, keyboard, and resizing regression results.

## Scope and interpretation

Grouped the duplicate-control and misplaced-target reports as one index repair episode. Later photo-index wiring is a separate unfinished feature.

## Sources

L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038); [index HTML](https://github.com/llappwork-ctrl/bug-detective-agency/blob/7660038/index.html).

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-012) · [Back to QA Case Studies](README.md)
