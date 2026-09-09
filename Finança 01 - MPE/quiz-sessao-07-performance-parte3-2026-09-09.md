---
quiz: "Session 7 — Performance, Part 3: Betting Against Beta, Buffett, and the Limits"
tags:
  bab: "1 · Case 1 — Betting Against Beta"
  funding: "2 · Why the Line Is Flat: Funding Liquidity"
  buffett: "3 · Case 2 — Buffett's Alpha"
  limits: "4 · What Performance Evaluation Cannot Do"
---

## bab

Q: Beta-sorted legs give a low-beta leg with pre-ranking beta $\beta_L<1$ and excess return $R^e_L$, and a high-beta leg with $\beta_H>1$ and excess return $R^e_H$. Which portfolio is the Frazzini–Pedersen BAB factor, and what is its market beta?
- $R^e_L-R^e_H$, with market beta $\beta_L-\beta_H<0$: the raw spread is already the bet against beta, and its negative beta is the compensation the strategy earns.
- $\beta_L R^e_L-\beta_H R^e_H$, with market beta $\beta_L^2-\beta_H^2<0$: each leg is weighted by its own beta so the larger exposure carries the larger weight.
- $\frac{1}{\beta_L}R^e_L-\frac{1}{\beta_H}R^e_H$, with market beta $1-1=0$: each leg is scaled by the leverage that brings its beta to one, so the combination is beta-neutral.
- $\frac{1}{\beta_H}R^e_L-\frac{1}{\beta_L}R^e_H$, with market beta $\beta_L/\beta_H-\beta_H/\beta_L<0$: the legs are cross-scaled so that the cheaper leg receives the larger weight.
<!-- YW5zOjI= -->
> Dividing each leg's excess return by its beta is exactly the leverage that scales that leg's beta to one (7.16): lever the low-beta leg up ($1/\beta_L>1$), delever the high-beta leg down ($1/\beta_H<1$), then go long the first and short the second. Both legs then carry beta one, so the combination has beta $1-1=0$ and is approximately self-financing. The naive unlevered spread is a large short-market position that bleeds in every rising market and hides the anomaly beneath the beta.
> Ref: Ribeiro (2026), Ch. 7, §7.5.2 (p. 247), eq. (7.16); Example 7.5 (p. 248)
> Similar: Ribeiro, Problem 7.5(b),(c) (p. 259)

Q: The chapter's simplified two-decile BAB-style factor over 1963–2026 earns 5,72% per year with a CAPM $t$ of 2,36, then 4,13% ($t=2{,}01$) against FF3, then 1,68% ($t=0{,}82$) against the four-factor model. What is the chapter's own verdict on this sequence?
- That the low-beta effect is a data-mined artefact of the two-decile construction, since a genuine premium would survive a benchmark built from factors that are themselves long–short portfolios.
- That the CAPM alpha is the right number, because the BAB factor is beta-neutral by construction, so its mean *is* its CAPM alpha and further factors only introduce look-ahead into the benchmark.
- That value and momentum absorb most of the return, so the flat SML is fully explained by the Fama–French factors and the low-beta anomaly should be dropped from the factor list.
- That the anomaly is real but the distinctive contribution is smaller than the CAPM alpha suggests: where a return comes from depends entirely on what you insist it be measured against.
<!-- YW5zOjM= -->
> The chapter is explicit that this "is not a verdict that the low-beta effect is unreal — §7.5 argues it is quite real." It is a demonstration of the ladder's discipline: a naive evaluator benchmarking against the market alone would credit a highly significant 5,7% to skill; against Carhart, the residual is a modest 1,7% the data cannot distinguish from luck at this sample length. A strategy's alpha and its factor exposures are two readings of one regression.
> Ref: Ribeiro (2026), Ch. 7, Example 7.4 (pp. 244–245), §7.5.3 (p. 248)
> Similar: Ribeiro, Problem 7.5(d) (p. 259)

