---
quiz: "Session 9 — Efficiency, Predictability, and the Capstone, Part 2: Event Studies"
tags:
  anormal: "1 · Abnormal Returns and the Benchmark Model"
  janelas: "2 · Estimation and Event Windows"
  cumulacao: "3 · CAR, CAAR, and Buy-and-Hold"
  covid: "4 · Example 9.1 — The COVID-19 Crash"
  armadilhas: "5 · Statistical Pitfalls and Post-Earnings Drift"
---

## anormal

Q: Under the market model, where does the joint-hypothesis problem enter the definition of an abnormal return?
- It enters through the choice of estimation window, since a window that is too short makes the estimated beta unstable and the abnormal return noisy.
- It enters through the word abnormal itself, which is defined by a benchmark model, so a bad benchmark manufactures abnormal returns out of nothing.
- It enters through the market proxy, since the true market portfolio is unobservable and any index is only a partial stand-in for that portfolio.
- It does not enter, because subtracting a fitted regression line removes any dependence on the model that generated the fitted values in the sample.
<!-- YW5zOjE= -->
> The abnormal return is the realized return minus $\hat\alpha_i + \hat\beta_i R_{m,t}$, and that second piece **is** a model of expected returns. So every event study tests the announcement's impact and the benchmark jointly. The market-proxy point is real too, but it is Roll's critique rather than the definitional issue asked about here.
> Ref: Ribeiro (2026), Ch. 9, §9.2.1 (pp. 305–306), §9.1.3 (p. 301)
> Similar: Ribeiro, True/False bank, Ch. 9

Q: A researcher measures abnormal returns against a constant-mean-return model rather than the market model. What is the consequence?
- Nothing changes materially, since over short event windows the two benchmarks produce abnormal returns that are identical by construction.
- The abnormal returns become more precise, because a constant mean has one parameter to estimate rather than the two the market model requires.
- Market-wide moves during the event window are no longer netted out, so a market crash shows up as abnormal even where the firm did nothing unusual.
- The cross-sectional test is invalidated, because the constant-mean model violates the independence assumption the $t$-statistic relies upon.
<!-- YW5zOjI= -->
> The market model's job is to subtract $\hat\beta_i R_{m,t}$, the part of the return explained by the market's own move. Drop it and every firm inherits the market's move as "abnormal". This is exactly why Example 9.1's CAAR is flat through a crash: the aggregate collapse is absorbed by the beta term, not counted as abnormal.
> Ref: Ribeiro (2026), Ch. 9, §9.2.1 (pp. 305–306), Example 9.1 (p. 308)
> Similar: Ribeiro, Problem 9.4

## janelas

Q: Why must the estimation window and the event window not overlap?
- Because overlapping windows double-count the event days, so the cumulative abnormal return is inflated by roughly the length of the overlap.
- Because the event contaminates the parameters that define what normal means, which biases the estimated abnormal returns toward zero.
- Because the market model assumes homoskedastic residuals, and event-period volatility is higher, so the overlap violates that assumption.
- Because regulators require a clean separation of the two periods before an event study may be submitted as evidence in litigation proceedings.
<!-- YW5zOjE= -->
> If the event sits inside the estimation sample, the fitted $\hat\alpha$ and $\hat\beta$ partly absorb the event's own return. "Normal" is then defined to include the very thing being measured, and the abnormal return shrinks toward zero. The chapter also leaves a gap before the event, which protects against news leaking before the formal date.
> Ref: Ribeiro (2026), Ch. 9, §9.2.2 (pp. 306–307)
> Similar: Ribeiro, Problem 9.4; Campbell, Lo & MacKinlay, Ch. 4

