# Mystery 004: Case Files opens only once

**Project** — The Bug Detective Agency  
**Investigation ID** — QA-003  
**Type** — Intentional QA challenge  
**Evidence status** — Verified

## Expected and observed behavior

The Case Files button should reopen after closing. The stored challenge uses { once: true }, which removes the opening listener after its first activation.

## Laura's contribution

Laura identified { once: true } without hints and explicitly celebrated finding it in the conversation.

## AI collaboration

Codex planted the exercise. The technical explanation and later evidence recovery were AI assisted.

## The specific finding

The stored challenge includes this listener option:

```js
{ once: true }
```

It makes the listener run once. Removing it is the candidate correction, but the retained exercise still has it. This case study records an independent diagnosis, not a completed repair. Repeated opening, closing, and keyboard retesting would be new evidence if performed later.

## Correction and verification

The retained mystery-004 script still contains the planted option. L1 and the conversation support Laura's independent diagnosis. No completed correction or retest is documented.

## Evidence still missing

Evidence of removing the option and retesting repeated opening and closing. No Git history exists in the challenge directory.

## Scope and interpretation

Verified applies to the stored cause and documented diagnosis. It does not mean the challenge was fixed.

## Sources

L1, section 21; E4; conversation C1.

Source identifiers refer to the [source records in the investigation log](investigation-log.md#source-records). Historical browser observations and AI-reported checks are attributed separately. This documentation recovery did not perform a new browser retest.

[Full inventory entry](investigation-log.md#qa-003) · [Back to QA Case Studies](README.md)
