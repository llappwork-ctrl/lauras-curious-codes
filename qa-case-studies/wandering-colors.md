# Wandering Colors: folder edit recolored other objects

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-007  
**Type** — Real development defect: shared CSS  
**Evidence status** — Partially documented

## Expected and observed behavior

Laura intended to recolor the case folder. The window and bookcase also turned purple after editing a shared rule.

## Laura's contribution

Laura inspected the stylesheet, located the separate .desk-folder rule, and corrected the mistake before ChatGPT supplied the diagnosis.

## AI collaboration

ChatGPT supported the surrounding learning session. The learning account explicitly distinguishes this independent correction from nearby AI-diagnosed mistakes.

## What connected the symptom to the cause

A selector can apply one style rule to several objects. Laura wanted only the folder to change color, so noticing the window and bookcase change too was evidence to inspect which elements the rule selected. The learning account says she found the separate `.desk-folder` rule before ChatGPT supplied the diagnosis.

## Correction and verification

L1 and L2 record the unexpected effects and Laura's correction. The exact offending diff and a named list of retested neighbors are missing.

## Evidence still missing

Before/after CSS diff and a specific regression test record.

## Scope and interpretation

Wandering Colors is the portfolio title for this recorded incident, not a second investigation.

## Sources

L1, section 14A; L2.

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-007) · [Back to QA Case Studies](README.md)
