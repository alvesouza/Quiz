---
quiz: "Session 9 — Efficiency, Predictability, and the Capstone, Part 3: Predictability, Backtesting, and the Map of m"
tags:
  identidade: "1 · The Present-Value Identity"
  discount: "2 · Discount Rates, and What the Ratio Forecasts"
  exemplo: "3 · Example 9.2 and Its Statistical Caveats"
  noticias: "4 · Variance Decomposition and the Sign of News"
  backtest: "5 · Active Management and Disciplined Backtesting"
  capstone: "6 · The Map of the Discount Factor"
---

## identidade

Q: Why does the chapter insist that the Campbell–Shiller relation is an identity rather than a theory?
- Because it holds only under the assumption of constant expected returns, which makes it an accounting statement rather than a behavioural one.
- Because it cannot be false, so the dividend–price ratio must forecast returns, dividend growth, or both, and only which one is an open question.
- Because it was derived from a general equilibrium model whose assumptions are so weak that no data could ever be brought to bear against it.
- Because it links only observable quantities, so it can be verified arithmetically in any sample without estimating a single free parameter.
<!-- YW5zOjE= -->
> The relation follows from the definition of a return plus a log-linearisation, so no economic assumption can overturn it. That is precisely what gives it teeth: the ratio is *forced* to forecast something. The empirical content of §9.3 is not whether it forecasts but **which** of the two it forecasts, and the answer turns out to be returns.
> Ref: Ribeiro (2026), Ch. 9, §9.3.1 (pp. 311–312), Key result
> Similar: Ribeiro, Problem 9.6

Q: What is the Gordon growth model's role in the chapter's treatment of the identity?
- It is the constant-rate special case in which the ratio equals the discount rate minus growth, so nothing is left to forecast at all.
- It is the empirical benchmark against which the predictive regressions of Example 9.2 are judged for economic significance.
- It supplies the log-linearisation constant that makes the Campbell–Shiller approximation accurate over long historical samples.
- It provides the upper bound on the dividend–price ratio that the excess-volatility literature shows the data routinely violate.
<!-- YW5zOjA= -->
> Set the expected return and the growth rate to constants and the identity collapses to $d/p = r - g$: a fixed ratio with no forecasting power. So any **movement** in the ratio is, by construction, movement in expected returns or in expected growth. Gordon is the case where there is nothing to explain, which is what makes it the right reference point.
> Ref: Ribeiro (2026), Ch. 9, §9.3.2 (pp. 312–313)
> Similar: Ribeiro, Ch. 2 (the Gordon model in the SDF language)

## discount

Q: The empirical answer the chapter calls "Discount Rates" is which finding?
- The dividend–price ratio forecasts dividend growth strongly and returns weakly, so price movements are dominated by cash-flow news.
- The dividend–price ratio forecasts both returns and dividend growth about equally, so the identity's two channels are roughly balanced.
- The dividend–price ratio forecasts returns and has almost no power over dividend growth, so price movements are dominated by discount rates.
- The dividend–price ratio forecasts neither once Stambaugh's bias is corrected, so the identity is satisfied by an unforecastable residual.
<!-- YW5zOjI= -->
> Almost all the variation in the ratio is variation in **expected returns**. Read the implication carefully because it reverses the natural intuition: when prices fall relative to dividends, the market is not forecasting worse dividends, it is demanding a higher return on the same dividends. In the course's language, the discount factor moves.
> Ref: Ribeiro (2026), Ch. 9, §9.3.3 (pp. 313–314), Key result
> Similar: Cochrane (2011), "Discount Rates"

Q: Why does the chapter treat Shiller's excess volatility and return predictability as the same fact?
- Because both are artefacts of the same overlapping-sample problem, which inflates the apparent variability of prices and of estimated slopes alike.
- Because excess volatility is measured on prices while predictability is measured on returns, and the two series are linked by a constant of proportionality.
- Because both were established on the same Shiller dataset, so any sampling error in that dataset propagates identically into each of the two findings.
- Because prices moving without cash-flow news is the same thing as prices being volatile relative to dividends and the ratio forecasting returns.
<!-- YW5zOjM= -->
> One phenomenon, two descriptions. If prices move a great deal while expected dividends barely move, then prices look excessively volatile relative to the present value of subsequent dividends — and the dividend–price ratio that results must forecast returns. Shiller described the variance; the predictability literature described the forecast.
> Ref: Ribeiro (2026), Ch. 9, §9.3.3 (p. 314)
> Similar: Shiller (2015), *Irrational Exuberance*

## exemplo

