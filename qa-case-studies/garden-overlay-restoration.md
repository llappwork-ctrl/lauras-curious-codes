# Garden butterflies and hand absent

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-013  
**Type** — Real development regression: missing markup  
**Evidence status** — Verified

## Expected and observed behavior

Collected records should change the garden. The saved HTML contained only the background, while overlay assets, CSS, and flag-reading logic remained.

## Laura's contribution

Laura reported the unchanged garden and missing hand and supplied Claude's earlier garden handoff.

## AI collaboration

Codex traced the missing elements, restored Claude's approved overlay positions, and reported simulated fresh, partial, all-five, and cleared-state checks.

## Correction and verification

C1 records the diagnosis and restoration. Commit 7660038 contains the restored garden structure; 46b4b9f later adds the reveal and another baseline butterfly.

## Evidence still missing

Laura's detailed post-restoration visual and keyboard retest.

## Scope and interpretation

The earlier restoration had seven butterflies. The later version has eight, so baseline counts must be tied to a version.

## Sources

L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038); [46b4b9f](https://github.com/llappwork-ctrl/bug-detective-agency/commit/46b4b9f).

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-013) · [Back to QA Case Studies](README.md)
