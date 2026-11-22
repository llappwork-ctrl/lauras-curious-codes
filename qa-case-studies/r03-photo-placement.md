# R03 photo positioned below its case sheet

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-010  
**Type** — Real development defect: visual placement  
**Evidence status** — Partially documented

## Expected and observed behavior

The approved soil photo should cover the incorrect photo printed on the case sheet. It appeared separately underneath.

## Laura's contribution

Laura reported the mismatch, personally located the positioning code, and adjusted the R03 photograph with guidance.

## AI collaboration

Codex explained relative and absolute positioning and supplied placement guidance.

## Correction and verification

L1 records Laura's adjustment. Commit 7660038 contains .r03-sheet and .r03-photo-overlay with percentage positioning.

## Evidence still missing

A specific post-adjustment screenshot or browser result and a resize regression test.

## Scope and interpretation

Different from QA-011, which concerns image loading.

## Sources

L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038); [overlay CSS](https://github.com/llappwork-ctrl/bug-detective-agency/blob/7660038/style.css).

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-010) · [Back to QA Case Studies](README.md)