Q: Between the paper BAB factor and a tradable low-beta fund lies a set of frictions. Which combination does the chapter name, and what is its point about the funding crisis?
- Turnover costs, capacity limits in large-cap names, and index-reconstitution effects; in a funding crisis the strategy's rebalancing is delayed, so realized returns lag the paper factor by the trading horizon.
- Borrowing above the risk-free rate, lending fees on hard-to-borrow high-beta names, and forced liquidation on margin calls; the crisis that creates the premium is the one that can carry a levered BAB fund out.
- Bid–ask spreads on the low-beta leg, short-sale constraints in small caps, and dividend-withholding drag; in a funding crisis the low-beta leg becomes unshortable, so the strategy converts into a long-only tilt.
- Management fees, benchmark tracking error against a market index, and the tax treatment of short rebates; in a funding crisis the strategy's tracking error spikes, so investors redeem exactly when the premium is largest.
<!-- YW5zOjE= -->
> The factor formula assumes leverage is free and frictionless; it is not. Real borrowing costs more than the risk-free rate, high-beta names carry the steepest lending fees, and a levered beta-neutral book can be compelled to liquidate at the worst moment. There is also a capacity limit — the anomaly is strongest among smaller, less liquid stocks — so a realistic net-of-cost Sharpe ratio is meaningfully below the gross figure of 0,30 the simplified factor posts.
> Ref: Ribeiro (2026), Ch. 7, §7.5.3 (p. 248), §7.5.4 (pp. 249–250)
> Similar: Ribeiro, Problem 7.5(d) (p. 259)

## funding

Q: Frazzini and Pedersen explain the flat SML by leverage constraints. What is the mechanism, and which prediction does the chapter say makes it more than a story?
- Constrained investors who want high returns but cannot borrow reach for high beta, bidding it up and leaving low beta too cheap; the premium should be larger when funding is tight, and the strategy should lose sharply in funding crises.
- Constrained investors hold too little of the market portfolio, so the zero-beta rate rises above the bill rate; the premium should be larger when short rates are high, and the strategy should be flat when the yield curve inverts.
- Constrained investors prefer lottery-like payoffs and overpay for volatile stocks; the premium should be larger after periods of high market volatility, and the strategy should lose when volatility mean-reverts.
- Constrained investors are benchmarked against a market index and avoid low-beta names that create tracking error; the premium should be larger when dispersion is high, and the strategy should lose in bull markets.
<!-- YW5zOjA= -->
> An investor who craves return but cannot lever has only one route: tilt into high beta, which delivers high expected return per dollar invested with no borrowing. That crowd bids high beta up and neglects low beta — exactly the flat line. The signature conditional prediction is that flatness worsens when constraints bind harder, and Frazzini–Pedersen find that time-variation against funding proxies. Lottery preference and benchmarking are the named *alternative* readings; they share the prediction about prices but differ on why, and the data have not cleanly chosen.
> Ref: Ribeiro (2026), Ch. 7, §7.5.5 (pp. 250–251), PhD Hint (p. 251)
> Similar: Ribeiro, Problem 7.5(d) (p. 259)

## buffett

Q: A vehicle's unlevered stock portfolio earns mean excess return $\mu$ with volatility $\sigma$; the vehicle applies leverage $L>1$ financed by insurance float whose cost is $c$ *below* the bill rate. What are the levered excess return, the levered volatility, and the effect on the Sharpe ratio?
- $L\mu$ and $L\sigma$, with the Sharpe ratio rising to $L\mu/\sigma$, because leverage multiplies the return while the float leaves the volatility of the underlying book unchanged.
- $L\mu+(L-1)c$ and $L\sigma$, with the Sharpe ratio essentially unchanged, because leverage scales an existing Sharpe ratio rather than manufacturing one.
- $L\mu-(L-1)c$ and $\sqrt{L}\,\sigma$, with the Sharpe ratio rising, because volatility scales as the square root of the leverage while the return scales linearly.
- $\mu+(L-1)c$ and $L\sigma$, with the Sharpe ratio falling, because only the financing benefit is levered while the underlying excess return is earned once on equity capital.
<!-- YW5zOjE= -->
> Leverage multiplies both the excess return and the volatility, and cheap float adds $c$ saved on each of the $L-1$ borrowed dollars. So the Sharpe ratio barely moves — that is the point: leverage does not manufacture a Sharpe ratio, it scales one, turning a solid $\mu$ into a spectacular levered return that compounds over decades. The contrast is the constrained investor of §7.5.5, who borrows *above* the bill rate and whose leverage is yanked away at the bottom.
> Ref: Ribeiro (2026), Ch. 7, §7.6.2 (p. 252), Example 7.6 (p. 252)
> Similar: Ribeiro, Problem 7.6(a),(c) (p. 259)

