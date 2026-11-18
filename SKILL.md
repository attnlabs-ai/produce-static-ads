---
name: "produce-static-ads"
description: "Produce or revise reference-led static ads with complete product truth, exact copy, bounded paid attempts, targeted edits and independent acceptance checks."
---

# Produce Static Ads

Procedure synchronized with the UAM workflow on **2026-11-18**. This is a portable procedure, not the UAM executable, provider integration or client asset library. Production, owner approval and ad activation are separate states.

## 1. Establish the brief and authorization

Resolve the product, adult or other intended audience, one argument, current verified offer, approved copy, reference intent, placement/aspect, count, deadline and delivery route. Carry existing explicit authorization forward; do not ask again merely because a session changed. For new concepts, draft and rank before paid rendering and obtain the required human approval. Reference remakes preserve the selected structure, not a generic interpretation of the idea.

Apply each standing rule by its strength, condition and fit to this task. A default to vary backgrounds must not redesign a copy-only reskin. Do not turn a stylistic preference into a universal stop. Do not silently change factual rules or standing approval requirements. Ask only for a genuinely missing owner decision after preparing the reviewable work.

**Complete when:** each slot has a stable ID, the exact authorized scope, its source reference and an approved brief.

## 2. Name the reference mechanism and map every line

Bind the actual reference image to the slot. Preserve composition, focal order, subject positions, text-zone placement, text density, type hierarchy, whitespace, crop, lighting and native UI treatment as required by the brief. Target-brand typography and appropriate colors govern designed zones; native screenshot or handwriting mechanics remain native.

Every new concept carries:

- `mechanism`: one sentence naming the visible device that makes the source work.
- `copyMap`: `[{"zone":"…","text":"…","speaker":"optional"}]` for all on-image lines.
- `allowedChrome`: any necessary UI words, separate from ad copy.
- `mechanismTransfers`: false, with a plain `mechanismBlocker`, if the device needs an offer, price, product or proof that cannot be used.

Keep script labels and speaker names out of copy values. Place a speaker in the speaker field. Remove duplicated phrases, placeholders and invented badges. Discard unauthorized reference offers, testimonials, guarantees, ingredient props and competitor products. Preserve legitimate co-brand artwork when it is part of the target product.

Do not replace a price-led checkout, gift grid or sale mechanism with vague ingredient prose and call it faithful. Resolve the blocking factual permission or explicitly approve a different mechanism first.

**Complete when:** the source mechanism transfers truthfully and every approved line has one defined position.

## 3. Build complete, current product truth

Use current official product photos and a source-backed truth card. Verify exact SKU, pack form, count, dimensions where known, lid/open state, material, label artwork and all readable pack words. Refresh stale packaging against current official sources rather than blindly trusting cached assets.

The truth inputs must show **every distinct pack visible in the intended scene**. For multiple packs, use a truth sheet as the primary product input or pass each real pack as a clearly identified additional reference. State which image shows which pack. Do not describe an unseen second SKU. A single-pack brief must not receive an unsolicited second pack just because the truth sheet contains both.

Maintain a pack catalog with expected printed text and truth-image hashes where the receiving implementation supports it. For a product-free screenshot or text ad, explicitly declare that no product is visible. The layout reference must not become a substitute product authority. Do not fabricate testimonials, numbers, guarantees, discounts or efficacy.

**Complete when:** all intended packs and printed text are grounded in real images, with no conflicting alternate-SKU instructions.

## 4. Run a no-image-spend preflight

Verify real image bytes, useful resolution, current packaging, exact copy, approved concept, full product coverage, reference/brief consistency and remaining attempt budget. Validate that the actual provider supports the chosen model, aspect and edit mode. Explicit user choices override defaults; never silently substitute a model or ratio.

The current source UAM default is **GPT Image 2.6 Flare through KIE** (`gpt-image-2-6/flare-image-to-image` with references). Its current adapter lists native 3:4 and 4:5 support. This is a dated implementation snapshot, not a requirement to use that provider in every receiving environment. Verify live capabilities and pricing before paid submission. Use native output at the approved aspect; do not crop, pad or stretch to fake a native master. Exact pixel requirements remain separate from aspect requirements.

A dry run means **no image-generation spend**, not a promise of zero cost: a receiving implementation may call a paid text model for copy/rule checks. State what it checks and whether any model call occurs.

Stop for missing pack authority, unsupported mechanism, unapproved copy, placeholder or script-label copy, a critical rule violation, a from-scratch rerender of an accepted slot without a new owner instruction, an exhausted slot cap, or two consecutive same-cause failures without changed inputs. Keep one clean brief per candidate; do not append a history of repair instructions.

**Complete when:** the saved plan shows the exact inputs, model/aspect, copy, remaining attempts, expected output and costs/limits with no unresolved preflight error.

## 5. Render a bounded proof

Start with one or a small approved proof wave; each wave contains at most eight, with human review before the next wave. Set the total spend ceiling before submission. Use at most **four paid candidates per slot, including edits**, unless the owner explicitly changes that cap. When a slot runs out of candidates, stop and report it with its saved punch list. Do not request the same budget again without a changed plan. After **two consecutive failures for the same cause**, change a substantive input such as truth image, reference handling, mode or copy; changing explanatory prompt wording alone is not a new strategy.