Q: The COVID study estimates over $\tau\in[-250,-12]$ rather than running the estimation window right up to $\tau=-1$. What does the two-week gap buy?
- It raises the number of degrees of freedom available for the regression, which tightens the confidence interval around the estimated beta.
- It aligns the estimation sample with a calendar quarter, so the fitted parameters can be compared with published quarterly risk measures.
- It removes the most volatile days from the sample, so the estimated residual variance is smaller and the test statistic correspondingly larger.
- It protects the parameters against news leaking before the formal event date, so pre-event drift does not contaminate the benchmark.
<!-- YW5zOjM= -->
> Information rarely arrives exactly on the announcement date. If the market began repricing in the days before $\tau=0$, those days belong to the event, not to normal times. Ending the estimation window early keeps the leak out of $\hat\alpha$ and $\hat\beta$. The cost is a slightly shorter estimation sample, which is cheap by comparison.
> Ref: Ribeiro (2026), Ch. 9, §9.2.2 (p. 307), Example 9.1 (p. 308)
> Similar: Ribeiro, True/False bank, Ch. 9

## cumulacao

Q: What distinguishes the cumulative abnormal return from the buy-and-hold abnormal return?
- The first sums abnormal returns while the second compounds them, so they agree over days and diverge badly over long horizons.
- The first is computed firm by firm while the second is computed on the portfolio, so only the second can be averaged across firms.
- The first uses the market model while the second uses a matched control firm, so the two rest on different benchmarks entirely.
- The first is measured in excess of the risk-free rate while the second is measured in excess of the benchmark's realised total return.
<!-- YW5zOjA= -->
> Summing and compounding are close over a few days and drift apart over years. The buy-and-hold measure also has a strongly **skewed** distribution and is far more sensitive to the benchmark, which is why long-horizon event studies are so much less credible than short-window ones. Report both at long horizons and expect argument.
> Ref: Ribeiro (2026), Ch. 9, §9.2.3 (pp. 307–308)
> Similar: Ribeiro, Problem 9.5

Q: The cross-sectional $t$-statistic divides the average cumulative abnormal return by which quantity?
- The time-series standard deviation of the daily abnormal returns, scaled by the square root of the length of the event window.
- The cross-sectional standard deviation of the firms' cumulative abnormal returns, divided by the square root of the number of firms.
- The residual standard error from the market-model regression, averaged across firms and scaled by the number of estimation days.
- The standard deviation of the market return over the event window, which normalises the statistic for market-wide volatility.
<!-- YW5zOjE= -->
> The test asks whether the firms agree. Dispersion **across firms** in their cumulative abnormal returns is the relevant noise, so $t = \overline{CAR} / (\sigma(CAR)/\sqrt{N})$. Its validity rests on the events being **independent across firms** — the assumption Example 9.1 deliberately violates and openly flags.
> Ref: Ribeiro (2026), Ch. 9, §9.2.4 (p. 308)
> Similar: Campbell, Lo & MacKinlay, Ch. 4

## covid

Q: In the COVID study the CAAR is $+0.4\%$ at $\tau=0$ even though the market was collapsing. What does the flat start show?
- That the pandemic was not yet news on 19 February 2020, so no information about the exposed industries had reached prices by that date.
- That the eight industries had betas near zero, so aggregate market moves passed through to their returns only very weakly over the window.
- That the event date was chosen badly, since a well-specified study places the largest abnormal return on the event day rather than later.
- That the market-wide move is absorbed by each industry's beta times the market return, so only industry-specific deviation is measured.
<!-- YW5zOjM= -->
> This is the subtlest point in the example. The crash itself is *not* abnormal — it is exactly what a beta times a falling market predicts. The CAAR only departs from zero once the pandemic's **differential** severity became clear from late February. The flat start also confirms that the market model fits well in normal times.
> Ref: Ribeiro (2026), Ch. 9, Example 9.1 (pp. 308–309)
> Similar: Ribeiro, Problem 9.4

