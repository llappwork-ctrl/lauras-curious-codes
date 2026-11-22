# Flower lamp ignored its hidden starting state

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-005  
**Type** — Real development defect: CSS visibility  
**Evidence status** — Partially documented

## Expected and observed behavior

The orange flower lamp should begin hidden. Laura observed it remaining visible after adding hidden and suspected a conflicting display rule.

## Laura's contribution

Laura predicted the CSS interaction, tried display: auto, removed the display declaration, and verified that the lamp stayed hidden.

## AI collaboration

AI explained that display: auto is invalid. The diagnosis drew on earlier guidance and the Lingering Whisper exercise.

## Applying an earlier lesson

Laura had already investigated a CSS declaration overriding HTML's hidden state in Lingering Whisper. She recognized the same pattern when the flower lamp remained visible. Her experiment with `display: auto` is retained as part of the learning record; AI explained why that value was invalid. The recorded final action was removing the display declaration and checking that the lamp stayed hidden.

## Correction and verification

L1 records prediction, experiment, correction, and personal retest. Commit ef549d4 contains a flower-lamp rule without display: block, but it is not a recovered isolated fix.

## Evidence still missing

Original faulty rule, exact correction diff, and broader reset/reload test results.

## Scope and interpretation

Related to QA-002, but a separate real-game application.

## Sources

L1, sections 20 and 21; [ef549d4](https://github.com/llappwork-ctrl/bug-detective-agency/commit/ef549d4).

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-005) · [Back to QA Case Studies](README.md)
