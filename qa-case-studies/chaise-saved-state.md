# Chaise already shifted and reload restoration

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-008  
**Type** — Saved-state investigation and related persistence correction  
**Evidence status** — Verified

## Expected and observed behavior

A repeat clue click seemed not to move the chaise because it was already shifted. A related persistence change restores the shifted class after reload.

## Laura's contribution

Laura checked the saved clue value, class membership, and computed transform in DevTools, then temporarily removed and restored the class and observed movement.

## AI collaboration

AI helped implement restoring the visual class from saved progress. The exact author of the initial restoration snippet is not established by the commit alone.

## Two related findings

The apparent movement failure was an investigation of a scene already in its completed state. Temporarily removing and restoring the class let Laura observe movement again. Separately, the committed persistence code reapplies the shifted class on page load when `begoniaClueFound` is saved. These findings share a state model, but the apparent no-op and the reload restoration are not counted as two independently diagnosed bugs.

## Correction and verification

L1 records the browser investigation. Commit 88bb7f4 adds restoration of chaise-shifted when begoniaClueFound is saved.

## Evidence still missing

A dated full before-clue, after-clue, and after-refresh test record.

## Scope and interpretation

The apparent non-movement was an already-completed state. Do not describe it as proof the movement handler failed.

## Sources

L1, section 18; [88bb7f4](https://github.com/llappwork-ctrl/bug-detective-agency/commit/88bb7f4); [restoration code](https://github.com/llappwork-ctrl/bug-detective-agency/blob/88bb7f4/script.js).

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-008) · [Back to QA Case Studies](README.md)