Q: Example 9.2 regresses cumulative returns on the year-end dividend–price ratio at two horizons. What does it find?
- One year gives slope 11.76 with $R^2$ of 12.5%; five years gives slope 1.75 with $R^2$ of 2.3%, so predictability decays as the horizon lengthens.
- One year gives slope 1.75 with $R^2$ of 2.3%; five years gives slope 11.76 with $R^2$ of 12.5%, so both rise sharply with the horizon.
- Both horizons give slopes near 1.75 with $R^2$ close to 2.3%, so the relationship is weak and essentially flat across horizons.
- Both horizons give slopes above 11 with $R^2$ above 12%, so predictability is strong and roughly constant across the two horizons.
<!-- YW5zOjE= -->
> The one-year result is weak: $t=1.49$, $R^2=2.3\%$. The five-year result is unmistakable: $R^2=12.5\%$, $t=3.65$ by OLS and $2.98$ once Newey–West corrects the overlap. The rise of both slope and $R^2$ with horizon is the hallmark: a small one-year effect **cumulates** because the predictor is highly persistent.
> Ref: Ribeiro (2026), Ch. 9, Example 9.2 (pp. 314–315), Figure 9.2
> Similar: Ribeiro, Problem 9.6

Q: In the five-year regression the OLS $t$ is 3.65 and the Newey–West $t$ is 2.98. Which is the honest figure, and why?
- The OLS figure, since Newey–West is a conservative adjustment appropriate only when residuals are heteroskedastic rather than serially correlated.
- Neither, since the Stambaugh correction supersedes both and produces a third statistic that the chapter reports in place of these two.
- The OLS figure, since the overlap affects the point estimate rather than its standard error and is therefore already reflected in the slope.
- The Newey–West figure, since five-year windows sampled annually share four years of data, and that overlap inflates the naive standard error.
<!-- YW5zOjM= -->
> Overlapping windows induce serial correlation in the residuals, so the naive standard error is far too small and the OLS $t$ is overstated. Report **2.98**. Note the division of labour with the other caveat: Newey–West fixes the standard error, while **Stambaugh** concerns the point estimate, biasing the slope upward in small samples.
> Ref: Ribeiro (2026), Ch. 9, Example 9.2 (p. 315)
> Similar: Ribeiro, Ch. 8 §8.4.2 (overlapping returns in the EH regression)

Q: What causes the Stambaugh bias, and in which direction does it push the estimated slope?
- The predictor is highly persistent and its innovations correlate negatively with returns, which biases the estimated slope upward in small samples.
- The dependent variable is a cumulative multi-period return, which biases the slope downward by an amount growing with the forecast horizon.
- The regression omits the risk-free rate, which correlates with the predictor and biases the slope toward zero in every finite sample.
- The predictor is bounded below by zero, which truncates its distribution and biases the slope downward whenever the ratio is near its floor.
<!-- YW5zOjA= -->
> Both conditions are needed: a persistent regressor **and** innovations negatively correlated with the return. Together they push the estimated slope **upward**, so the true predictability is somewhat weaker than the point estimates suggest and the $t$-statistics overstate significance. Neither caveat overturns the qualitative finding.
> Ref: Ribeiro (2026), Ch. 9, Example 9.2 (p. 315)
> Similar: Ribeiro, True/False bank, Ch. 9

## noticias

Q: Expected future returns on the market rise today, with expected dividends unchanged. What happens to the price?
- It rises, because a higher expected return mechanically raises the present value that investors assign to the unchanged dividend stream.
- It is unchanged, because the two effects in the present-value identity offset exactly when dividend expectations are held fixed.
- It falls, because a higher required return on the same cash flows is a lower price today, and holders lose now while expecting more later.
- It rises or falls depending on the persistence of the shock, since only permanent changes in expected returns move the price at all.
<!-- YW5zOjI= -->
> This sign is the chapter's favourite trap. Discount-rate news of the "good" kind — higher expected future returns — is **bad news for today's price**. The holder takes a capital loss now in exchange for a higher expected return going forward. Getting this backwards inverts the interpretation of every predictive regression in the section.
> Ref: Ribeiro (2026), Ch. 9, §9.3.5 (pp. 316–317)
> Similar: Ribeiro, Problem 9.6

Q: How does the balance of cash-flow news and discount-rate news differ between the aggregate market and individual stocks?
- Cash-flow news dominates both, but the aggregate market shows a larger discount-rate component at horizons beyond about five years.
- Discount-rate news dominates the aggregate market, while cash-flow news matters far more for individual stocks.
- Discount-rate news dominates both, and the distinction between the aggregate and the individual stock is one of degree rather than of kind.
- Cash-flow news dominates the aggregate market, while discount-rate news matters far more for the individual stock in the cross-section.
<!-- YW5zOjE= -->
> Firm-specific fortunes move individual stocks; aggregate prices move overwhelmingly on the discount rate. The contrast is worth stating explicitly because it explains why the index is far more predictable than any single name, and why the excess-volatility debate has always been an argument about the **market**, not about particular firms.
> Ref: Ribeiro (2026), Ch. 9, §9.3.4 (p. 316), §9.3.5 (pp. 316–317)
> Similar: Cochrane (2011), "Discount Rates"

## backtest

