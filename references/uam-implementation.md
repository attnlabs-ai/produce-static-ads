# UAM implementation map

Verified against the source workspace on 2026-11-18. This repository contains **documentation only**. The commands below are a map for someone who separately has the current UAM implementation; cloning this repo does not install them, configure credentials or enable generation. Other assistants can follow SKILL.md with their own equivalent tools.

| Step | Source UAM component | Function |
|---|---|---|
| Draft concepts | `tools/creative-concept/concept-cards.js` | Draft and independently rank concepts with mechanism and copy map. |
| Approval bridge | `tools/creative-concept/card-to-uam.js` | Record actual owner approval; emit exact arguments; `--check` invokes preflight. |
| Locked copy | `tools/creative-copy/write-copy.js` | Ground, lint and rank copy; pass the selected text using `--copy-json`. |
| Generation | `tools/static-ad-generator/ultimate-ad-maker.js` | Reference-led native rendering or targeted full-image edit. |
| Durable execution | `scripts/creative-job-control.js` plus the environment's durable supervisor | Preserve owner, task receipts and paid-candidate state. |
| Product coverage | `product-truth-cards/pack-catalog.json` and multi-product truth inputs | Match every visible pack to official artwork and expected text. |
| Text first | `tools/creative-qa/pack-text-check.js` | Check pack words and locked copy before design review. |
| Punch list | `tools/creative-qa/carbon-review.js punchlist` | Save at most five reference-aware fixes with the same brief. |
| Verify | `tools/creative-qa/carbon-review.js verify` | Close the frozen list and identify regressions. |
| Blind comparison | `tools/creative-qa/carbon-review.js compare` | Compare exact old/new candidates against the source; retain the earlier one on a tie. |
| Slot state | `tools/static-ad-generator/slot-state.js` | Persist failure cause and accepted-candidate identity. |
| Delivery gate | `tools/creative-qa/delivery-gate.js` | Distinguish send, noted send and hold. |

## Current routing snapshot

The source adapter and machine-readable policy select KIE `gpt-image-2-6/flare-image-to-image` for reference input and the corresponding text-to-image route when no reference images are supplied. The current adapter supports native 3:4 and 4:5; explicit model/aspect contracts override defaults. Select the requested placement, not an arbitrary model's convenient ratio. Verify live provider prices, exact pixel output and capabilities before paying.

## Important boundaries

- `--dry-run` submits no image task, but its copy/rule check may use a paid text-model call.
- Pass every additional pack with an actual truth image, or use a clearly identified input truth sheet.
- A product-free concept uses `--no-product-visible`.
- One tracked candidate uses `--qa-retries 0`; edits count toward the four-candidate slot ceiling.
- `--surgical-edit-target` requests a targeted edit. It does not certify a true masked edit or guarantee every other pixel stays identical. Compare the complete output.
- Product/text safety, reference fidelity, creative acceptance, human approval and actual delivery are distinct checks.
- No command here authorizes client publication, ad activation, spend changes or sharing private assets.
