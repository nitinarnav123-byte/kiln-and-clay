# Audit — round 2 (final)

## Technical audit
| # | Dimension     | Score | Key finding |
|---|---------------|-------|-------------|
| 1 | Accessibility | 4/4 | Labelled inputs, aria-live errors, focus-visible rings, one h1, alt text, ~12:1 body contrast, reduced-motion handled |
| 2 | Performance   | 4/4 | Hero eager + fetchpriority; below-fold lazy; dimensions set (no CLS); bounded effects; zero deps |
| 3 | Responsive    | 4/4 | Verified 375px: no horizontal overflow, CTA above fold, ≥44px inputs |
| 4 | Theming       | 4/4 | Full OKLCH token system, consistent; single dark theme is intentional (scene sentence) |
| 5 | Anti-patterns | 3/4 | Distinctive dark-stoneware direction dodges the cream cliché; 2 subtle P3 prose flags remain |
**Technical: 19/20**

## Design & heuristics
| # | Heuristic | Score |
|---|-----------|-------|
| 1 | Visibility of status | 4 |
| 2 | Match real world | 4 |
| 3 | User control/freedom | 3 |
| 4 | Consistency | 4 |
| 5 | Error prevention | 3 |
| 6 | Recognition > recall | 4 |
| 7 | Flexibility/efficiency | 3 (schedule "Book" prefills the form) |
| 8 | Aesthetic/minimalist | 4 |
| 9 | Error recovery | 3 |
| 10 | Help/docs | 3 |
**Design: 35/40**

## Slop test: PASS (both altitudes)
- First-order (guess palette from "ceramics studio"): would guess cream/beige — we shipped dark fired-stoneware + celadon. Dodged.
- Second-order ("artisan but not cream" → terracotta-everything): dodged; committed dark ground, one glaze accent.

## Severity counts: P0: 0   P1: 0   P2: 0   P3: 2

### P3 (non-blocking, documented)
- `aphoristic-cadence` (detector) — a few short punchy sentence fragments in body copy. Reads intentional for this warm voice; left as-is.
- `numbered-section-markers` (detector) — **false positive.** The 01/02/03 label one genuine ordered sequence (a class morning: start → make → fire), used once on the page. Impeccable's own rule exempts real sequences; this is voice, not scaffolding.

## Round trend: R1 ≈ 51 → R2 = 54 / 60  (Excellent band)
- R1 → R2 fixes: swapped Fraunces+Inter → Newsreader+Hanken Grotesk (cleared `overused-font`); removed em-dash overuse from body copy.

## Verdict: SHIP
Technical 19 ≥ 17 ✓ · Design 35 ≥ 32 ✓ · slop PASS ✓ · zero P0/P1 ✓

## Client to-dos before going live (flagged, not defects)
- Replace placeholder schedule, prices (€65/€120/€300), and Lisbon address with real values.
- Wire the booking form to a real endpoint (currently a validated client-side demo).
- Swap stock studio photos for real photos of Kiln & Clay + student work (strongest proof).
- Add Instagram/contact links in footer.