Q: A manager reports a backtested gross Sharpe ratio of 1.4 and calls it a strong result. What does Sharpe's arithmetic say about that claim?
- That it is strong evidence, since a Sharpe ratio above one is attainable by fewer than a tenth of active managers in any sample period.
- That it can only be assessed after adjusting for the benchmark, since a gross Sharpe ratio has no meaning until a factor model is specified.
- That beating the market gross is guaranteed for half of active dollars before costs, so a gross figure by itself establishes nothing at all.
- That it is invalid, since Sharpe's arithmetic shows the aggregate of active managers must underperform the market both before and after costs.
<!-- YW5zOjI= -->
> Passive investors hold the market, so active investors in aggregate hold the market too — before costs. Half the active dollars therefore beat it gross by construction, in every market and every period. It is **arithmetic, not a theory**, and it is why the chapter treats a gross backtest as a hypothesis rather than a result.
> Ref: Ribeiro (2026), Ch. 9, §9.4.1 (pp. 317–318), Key result
> Similar: Ribeiro, Ch. 7 (performance measurement)

Q: The fundamental law of active management approximates the information ratio as the information coefficient times the square root of breadth. What is its principal caution?
- That breadth counts independent bets, and a thousand names tilted on one signal is close to one bet rather than a thousand.
- That the information coefficient is unstable over time, so the law holds only for managers whose forecasting skill is stationary across regimes.
- That the square-root form is an approximation which fails badly whenever breadth exceeds a few hundred independent positions per year.
- That the law describes net rather than gross information ratios, so transaction costs are already embedded in the coefficient it reports.
<!-- YW5zOjA= -->
> Overstating breadth by ignoring the correlation of positions is the commonest way the law is used to flatter a strategy: the positions share a common factor, so the independent breadth collapses toward one and the information ratio falls back toward the coefficient itself. The second caution is the reverse of option D — the law describes **gross** ratios, and the breadth that raises it also raises turnover and therefore costs.
> Ref: Ribeiro (2026), Ch. 9, §9.4.2 (pp. 318–319)
> Similar: Ribeiro, Ch. 6 §6.2; Ch. 7

Q: In Example 9.3 the gross Sharpe ratio of 1.4 is deflated step by step. Which sequence does the chapter follow?
- Data-snooping first, then capacity, then costs, then factor exposure, then out-of-sample, ending at an alpha of about 3.5% per year.
- Costs and turnover, then factor exposure, then data-snooping, then capacity, then out-of-sample, ending at an alpha of about zero.
- Factor exposure first, then costs, then out-of-sample, ending with a net Sharpe ratio of 1.25 that the chapter regards as credible.
- Costs, then capacity, then out-of-sample, ending at a harvestable alpha of 1.5% that survives every one of the remaining deflators.
<!-- YW5zOjE= -->
> Turnover of 500% at 0.30% round trip costs 1.5%, so net return is 12.5% and net Sharpe 1.25. Four factors explain 9 of those 12.5 points, leaving alpha of 3.5%. Best of 30 specifications makes $t\approx2.4$ what luck produces, against the Harvey–Liu–Zhu bar of 3. Capacity leaves perhaps 1.5% harvestable. Out of sample: nothing.
> Ref: Ribeiro (2026), Ch. 9, Example 9.3 (p. 321), §9.4.3–9.4.5
> Similar: Ribeiro, Project 2

## capstone

Q: In the capstone map of the discount factor, which session is the one that is *not* an answer to the question "what is $m$"?
- Session 3, because the mean–variance frontier is a statement about portfolio weights rather than about any pricing kernel.
- Session 7, because performance measurement evaluates managers rather than assets, so it lies outside the asset-pricing framework entirely.
- Session 8, because the term structure is priced by no-arbitrage recursion and therefore needs no specification of the discount factor at all.
- Session 5, because factor models there are built to model the covariance matrix, and explaining comovement is a different job from pricing.
<!-- YW5zOjM= -->
> Session 5 builds factor models for **risk**: the object is $\Sigma$, and the purpose is to make the covariance matrix estimable. Session 6 then asks which of those factors are **priced**. Confusing the two is the standard error the chapter warns about. Session 3 *is* about $m$ — the minimum-variance discount factor is the frontier seen from the other side.
> Ref: Ribeiro (2026), Ch. 9, §9.5 (pp. 323–325)
> Similar: Ribeiro, Ch. 5 §5.1; Ch. 6 §6.1

Q: What is Session 9's own entry in the map of the discount factor?
- That the discount factor is linear in several traded factors, which is what makes the cross-section of average returns tractable.
- That the discount factor is bounded below by zero, which is the content of the no-arbitrage condition established in the first session.
- That the discount factor is reweighted into a risk-neutral measure, which is what allows derivatives to be priced without any premia.
- That the discount factor varies over time, so time-varying expected returns are the source of the predictability the chapter documents.
<!-- YW5zOjM= -->
> Each session contributes one clause. Session 9's is **time variation**: prices move because $m$ moves, which is the same statement as expected returns moving, which is the same statement as the dividend–price ratio forecasting returns. The other three options belong to sessions 6, 1 and 8 respectively.
> Ref: Ribeiro (2026), Ch. 9, §9.5 (pp. 323–325)
> Similar: Ribeiro, Ch. 9 §9.3.3
