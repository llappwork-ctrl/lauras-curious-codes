# Hesitant Signals

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-001  
**Type** — Intentional QA challenge  
**Evidence status** — Partially documented

## Expected and observed behavior

The Case Files panel, its button wording, and aria-expanded should agree after a click. They disagreed because the open state was calculated before the panel was toggled.

## Laura's contribution

Laura used DevTools and hints, worked through the correction, and checked that the label and accessibility attribute matched the resulting state.

## AI collaboration

AI guidance is recorded. The available account does not reliably identify the challenge author or reproduce the exact hints.

## Correction and verification

The retained mystery-001 script toggles the panel before calculating isOpen. The learning account records correction and checking. No separate fix commit, original faulty snapshot, or detailed regression checklist was recovered.

## Evidence still missing

Original broken snippet, exact assistance, dated test steps, and a correction commit.

## Scope and interpretation

The practice Case #001 is distinct from the game's story Case #001.

## Sources

Learning record L1, section 18; exercise record E1.

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-001) · [Back to QA Case Studies](README.md)
