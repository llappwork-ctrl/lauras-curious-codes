# Opening lesson syntax errors and listener placement

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-014  
**Type** — Real development defects during guided editing  
**Evidence status** — Verified

## Expected and observed behavior

The script stopped with an illegal top-level return, then a duplicate const button declaration. A garden listener was also placed inside the function it was meant to activate.

## Laura's contribution

Laura edited in VS Code, reported the errors, and moved or removed the identified lines with exact guidance.

## AI collaboration

Codex reproduced the syntax errors and identified the listener placement. Codex provided the correction instructions.

## Correction and verification

C1 records the actual parser errors and follow-up inspection. Corrected code is preserved in 7660038. A complete browser pass for the opening sequence is unrecorded.

## Evidence still missing

Full browser regression results after the guided corrections.

## Scope and interpretation

Kept together as one opening-sequence editing episode rather than three independent case-study claims.

## Sources

L1, section 21; C1; [7660038](https://github.com/llappwork-ctrl/bug-detective-agency/commit/7660038).

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-014) · [Back to QA Case Studies](README.md)