Run paid batches in a durable job system with one honest owner, immutable slot IDs, persisted provider task IDs, checkpoints and terminal evidence. Never claim running from dispatch alone or resubmit business/provider actions merely to repair missing status delivery. In UAM, disable automatic image QA retries (`--qa-retries 0`) so each paid candidate is tracked separately.

Render the complete ad natively with the image model. Never paste or composite product photos, logos or text onto the finished ad. A reference sheet made from real input photos is allowed as an input, not as a finished ad.

**Complete when:** each submitted task has a receipt and a preserved native candidate, or an explicit known failure; unknown outcomes are reconciled before retries.

## 6. Check pack words and copy before design review

Read every visible pack against its official photo and expected text, at original resolution and by crop where needed. Transcribe approved overlay copy and check it appears once, in its assigned zone, with correct spelling and no missing, extra or repeated words. Case-only differences may be acceptable when authorized by the design contract.

A product-shaped object with the wrong label is not a pass. If a model reader is unavailable, inspect the actual crop yourself and record that limitation. An automated score never overrides a readable package error. A critical text failure goes straight to a targeted repair, not to a design reviewer who might average it away.

**Complete when:** pack text and approved copy are clean, with literal source-versus-output evidence.

## 7. Create one frozen punch list

Give an independent reviewer the **actual candidate, exact source reference, all official product truths and the same brief, including its prohibitions**. Ask for at most five concrete corrections, each with severity and whether it needs an edit or a composition rerender. Inspect the actual image yourself.

Freeze this first list. Later checks verify it rather than inventing a fresh redesign. Reject suggestions that contradict the authorized brief. Record any waiver: the alleged defect is absent on inspection, the brief forbids the suggestion, or a medium/low taste preference risks a correct asset. Do not waive a real high-severity fault for taste.

**Complete when:** a bounded punch list identifies exact defects and allowed repairs without moving the creative goalposts.

## 8. Repair by targeted edit first

For a wrong word, missing line or one wrong element, edit the existing candidate with one defect class per attempt. Supply truth images for **all packs still visible**, not just the pack being fixed. Recheck the whole image after the edit because the model may redraw frozen content.

A prompt saying “keep every other pixel unchanged” or a flag named “surgical” is not proof of a true masked or pixel-constrained edit. Use that capability when it exists and verify outside-zone drift. When the tool performs a full-image pass, disclose that fact and compare every preserved region. Never promise pixel identity that the tool does not establish.

Rerender from clean reference inputs only for a composition failure or after two targeted edits fail, within the total cap and changed-input rule. Do not switch to deterministic product/text assembly to escape a failed native render.

**Complete when:** the requested defect is corrected, pack/copy checks pass again and preserved content has been compared with the previous candidate.

## 9. Verify, compare and accept

Verify the frozen punch list against the repaired candidate and previous image. Check only which fixes are closed, any regression and any remaining client-rejection defect. For a slot with an existing best candidate, run a blind source-aware comparison. A polish edit of an accepted candidate must win outright, or the accepted one stays. Otherwise a win or tie satisfies comparison gate 5; on a tie keep the earlier candidate. All other acceptance gates must still pass. Never rerender an accepted candidate from scratch for polish without a new owner instruction.

Acceptance requires all five:

1. Every visible pack's printed words match the real pack.
2. Every approved copy line is exact and appears once.
3. No applicable mandatory rule is broken.
4. The punch list is closed with no new fault.
5. The candidate wins or ties the previous best in comparison, if one exists; retain the earlier candidate on a tie.

A reviewer score or “ready” flag is not the pass line. Technical acceptance is not human creative approval, a performance result or launch authorization.

**Complete when:** the exact candidate hash is accepted against all five gates, or the slot ends honestly with a saved blocker and remaining attempts.

## 10. Deliver verified files

Use the authorized delivery route and verify receipts for the exact files. Include native finals, a contact sheet when useful, source-versus-output comparisons for reference work and a manifest with IDs, hashes, dimensions, input truth, locked copy, provider/model, task IDs, attempt counts and QA state.

A delivery gate may say send, send with note or hold. Never deliver a hold as finished. If the owner asks to see drafts, label defects and review-only status clearly. Report requested, submitted, generated, technically accepted, human approved and delivered counts separately. A local file or successful process exit is not delivery proof.

**Complete when:** all promised outputs have delivery receipts, and unresolved failures are explicitly named. Keep credentials, private briefs, client assets, internal links and third-party reference files out of public packages.

## Working record and implementation notes

For each row retain: stable ID; current authorization; copy verbatim; mechanism and copy map; source and product paths/hashes; allowed changes; exact geometry; model/tool and task ID; cost limit and paid attempts; punch list; candidate hashes; independent checks; acceptance; human approval; delivery receipt; blocker and next action.

For a clearly labeled map to a separately installed UAM workspace, read [UAM implementation notes](references/uam-implementation.md). No script listed there is bundled in this repository.
