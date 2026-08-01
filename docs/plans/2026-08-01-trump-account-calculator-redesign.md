# Trump Account Calculator — v2 Redesign

**Date:** 2026-08-01
**Status:** Approved

## Goal

Professionalize the existing single-file `index.html` calculator. Keep all functionality and math identical; replace the visual identity with a clean, modern **black / white / gold** theme, all sans-serif, with subtle American emoji accents.

## Palette

- Background: deep near-black (`#0a0a0a`), surfaces at slightly lighter blacks.
- Text: white / off-white; muted text in grays.
- Accent: gold (`#e7b94a` family) — the single brand accent.
- Borders/hairlines: white at low opacity.
- Chart: gold balance line with gradient area fill, white dashed contribution line.

## Typography

- Remove all Georgia/serif. Full sans-serif system stack.
- Heavy-weight headline (700–800), tabular numerals (`font-variant-numeric`).
- Uppercase, letter-spaced micro-labels for the data-led Fidelity feel.

## Components

- **Sliders:** thin (4px) track, gold fill on left, translucent track on right; clean white thumb with soft ring/shadow; larger hit area; gold focus ring.
- **Cards:** black gradients, hairline white/8 borders, larger radius (18px), subtle elevation.
- **Tabs:** segmented pill control — one soft container, gold pill for active tab.
- **Header:** emoji flag row (🇺🇸 ⭐ 🦅 ⭐ 🇺🇸) replaces drawn coins; tagline keeps "The American Dream starts now."
- **Breakdown bar:** rounded segments (white = your money, gold = growth) with percentage chips.
- **Chart:** smooth gold area chart (gradient fade to transparent), dashed white contribution line, glowing age dot. Sample at 6-month intervals for smoothness.
- **Polish:** transitions, `requestAnimationFrame`-throttled redraws, refined focus states, tightened spacing.

## Emoji usage (sparing, professional)

- Header: 🇺🇸 ⭐ 🦅 ⭐ 🇺🇸
- Tagline: ⭐
- Tax note: 🏛️
- Footer: 🦅 🇺🇸

## Constraints

- Single HTML file, zero dependencies, offline. Same math, self-test, and semantics.
