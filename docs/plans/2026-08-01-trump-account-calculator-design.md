# Trump Account Calculator — Design

**Date:** 2026-08-01
**Status:** Approved

## Goal

A single-file, offline `index.html` web page that teaches a teen how a real Trump Account grows — $1,000 government seed, parental contributions up to $5,000/yr, invested in American stocks (S&P 500-style returns), maturing at age 18.

## Real program facts (from trumpaccounts.gov)

- Every U.S. citizen child born 2025–2028 gets a $1,000 seed from the U.S. Treasury.
- Parent is sole custodian until age 18; then the account is the child's.
- Up to $5,000/yr can be added by the parent.
- Funds invested in American companies (S&P 500 historical average ~10%).
- Tax-advantaged, traditional-IRA style.
- Official projections illustrate value at ages 18, 27, 55 ("illustration only").

## Requirements

- Single HTML file, zero dependencies, works fully offline by double-clicking.
- Inputs: government seed ($0–$1,000, default $1,000), annual contribution ($0–$5,000), expected annual return (0–15%, default 10%), all via sliders with live value readouts.
- Contributions apply from birth to age 18 only; after 18 the balance grows untouched.
- Timeline tabs: Age 18 ("It's all yours"), Age 27, Age 55.
- Results: headline projected value at the selected age; breakdown of "your money" (government seed + contributions) vs. "growth" (free money) with a stacked bar; year-by-year line chart on `<canvas>` showing balance vs. money put in.
- Tax-advantaged note banner.
- Theme: classy gold/navy/white official look, coin/piggy accents, "The American Dream starts now" vibe. Responsive: single column on phones, dashboard on desktop.
- Built-in console self-test verifying the `futureValue()` math against fixed expected values.

## Math

Monthly compounding (12 periods/yr).

```
r = annualRate / 100 / 12
n = months
futureValue = start * (1 + r)^n
              + (r != 0 ? monthly * (((1 + r)^n - 1) / r) : monthly * n)
```

Contributions stop at age 18; the age-27 and age-55 values are the age-18 balance compounded forward with no further contributions.

## Non-goals

- No persistence, no accounts, no network calls.
- Not a goal-tracker or milestone system.
