---
type: brief
title: "FX Hedging Brief for the Film Rights Receivable"
scenario: film-rights
engagement: fx-hedging
capability: fx-hedging
date: 2026-11-02
status: committed
hypothesis: "I expect the forward to average $25,584 more because two $92,880 advantages outweigh the put’s single $109,008 advantage under equal weights."
llm_used: "Codex (planning, calculations, drafting); Claude Opus 5.5 (input checks, ECB spot rate, arithmetic verification, critique)"
---

# FX Hedging Brief for the Film Rights Receivable

**To:** Chief Financial Officer
**From:** Nicholas Cancimilla
**Created by:** Nicholas Cancimilla
**Updated by:** Nicholas Cancimilla
**Date Created:** November 2, 2026
**Date Updated:** November 2, 2026
**Version:** 1.1  
**LLM Used:** Codex (planning, calculations, drafting); Claude Opus 5.5 (input checks, ECB spot rate, arithmetic verification, critique)

## Executive Summary

We will receive €3.6 million from a Spanish streaming platform in 273 days. A 5% decline in the euro would create a $201,888 shortfall against today’s dollar value, so I will compare three hedges and use the Stage 5 results to make a recommendation.

I will evaluate a forward, a money-market hedge, and a purchased EUR put; my preliminary scenarios favor the forward over the put on average proceeds.

## Background & Objectives

The studio sold content rights to a Spanish streaming platform and agreed to payment in euros. Our receivable is fixed, but the dollars available to cover our costs are not. The ECB’s November 2, 2026 reference rate is $1.1216 per euro, putting the payment’s current value at $4,037,760. A 5% decline would lower the rate to $1.06552 and proceeds to $3,835,872.

The goal is to understand how much protection each hedge provides, what that protection costs, and how much upside we retain if the euro strengthens.

## Methods

A **forward** would lock in the rate for selling our €3.6 million in 273 days. At an illustrative 1.1250, proceeds would be $4,050,000. This protects our budget but gives up stronger-euro upside and may require a counterparty credit line.

For a **money-market hedge**, we would borrow enough euros today for the receivable to repay principal and interest, convert the borrowing into dollars, and invest them until settlement. This fixes dollar proceeds but uses borrowing capacity and requires several transactions.

A **purchased EUR put** would let us sell at an illustrative strike of 1.1216 while keeping stronger-euro upside. The assigned premium of $0.0224 per euro costs $80,640, reducing the net floor to $3,957,120 before premium financing costs. We pay the premium even if we never exercise the option.

## Limitations & Next Steps

### Assumptions

I assume the customer pays the full amount on time, the 273 days starts on November 2, 2026, and each hedge covers the entire receivable with no offsetting euro expenses. The money-market comparison assumes access to borrowing and investment at the modeled rates.

The indicative forward of 1.1756 and assigned option premiums are teaching values, not market quotes. The assumed 1.1250 forward reflects a small USD-over-EUR interest-rate differential; Stage 2 will replace that assumption using sourced USD and EUR rates and spot from its starting date. Initial calculations exclude bank fees, bid-ask spreads, taxes, and premium financing costs. Money-market interest and the option premium are included.

### Hypothesis

I expect the forward to average about $25,600 more than the put because the put trails by $92,880 in both the down and flat scenarios but gains only $109,008 in the up scenario. I give equal weight to a 5% euro decline, no change, and a 5% increase. The put beats the illustrative forward above 1.1474, approximately 2.3% above starting spot. These are preliminary scenarios, not estimated probabilities.

I would be wrong if, using updated inputs and the same equally weighted −5%, 0%, and +5% scenarios around the Stage 2 starting spot, the put’s average net proceeds exceed the forward’s.

### Roadmap

- **Stage 2** produces the workbook design, formulas, and checks in `capabilities/fx-hedging/spec.md`.
- **Stage 3:** AI builds `capabilities/fx-hedging/model.xlsx`, and I audit it in `analysis/YYYY-MM-DD-film-rights-build-audit-analysis.md`.
- **Stage 4** updates market inputs and records sources and timestamps in `data/YYYY-MM-DD-film-rights-market-data-memo.md`.
- **Stage 5** uses an independent LLM run plus hand calculations, documented in `analysis/YYYY-MM-DD-film-rights-validation-analysis.md`, before the final recommendation in `docs/decisions/YYYY-MM-DD-film-rights-hedge-decision-memo.md`.

## References

European Central Bank. (2026, November 2). [Euro foreign exchange reference rates](https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html).

Stauffer, A. (2026). [Stage 1—Executive brief](https://adamwstauffer.github.io/ai-lms/fx-hedging-stage1.html).

Stauffer, A. (2026). [Scenarios: EUR receivables (USD base), Scenario 28: Film-rights](https://github.com/adamwstauffer/shidler/blob/main/courses/International-Finance-And-Securities/projects/fx-hedging/scenarios.md).

Stauffer, A. (2026). [Decision memo template](https://github.com/adamwstauffer/shidler/blob/main/courses/International-Finance-And-Securities/projects/fx-hedging/_templates/template-decision-memo.md).