Q: Frazzini, Kabiller and Pedersen (2018) report a Berkshire Sharpe ratio of about 0,79 over 1976–2017. The chapter applies its own detection arithmetic to that number in reverse. What does it conclude?
- That the record cannot be assessed statistically, since the Sharpe ratio of a single vehicle is not an alpha and the years-to-detect formula applies only to information ratios.
- That the record is precisely what the coin-flipping tournament predicts, since the maximum of a very large population of unskilled investors will always look like this by chance.
- That the implied $t$ over roughly forty years is about 2, so the record is significant but only barely, which is why the factor decomposition is needed to settle the question.
- That the implied $t$ over roughly forty years is about 5, so the record is real beyond statistical doubt and demands an explanation rather than a dismissal.
<!-- YW5zOjM= -->
> $0{,}79\times\sqrt{40}\approx5{,}0$ — overwhelming significance, far above what the coin-flipping survivors of §7.1.1 would produce even in a population of every investor who ever lived. Berkshire is not a lucky flipper. That is exactly what makes the decomposition interesting: the puzzle is not *whether* Buffett is skilled but *what the skill consists of*.
> Ref: Ribeiro (2026), Ch. 7, §7.6.1 (p. 251), Key result (p. 254)
> Similar: Ribeiro, Problem 7.6(b) (p. 259)

Q: What are the three parts of the Frazzini–Kabiller–Pedersen decomposition of Berkshire's record, in the chapter's own terms?
- Roughly 1,6–1,7 to 1 leverage financed by float above the bill rate; loadings on size and momentum; and a residual alpha that grows as the benchmark is enriched toward the four-factor model.
- Roughly 2 to 1 leverage financed by public debt at the bill rate; loadings on the market and profitability; and a residual alpha that survives every benchmark, which is the paper's headline finding.
- Roughly 1,6–1,7 to 1 leverage financed by float below the bill rate; loadings on value, BAB and quality-minus-junk; and a residual alpha that shrinks toward insignificance as those factors enter.
- Roughly 1,6–1,7 to 1 leverage financed by float below the bill rate; loadings on the market alone, since Berkshire's beta exceeds one; and a residual alpha attributable to private operating companies.
<!-- YW5zOjI= -->
> Cheap, permanent leverage times a leveraged bet on cheap, safe, quality stocks, plus a shrinking residual. Berkshire's market beta is well *below* one — the returns are high and the beta is low, the low-beta anomaly incarnate — so a naive observer who assumes high returns must mean high risk has the story backwards. Note the chapter declines to reproduce the paper's exact loadings and residual table, citing only the Sharpe ratio and the leverage as robust.
> Ref: Ribeiro (2026), Ch. 7, §7.6.2 (pp. 252–253), Key result (p. 254)
> Similar: Ribeiro, Problem 7.6(b),(d) (p. 259)

