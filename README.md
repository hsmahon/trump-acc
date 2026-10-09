# 🇺🇸 Trump Account Calculator

A single-file, offline calculator showing how a Trump Account grows — the $1,000 Treasury seed, contributions up to $5,000/yr, and S&P 500-style returns to ages 18, 27, and 55.

**Live demo:** https://hsmahon.github.io/trump-acc/

## What it does

- Shows projected balance at ages 18, 27, and 55
- Adjustable family contributions plus employer match (up to $2,500/yr, shared $5,000/yr cap)
- Monte Carlo projections (5,000 paths) with Low / Median / Above-average scenarios
- Breaks down your money vs. market growth
- Canvas fan chart

Projections use Monte Carlo simulation instead of a single fixed return because real market returns vary year to year. Simulating 5,000 possible histories from long-run S&P 500 behavior (μ≈10.3%, σ≈16%) shows the range of outcomes, not just the average.

---

Built with [OpenCode](https://opencode.ai) — a project I wanted to try after sleeping on it since January.

[hsmahon](https://github.com/hsmahon)
