# Changelog

## Stage 00 — Brief Architect
Froze spec.md. Greenfield one-pager → single index.html. Flagged 4 `[assumed]` items (price, schedule, endpoint, address) for the client.

## Stage 01 — Reference Scout
Register = brand. Ran per-industry research; identified the cream/beige + hands-on-wheel cliché and banned it. Chose committed dark fired-stoneware palette + celadon glaze accent. Signature move: hand-thrown SVG divider + glaze-sheen CTA. Wrote references.md. (Gate skipped via --auto.)

## Stages 02–06 — Design/Copy/CTA/Engineering/Media
Built index.html: OKLCH token system; Newsreader/Hanken type; hero with value + CTA above fold; 3-step "what it's like"; schedule with seat scarcity; ≤3 pricing tiers; validated booking form with success state + schedule-row prefill; 5 verified Unsplash images (1 candidate rejected on a 404 during URL verification), lazy-loaded with alt + dimensions.

## Stage 07 — Responsive
Verified in-browser at 375px: no horizontal overflow (doc width = viewport), CTA above fold, ≥44px targets, images loaded.

## Stage 08 — Standards
a11y: labels, aria-live errors, focus-visible, semantic landmarks, reduced-motion. SEO: title/description/canonical/OG/Twitter, one h1. Perf: lazy/eager split, dimensions, no deps.

## Stage 09 — Auditor
Round 1: detector flagged overused-font (Fraunces+Inter) + em-dash overuse → fixed in place (font swap, copy de-dashed). Round 2: 54/60, zero P0/P1, slop PASS → SHIP. Two P3s documented (one a false positive). See audit.md.
