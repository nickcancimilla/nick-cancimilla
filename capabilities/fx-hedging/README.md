# FX hedging

This capability compares ways to convert a future EUR receivable into USD. The film-rights scenario concerns a U.S. film studio receiving €3,600,000 from a Spanish streaming platform in 273 days.

## Current deliverable

[Stage 1 executive brief](../../docs/briefs/2026-11-02-film-rights-hedge-brief.md) defines the exposure, hedge alternatives, assumptions, hypothesis, and analysis plan. Its calculations are preliminary scenario comparisons; the workbook and final recommendation are planned for later stages.

## Planned files

- `spec.md`: Stage 2 workbook design, named ranges, formulas, and validation checks.
- `model.xlsx`: Stage 3 workbook, populated with updated market inputs in Stage 4.
- `../../analysis/`: Build audit and Stage 5 validation.
- `../../data/`: Market-data sources and timestamps.
- `../../docs/decisions/`: Stage 5 hedge decision memo.

## Conventions

EURUSD is quoted in USD per EUR. Preserve the assigned EUR amount and 273-day horizon. Label assumptions, teaching inputs, and sourced market observations distinctly. Include premium and financing treatment when comparing terminal USD proceeds.

## Source

[Course FX hedging project instructions](https://adamwstauffer.github.io/ai-lms/fx-hedging-stage1.html).
