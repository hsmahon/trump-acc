# Trump Account Calculator Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** A single-file, offline `index.html` web page that models the real U.S. Trump Accounts program — $1,000 Treasury seed, up to $5,000/yr parental contributions, S&P 500-style returns, maturing at age 18 — for a teen.

**Architecture:** One self-contained HTML file with embedded CSS and vanilla JS. Core math in a pure `futureValue(start, annualContribution, ratePct, months)` function, verified by a built-in console self-test. A `<canvas>` renders the year-by-year balance vs. contributions chart. No libraries, no CDN, no build tools.

**Tech Stack:** HTML5, CSS3, vanilla JS, HTML5 Canvas.

---

### Task 1: Scaffold `index.html` shell

**Files:**
- Create: `index.html`

**Step 1:** Write the structural skeleton: banner header ("The American Dream starts now."), three input sliders (government seed, annual contribution, expected return), three timeline tab buttons (18/27/55), headline result area, breakdown bar, `<canvas>`, tax-advantage note, and an empty `<script>` at the end of `<body>`.

**Step 2:** Open in a browser; confirm the layout renders.

**Step 3:** Commit: `git add index.html && git commit -m "chore: scaffold single-file app shell"`

---

### Task 2: Core math + self-test

**Files:**
- Modify: `index.html` (script block)

**Step 1:** Add `futureValue(start, annual, ratePct, months)` with monthly compounding.

**Step 2:** Add `selfTest()` asserting (tolerance ±$0.50):
- `futureValue(0, 0, 0, 120) === 0`
- `futureValue(1000, 0, 0, 120) === 1000`
- `futureValue(1000, 0, 10, 120)` ≈ 2707.04
- `futureValue(0, 100, 0, 120)` === 12000
- `futureValue(100, 50, 5, 12)` ≈ 719.06
Log `SELF-TEST PASS` / failures to console.

**Step 3:** Run the script with Node to confirm the self-test passes.

**Step 4:** Commit: `git commit -am "feat: compound interest math with self-test"`

---

### Task 3: Live updates to headline, breakdown, tabs

**Files:**
- Modify: `index.html`

**Step 1:** On every slider `input`, recompute for ages 18, 27, 55 (contributions stop at 18, then pure compounding).
**Step 2:** Update the active tab's headline value, the "your money vs. growth" breakdown bar, and the value readouts next to each slider.
**Step 3:** Verify with known inputs (e.g., seed 1000, contrib 0, rate 10% → ~$6,005 at 18).
**Step 4:** Commit: `git commit -am "feat: live headline, breakdown, and timeline tabs"`

---

### Task 4: Growth chart

**Files:**
- Modify: `index.html`

**Step 1:** `drawChart()` samples balance and contributions-total at each integer year; draws two polylines on canvas (gold = balance, gray = money put in) with auto-scaled Y axis and `$5k`-style labels.
**Step 2:** Redraw on every slider move and on tab switch (highlight selected age with a marker).
**Step 3:** Verify with contrib=0 the two lines overlap.
**Step 4:** Commit: `git commit -am "feat: canvas growth chart"`

---

### Task 5: Theme + responsiveness

**Files:**
- Modify: `index.html`

**Step 1:** Apply gold/navy/white styling, coin/piggy accents, tab styling, stacked-bar colors, responsive layout (single column < 640px, dashboard above).
**Step 2:** Visual check at phone and desktop widths.
**Step 3:** Commit: `git commit -am "style: classy gold Trump Accounts theme"`

---

### Task 6: Final verification

**Files:**
- Inspect: `index.html`

**Step 1:** Full checklist:
- Opens offline by double-clicking
- `SELF-TEST PASS` in console
- Sliders update headline, breakdown, chart live
- Tab switch updates headline + chart marker
- Stacked bar segments sum to balance
- Responsive at phone + desktop widths

**Step 2:** Commit any final fixes.
