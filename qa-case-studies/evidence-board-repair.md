# Evidence Board Repair

**Project** — The Bug Detective Agency  
**Type** — Real development defect  
**Correction committed** — November 15, 2026  
**Evidence status** — Verified cause and committed correction, with a reported functional retest

## The problem

The Evidence Room should open successfully and display the existing Evidence Board. Pin controls should become available for discovered records.

Five additional pin controls had been added to the HTML, but their record definitions were missing from the board's JavaScript. When the board checked those controls, it attempted to read `.key` from an undefined value.

Codex reproduced this error during a repository review:

`Cannot read properties of undefined (reading 'key')`

The affected IDs were `case001`, `soilPhoto`, `receipt`, `case000`, and `fallPhoto`.

## My contribution

I reviewed the findings and chose to defer the five unfinished controls temporarily.

I required the correction to preserve their markup, artwork, planned functionality, and any saved layout data. I also kept the existing navigation controls available.

Using Codex's walkthrough, I edited the board code in VS Code and committed the correction. I later confirmed that the Evidence Board worked.

Codex identified the record mismatch. I did not independently diagnose the root cause.

## Root cause

The HTML contained ten pin controls, while `boardRecords` defined only R01–R05.

The board selected every element with `data-pin-record`, including hidden controls. Hiding a control did not prevent JavaScript from processing it.

The lookup assumed that every selected control had a matching record definition.

## Correction

The correction:

- Limits active pin controls to IDs defined in `boardRecords`.
- Holds unsupported saved records in a deferred list.
- Includes those deferred records when saving the layout again.

This allows the existing board to operate while retaining data for the unfinished features.

## Verification and its limits

**My browser verification** — I confirmed that the Evidence Board worked after the guided correction. The conversation does not contain a detailed checklist of every action I tested.

**Codex's checks** — Codex reported syntax checks and an in-memory simulation using a supported record, a loose magnet, and a deferred record. The simulated save retained the deferred record's data.

Those simulated checks are separate from my browser verification. A complete keyboard, responsive-layout, and persistence regression test is not documented.

## What this investigation taught me

An interface element can exist in HTML before the JavaScript needed to support it is complete. The connection between the control and its record definition must be checked.

I also practiced preserving saved user data while temporarily deferring unfinished functionality.

## Evidence

- [Correction commit — 03a9dfe](https://github.com/llappwork-ctrl/bug-detective-agency/commit/03a9dfe)
- [Board code at the correction commit](https://github.com/llappwork-ctrl/bug-detective-agency/blob/03a9dfe/evidence-board.js)
- Guided investigation, implementation, and acceptance recorded in the Codex conversation.

[Full investigation log entry](investigation-log.md#qa-015) · [Back to QA Case Studies](README.md)