Q: "The whole record is just factors and leverage, so there is no skill here." Which set of three reasons does the chapter give for rejecting that conclusion?
- The recipe was identified and executed decades before the factors were named; the execution demanded a temperament that survives decades of doubt; and the leverage was not merely large but cheap and permanent.
- The factor loadings are estimated with error, so the residual is understated; the sample is survivorship-free only for the public book; and the private companies lie outside any factor benchmark.
- The decomposition uses factors published after the fact, so it is in-sample by construction; the residual is significant at conventional levels; and Berkshire's leverage was not observable to the market.
- The joint-hypothesis problem means the benchmark is always in doubt; the ladder was stopped short of FF5; and the counterfactual factor investor would in fact have matched Berkshire's return exactly.
<!-- YW5zOjA= -->
> The chapter is emphatic that "explained by factors" is not "explained away." The counterfactual investor who "just held the factors" would have needed factors nobody had published, float nobody else could source, and the temperament to hold through 1999–2000, when Berkshire lost roughly half its value relative to a soaring market. A record explained is a record understood, not a record dismissed — the decomposition tells you what the skill *was*, not that there was none.
> Ref: Ribeiro (2026), Ch. 7, §7.6.3 (p. 253), §7.6.4 (pp. 253–254); Common pitfalls (p. 257)
> Similar: Ribeiro, Problem 7.6(d) (p. 259)

## limits

Q: Every alpha in the chapter is measured against a benchmark model, which the chapter says makes any test of skill a joint test. Which example does it use to show the bind is not hypothetical, and what does it say about escaping it?
- The Sharpe-versus-IR conflict of Example 7.1, where a fund's beta inflates its total volatility; there is no escape, because the choice between the two measures is a matter of use rather than of evidence.
- The constrained style-analysis regression, where the imposed weights absorb a fund's true bets; there is no escape, because a coarse set of indices can always be gamed by a manager tilting within a style.
- Berkshire's enormous CAPM alpha, much of which is exposure to the BAB and QMJ factors the CAPM omits; there is no escape by any statistical device, because the true model of expected returns is not known.
- Survivorship bias, whose one-to-two-point magnitude is the same order as the alpha under investigation; there is no escape short of a survivorship-free database that retains every dead fund.
<!-- YW5zOjI= -->
> A nonzero alpha always rejects two things at once: that the manager has no skill, and that the benchmark is the true model. Berkshire makes it concrete — the CAPM "alpha" was substantially a benchmark error, not skill. Every test of skill is a test of skill *given a model*, and the model is always in doubt; a rejection is shared between the manager and the model, and the data cannot say in what proportion. That is the shadow Chapter 9 makes its explicit subject.
> Ref: Ribeiro (2026), Ch. 7, §7.7 (pp. 255–256); §7.6.2
> Similar: Ribeiro, True/False (p. 259)

Q: Beyond the ex-ante/ex-post gap and the joint hypothesis, the chapter names a third limit that applies to strategies rather than managers and ties it to Project 2. What is it, and what discipline does it prescribe?
- The ex-ante/ex-post gap: measures are computed from a sequence of conditions that will never recur, so the discipline is to report every statistic conditional on the market regime in which it was earned.
- The capacity limit: a rule that works at small size cannot be filled at billions, so the discipline is to deflate any reported Sharpe ratio by the turnover the strategy requires at realistic scale.
- Backtest overfitting: a rule chosen by searching history reports the maximum of many trials, so the discipline is out-of-sample testing and deflating the statistic for the breadth of the search.
- Smoothing and illiquidity: a rule holding thinly traded assets reports a volatility that is an artefact of appraisal, so the discipline is to unsmooth the series before any statistic is computed.
<!-- YW5zOjI= -->
> Try a hundred signals, a dozen holding periods and several weightings, report the best, and by the order-statistics logic of §7.3.5 the winner is large by construction whether or not any rule predicts. "A Sharpe ratio of two on a backtest that was the best of a thousand tried is no more impressive than a factor with $t=2{,}5$ from the zoo." This is the performance-evaluation face of the joint hypothesis: the alpha is jointly a statement about the world and about how hard you looked.
> Ref: Ribeiro (2026), Ch. 7, §7.7 (p. 256); §6.7, §7.3.5
> Similar: Ribeiro, True/False (p. 259); Projetos/Project2_Brief.pdf
