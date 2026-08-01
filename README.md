# 🇺🇸 Trump Account Calculator

**The American Dream starts now.** A single-file, offline calculator that shows a kid how a real Trump Account grows — the $1,000 U.S. Treasury seed, parental contributions up to $5,000/yr, and S&P 500-style returns, all the way to ages 18, 27, and 55.

## Live Demo

https://hsmahon.github.io/trump-acc/

## What it does

- **Government seed** — the $1,000 Treasury deposit is always applied (kids born 2025–2028).
- **Contributions** — slide up to $5,000/yr; contributions stop at 18, then the account compounds untouched.
- **Expected return** — S&P 500 historical average ≈ 10% by default.
- **Timeline tabs** — projected balance at Age 18 ("It's all yours"), 27, and 55.
- **Your money vs. growth** — a stacked breakdown of what you put in vs. what the market grew for free.
- **Growth chart** — a smooth, animated canvas chart of the balance (gold) vs. money put in (dashed).

## Design

Black, white, and gold — clean, modern, and sans-serif throughout, styled to feel like a premium fintech product (think Fidelity meets Robinhood). It fits entirely in the viewport with **no scrolling** on desktop, tablet, or mobile.

## Tech

A single `index.html` — HTML5, CSS3, vanilla JS, and Canvas. Zero dependencies, no build step, works fully offline. Double-click it and go.

Math is monthly-compounded and verified by a built-in console self-test (open DevTools to see `SELF-TEST PASS`).

## Program facts

Based on the official **Trump Accounts** program ([trumpaccounts.gov](https://trumpaccounts.gov)):

- Every U.S. citizen child born 2025–2028 receives a $1,000 seed from the U.S. Treasury.
- Parents are the sole custodian until age 18, when the account belongs to the child.
- Up to $5,000/yr can be added.
- Funds are invested in American companies.
- Tax-advantaged, traditional IRA-style.

Projections use historical S&P 500 averages and are estimates for illustration only — actual results are not guaranteed.

## Why this exists

A project I wanted to try after sleeping on it since January: using [OpenCode](https://opencode.ai) to go from an idea to a shipped, designed, and deployed page — this little calculator was the test run.

## Author

[hsmahon](https://github.com/hsmahon)