Q: Which set of figures does the COVID study report?
- CAAR of $-6.5\%$ at $\tau=+15$ with a cross-sectional $t$ of $-2.48$; oil at $-19.2\%$ and coal at $-13.1\%$, but steel $+0.8\%$ and autos $+2.9\%$.
- CAAR of $-19.2\%$ at $\tau=+15$ with a cross-sectional $t$ of $-6.50$; oil at $-13.1\%$ and coal at $-6.5\%$, with steel and autos both negative.
- CAAR of $-2.48\%$ at $\tau=+15$ with a cross-sectional $t$ of $-6.50$; the dispersion across the eight industries is small and statistically flat.
- CAAR of $-6.5\%$ at $\tau=+5$ with a cross-sectional $t$ of $-1.12$; oil at $-19.2\%$, coal at $-13.1\%$, and every other industry also negative.
<!-- YW5zOjA= -->
> Memorise the pair $-6.5\%$ and $t=-2.48$, and the dispersion, because the dispersion is the lesson: two of the eight "exposed" industries barely moved. Oil's $\beta=1.12$ and coal's $\beta=1.41$ are also quoted. The result is economically large and statistically discernible with only eight cross-sectional units.
> Ref: Ribeiro (2026), Ch. 9, Example 9.1 (pp. 308–309), Figure 9.1
> Similar: Ribeiro, Problem 9.4

Q: The chapter names a confound that a single-event study cannot separate from the pandemic effect in the energy names. Which is it?
- The simultaneous Saudi–Russia oil-price war, which compounded the collapse in energy returns over precisely the same event window.
- The Federal Reserve's emergency rate cuts, which raised the present value of long-duration cash flows across every industry at once.
- The suspension of short selling in several European markets, which mechanically removed downward pressure from the exposed names.
- The rebalancing of the major equity indices in March 2020, which forced passive funds to trade the affected industries in large size.
<!-- YW5zOjA= -->
> Two shocks hit energy in the same window, and with one calendar event there is no way to attribute the abnormal return to one rather than the other. Saying so is part of the answer: the chapter uses this to argue that a single event, however dramatic, gives far weaker inference than the thousand-event designs of the classic literature.
> Ref: Ribeiro (2026), Ch. 9, Example 9.1 (p. 309)
> Similar: Ribeiro, True/False bank, Ch. 9

## armadilhas

Q: Eight industry portfolios are studied around one calendar date. What does that do to the cross-sectional test?
- Nothing, provided the eight portfolios are value-weighted, since value weighting makes the abnormal returns independent by construction.
- It strengthens the test, because a common event date removes calendar-time noise that would otherwise inflate the residual variance.
- It invalidates the market model, since a single date leaves too few observations to estimate a beta for each of the eight portfolios.
- The abnormal returns are correlated across portfolios, so the independence assumption fails and the standard error is far too small.
<!-- YW5zOjM= -->
> This is event clustering. When events share a date, a common shock moves every firm's abnormal return together, so the eight observations carry far less information than eight independent ones. The effective sample is closer to one. The chapter flags this about its own example rather than hiding it, which is the behaviour to imitate.
> Ref: Ribeiro (2026), Ch. 9, §9.2.5 (pp. 309–310)
> Similar: Ribeiro, Problem 9.5

Q: Post-earnings-announcement drift is described as challenging one form of efficiency in particular. Which, and on what grounds?
- The weak form, because the drift is predictable from the price path alone once the announcement day's return has been observed by traders.
- The semi-strong form, because the information was public on the announcement day yet prices keep moving the same way for weeks.
- The strong form, because only investors with private access to the earnings figures before release can systematically exploit the drift.
- No form in particular, because the drift is a pure benchmark artifact and disappears entirely once a four-factor model is used instead.
<!-- YW5zOjE= -->
> Semi-strong efficiency says public information is impounded **immediately**: a jump at $\tau=0$, flat thereafter. The drift says the jump was incomplete, so a strategy buying the good-news group on day $+1$ earns an abnormal return on information everyone already had. The standing caveat applies — the rejection is joint with the benchmark.
> Ref: Ribeiro (2026), Ch. 9, §9.2.6 (pp. 310–311)
> Similar: BKM 13e, Ch. 11 §11.4 (p. 354)
