---
quiz: "Session 6 — Factor Models for Expected Returns"
tags:
  equiv: "1 · The Central Equivalence: Linear SDF and Beta Pricing"
  apt: "2 · The APT, 'Approximate', and Characteristics"
  sorts: "3 · The Portfolio Sort and the Evidence Factors"
  ff: "4 · The Fama–French Factors"
  grs: "5 · Testing I — Time-Series Alphas and GRS"
  fm: "6 · Testing II — The Cross-Section and Fama–MacBeth"
  zoo: "7 · The Factor Zoo and What Survives"
---

## equiv

Q: Chapter 5 ran the regression $R^e_{it}=\alpha_i+\beta_i'f_t+\varepsilon_{it}$ and used only the betas. What exactly is chapter 6's claim about the same regression?
- That the intercepts $\alpha_i$ are all zero, so loadings determine expected returns with nothing left over.
- That the betas are estimated consistently once the factors are traded excess returns.
- That the residual covariance matrix is diagonal, so the factors exhaust all comovement.
- That the factor covariance matrix $\Sigma_F$ is nonsingular, so the loadings are identified.
<!-- YW5zOjA= -->
> One regression, two chapters. Chapter 5 took the slopes and built $\Sigma$, leaving the intercepts untouched; chapter 6 is about those intercepts. "The model prices the cross-section" means every $\alpha_i=0$: once you know an asset's loadings, you know its expected return.
> Ref: Ribeiro (2026), Ch. 6, §6.1 (p. 191), §6.1.1 (p. 191)
> Similar: Ribeiro, True/False 1 (p. 222); Common pitfalls (p. 219)

Q: Substituting $m=a-b'f$ into $0=E_t[m R^e_i]$ and converting covariances into regression betas yields $E_t[R^e_{i,t+1}]=\beta_i'\lambda$. What is $\lambda$?
- $\lambda=\Sigma_F^{-1}\text{cov}(f,R^e_i)$, one vector per asset.
- $\lambda=R_{f,t}\,\Sigma_F\,b$, a single $K$-vector common to all assets.
- $\lambda=-\text{cov}(m,R^e_i)/E_t[m]$, the asset's own risk premium.
- $\lambda=b$, since the discount-factor loadings are the prices of risk by definition.
<!-- YW5zOjE= -->
> The chain is $0=E[mR^e]\Rightarrow E[R^e]=-R_f\,\text{cov}(m,R^e)=R_f\,\text{cov}(R^e,f)\,b=R_f\,\beta'\Sigma_F b$. The last equality uses $\text{cov}(R^e_i,f)=\beta_i'\Sigma_F$, the definition of a multiple-regression coefficient. $\lambda$ carries no $i$ subscript: prices of risk are common, betas vary asset by asset.
> Ref: Ribeiro (2026), Ch. 6, §6.1.2 (pp. 191–192), eq. (6.9)
> Similar: Ribeiro, Problem 6.1 (p. 220); True/False 2 (p. 222)

Q: Why does the chapter insist the equivalence between $m=a-b'f$ and $E[R^e_i]=\beta_i'\lambda$ runs in *both* directions?
- Because only the converse guarantees $\Sigma_F$ is invertible, which the forward direction assumes.
- Because the forward direction holds for traded factors and the converse for non-traded ones.
- Because a one-way implication would leave beta pricing as a separate hypothesis rather than a restatement of the SDF.
- Because the converse is what identifies the factors, which the forward direction leaves open.
<!-- YW5zOjI= -->
> Given beta pricing, set $b=R_f^{-1}\Sigma_F^{-1}\lambda$ and $a=R_f^{-1}+b'E[f]$; that $m$ prices every asset. Since each statement implies the other, they are one claim in two languages, and the choice between them is convenience. Testing "is $m$ linear in $f$?" — a statement about an unobservable — becomes testing "are these regression intercepts zero?"
> Ref: Ribeiro (2026), Ch. 6, §6.1.3 (pp. 192–193), Key result (p. 192)
> Similar: Ribeiro, True/False 1 (p. 222)

Q: Two uncorrelated traded factors have means 6% and 4% per year and variances $(15\%)^2$ and $(12\%)^2$. An asset loads $\beta=(1.2,\,0.5)$. Taking $R_f\approx1$, what are its expected excess return and the discount-factor loadings $b$?
- 9.2% per year, with $b=(0.06,\,0.04)$, the factor means themselves.
- 5.0% per year, with $b=(2.67,\,2.78)$, since $b$ deflates the premium twice.
- 10.0% per year, with $b=(1.2,\,0.5)$, the loadings carried over unchanged.
- 9.2% per year, with $b=(2.67,\,2.78)$.
<!-- YW5zOjM= -->
> Traded factors give $\lambda=E[f]$, so $E[R^e]=1.2(0.06)+0.5(0.04)=9.2\%$. Then $b=\Sigma_F^{-1}\lambda$, componentwise here: $0.06/0.0225=2.67$ and $0.04/0.0144=2.78$. Note the reading: factor 2 has the *smaller* premium but the *larger* loading, because it is less volatile and so a more efficient carrier of priced risk per unit of variance.
> Ref: Ribeiro (2026), Ch. 6, §6.1.5 (pp. 193–194)
> Similar: Ribeiro, Problem 6.1 (p. 220)

Q: Consumption growth is not a traded return. What does the factor-mimicking portfolio construction buy, and what does it cost?
- It converts the factor into a traded one that prices identically, at the cost of discarding the projection residual — which prices nothing anyway.
- It converts the factor into a traded one, at the cost of assuming the residual is uncorrelated with consumption.
- It leaves $\lambda$ free but makes the betas observable, so the time-series test becomes available without further assumption.
- It raises the factor's Sharpe ratio to the tangency level, at the cost of requiring a complete market.
<!-- YW5zOjA= -->
> Regress $g_t$ on the excess returns and keep the fitted part $f^*_t=\beta'R^e_t$. By construction $f^*$ is a traded excess return, and it shares $g$'s covariances with every return up to a residual orthogonal to returns — and anything orthogonal to returns prices nothing. So the non-traded case always reduces to the traded case, and the whole time-series apparatus becomes available.
> Ref: Ribeiro (2026), Ch. 6, §6.1.4 (p. 193); §6.6.4 (p. 212)
> Similar: Ribeiro, True/False 3–4 (p. 222)

Q: The chapter says the pricing question, the discount-factor question, and the frontier question are one question in three languages. What is the frontier statement?
- Beta pricing holds if and only if each factor individually lies on the mean–variance frontier.
- Beta pricing holds for all assets if and only if some portfolio of the factors is mean–variance efficient.
- Beta pricing holds if and only if the market portfolio is the tangency portfolio of the factors.
- Beta pricing holds if and only if the factors are mutually uncorrelated and each carries a positive premium.
<!-- YW5zOjE= -->
> By the Hansen–Jagannathan duality of chapter 2, a discount factor and a mean–variance-efficient portfolio are two views of one object. Pricing by $m=a-b'f$ says a portfolio *formed from* the factors — not any single factor — spans the tangency portfolio. This is exactly why the GRS test turns out to measure whether the test assets improve on the factors' Sharpe ratio.
> Ref: Ribeiro (2026), Ch. 6, §6.1.5 (p. 194); §6.5.2 (p. 206); Ch. 2 (Hansen–Jagannathan)
> Similar: Ribeiro, Problem 6.5 (p. 221); True/False 17 (p. 223)

## apt

Q: In the APT's arbitrage step, two well-diversified portfolios share the same $\beta_p$ but have different intercepts. What makes the constructed position an arbitrage?
- It is zero-beta and positive-cost, so any positive return exceeds the risk-free rate.
- It short-sells the idiosyncratic risk of both legs, which is free by the law of one price.
- It is zero-cost, its factor exposure nets to zero, and its residual risk is negligible, yet it earns $\alpha^{(1)}-\alpha^{(2)}\neq0$.
- It exploits the fact that well-diversified portfolios must have equal Sharpe ratios in equilibrium.
<!-- YW5zOjI= -->
> Long one, short the other in equal amount: a dollar long funded by a dollar short is costless, equal betas make the factor exposure cancel exactly, and diversification has already killed the residuals. What remains is a certain, costless, nonzero return. Banishing it for *every* pair forces the intercept to depend on the portfolio only through its betas — which is beta pricing.
> Ref: Ribeiro (2026), Ch. 6, §6.2.1 (p. 195)
> Similar: Ribeiro, Problem 6.2 (p. 220); True/False 12 (p. 222)

Q: The APT delivers *approximate* beta pricing. Which statement states most precisely what the approximation concedes?
- Each individual asset's alpha is bounded by a constant that shrinks as $N$ grows.
- Alphas may be nonzero for well-diversified portfolios but must vanish for individual assets.
- Alphas are zero on average across assets, so the cross-sectional mean pricing error is exactly zero.
- The sum $\sum_i\alpha_i^2$ (in the residual-risk metric) is bounded, so alphas may be scattered but not numerous and aligned.
<!-- YW5zOjM= -->
> A portfolio built to exploit alphas earns a Sharpe ratio rising with $\sum_i\alpha_i^2/\text{var}(\varepsilon_i)$ — the same quadratic form GRS uses. No-arbitrage caps the Sharpe ratio available in the economy, hence caps that sum. So the APT bounds the *aggregate* pricing error, not each one: scattered violations are allowed, systematic ones are not.
> Ref: Ribeiro (2026), Ch. 6, §6.2.2 (p. 196), §6.2.3 (pp. 196–197)
> Similar: Ribeiro, Problem 6.2 (p. 221); True/False 12 (p. 222)

Q: Why is the APT's "arbitrage" really a *near*-arbitrage, and what does that cost the argument?
- Because the residual risk of a large but finite portfolio is small, not zero, so closing the gap needs investors with bounded risk aversion — an assumption.
- Because short-selling constraints prevent the position from being formed, so the argument needs a frictionless market.
- Because the factor loadings are estimated, so the exposures cancel only up to sampling error.
- Because the two portfolios' intercepts are only observable ex post, so the trade cannot be placed ex ante.
<!-- YW5zOjA= -->
> Perfect diversification is a limit, not a portfolio. With finitely many assets the position carries a little residual risk, so someone must be willing to take a *near*-riskless bet with positive expected return. Mild, but an assumption — and it turns the APT from a pure no-arbitrage result into a result about limited near-arbitrage that loosens where capital is constrained.
> Ref: Ribeiro (2026), Ch. 6, §6.2.2 (p. 196)
> Similar: Ribeiro, Problem 6.2 (p. 221)

Q: Chamberlain and Rothschild (1983) replaced the exact factor structure with an approximate one. What does the weaker condition require?
- That the residual covariance matrix be diagonal up to a set of pairs of measure zero.
- That the residual covariance matrix have a bounded largest eigenvalue as $N$ grows, while the factor block's eigenvalues diverge.
- That residual correlations be positive but individually below a fixed threshold for every pair.
- That the number of factors $K$ grow slowly with $N$, so the residual becomes asymptotically negligible.
<!-- YW5zOjE= -->
> Strict diagonality is too strong for real data — chapter 5 measured small but nonzero residual correlations across industries. The fix is spectral: residuals may be mildly cross-correlated in pairs, but their comovement must not itself add up to another pervasive factor. Under that weaker premise the well-diversified portfolio still sheds its residual risk and the arbitrage argument still bites.
> Ref: Ribeiro (2026), Ch. 6, §6.2.3 (p. 196); Chamberlain–Rothschild (1983)
> Similar: Ribeiro, Ch. 5, §5.4; True/False 12 (p. 222)

Q: Fama called the APT a "fishing licence". Which of the following does the APT genuinely fail to deliver?
- The linearity of expected returns in loadings, which requires an equilibrium argument instead.
- The requirement that the market portfolio be mean–variance efficient.
- The identity of the factors, their number $K$, and the sign or size of any $\lambda_k$.
- A distributional assumption on returns beyond the factor structure.
<!-- YW5zOjI= -->
> The APT says: *if* returns have a $K$-factor structure and near-arbitrage is absent, *then* approximate beta pricing holds. It names no $f$, fixes no $K$, and signs no premium. That looseness is precisely the theoretical root of the factor zoo — the theory licenses the search without saying what will be caught.
> Ref: Ribeiro (2026), Ch. 6, §6.2.2 (p. 196); Key result (p. 196); §6.7 (p. 213)
> Similar: Ribeiro, True/False 8, 10 (p. 222)

Q: Daniel and Titman (1997) held the HML loading fixed and asked whether book-to-market still predicted returns. What did they find, and what happened to the finding?
- The loading won; later work overturned it in favour of the characteristic.
- Neither won; the test proved underpowered and the design was abandoned.
- The characteristic won and has never been successfully challenged, settling the debate behaviourally.
- The characteristic won; Davis, Fama and French (2000) re-ran it on a longer sample and found the loading mattered after all.
<!-- YW5zOjM= -->
> The design is exactly right: find stocks with a high characteristic but a low loading, and the reverse, and see which predicts. Daniel–Titman found the characteristic won — evidence against the risk story. Davis–Fama–French, on a longer sample, found the loading mattered. The question is not settled, and the course's covariance stance is a working discipline, not a proof.
> Ref: Ribeiro (2026), Ch. 6, §6.2.4 (pp. 197–198); §6.7.3 (p. 216)
> Similar: Ribeiro, True/False 7 (p. 222)

## sorts

Q: What makes the portfolio sort a *nonparametric* test?
- It fits no functional form and assumes no pricing model; it just asks whether ranking on the characteristic separates returns.
- It uses ranks rather than levels, so it is invariant to the distribution of the characteristic.
- It requires no estimate of the covariance matrix, so no distributional assumption is needed for the standard error.
- It uses value weights rather than equal weights, which removes the need for a parametric size control.
<!-- YW5zOjA= -->
> Rank, split into deciles, hold, record, and form the long–short spread. No regression, no CAPM, no linearity in the characteristic. That is the sort's great virtue: it cannot be wrong about the pattern it displays, because it fits nothing. It is a direct look at the conditional mean return as a function of the characteristic.
> Ref: Ribeiro (2026), Ch. 6, §6.3.1 (p. 198)
> Similar: Ribeiro, Problem 6.3 (p. 220); True/False 11 (p. 222)

Q: Fama and French set decile breakpoints on NYSE stocks only, then apply them to the NYSE/AMEX/NASDAQ universe. Why?
- Because NYSE stocks have longer histories, so the breakpoints can be computed further back in time.
- Because AMEX and NASDAQ are thick with tiny firms, so all-stock breakpoints would pack the extreme portfolios with micro-caps and exaggerate the premium.
- Because NYSE listing requirements guarantee the accounting data are audited, removing look-ahead bias.
- Because value weighting is only well defined within a single exchange.
<!-- YW5zOjE= -->
> NYSE breakpoints are the standard guard against a spread that is really a micro-cap artefact. It is one of four design choices — with weighting, single-versus-double sorts, and rebalancing/timing — each of which can manufacture or destroy a premium, which is why a careful reader interrogates them before believing a number.
> Ref: Ribeiro (2026), Ch. 6, §6.3.2 (pp. 198–199)
> Similar: Ribeiro, Problem 6.3 (p. 220)

Q: In the book's decile value sort (1963–2026), the ten book-to-market deciles run 6.9, 7.8, 7.6, 6.9, 7.0, 8.7, 7.3, 9.3, 10.8, 11.5 %/yr. The spread earns 4.6%/yr with market beta 0.09. Why is its CAPM alpha (3.9%, $t=1.8$) so close to the raw premium?
- Because the CAPM alpha equals the raw premium whenever the spread is a zero-cost long–short portfolio.
- Because the market premium over this sample happened to be near zero.
- Because the spread carries almost no market beta, so there is virtually nothing for the CAPM to explain away.
- Because the value and growth deciles have equal Sharpe ratios, which forces the alpha to equal the mean.
<!-- YW5zOjI= -->
> $\alpha=\bar R^e-\beta\,\bar R^e_{mkt}\approx 4.6-0.09(7.2)\approx3.9\%$. Value and growth have nearly the same market exposure, so the risk adjustment removes almost nothing. That is the anomaly in miniature: a robust spread in average returns, orthogonal to market beta, that a one-factor model has nothing to say about.
> Ref: Ribeiro (2026), Ch. 6, §6.3.3, Example 6.1 (p. 199)
> Similar: Ribeiro, Problem 6.3 (p. 220)

Q: Only six of the nine decile-to-decile steps in that value sort are increases, and decile 4 earns less than decile 2. What is the right reading?
- The non-monotonicity refutes the value premium, since a genuine risk factor must order returns exactly.
- The middle deciles should be dropped and the spread recomputed on the extremes only.
- The wandering middle proves the characteristic is a proxy for size rather than value.
- The pattern is a tendency, not a staircase — the honest texture of real anomaly data, and it does not invalidate the spread.
<!-- YW5zOjM= -->
> The book is explicit that the rise is not perfectly monotone and calls it typical. Perfect monotonicity would strengthen the evidence; a single wandering middle decile is noise, not refutation. What the spread establishes is an *association* between the characteristic and average returns in the sample — no more, and no less.
> Ref: Ribeiro (2026), Ch. 6, §6.3.3 (p. 199), §6.3.5 (p. 202)
> Similar: Ribeiro, Problem 6.3 (p. 220); True/False 14 (p. 222)

Q: A clean, monotone, high-$t$ decile spread is displayed. Which conclusion does it license?
- That the characteristic is associated with average returns in this sample, robustly and without a model.
- That the characteristic captures a priced risk, since the spread has no market beta.
- That the premium will survive out of sample, since monotonicity rules out data-snooping.
- That the premium is earnable, since the long–short portfolio is by construction zero-cost.
<!-- YW5zOjA= -->
> That is exactly what "nonparametric" delivers and all it delivers. The sort does *not* establish that the characteristic captures a risk (covariance or characteristic — the sort cannot tell), that the premium survives trading costs (turnover, micro-caps), that it is not data-snooped, or that it will persist. Treat a significant spread as the beginning of the argument.
> Ref: Ribeiro (2026), Ch. 6, §6.3.5 (p. 202); Common pitfalls (p. 219)
> Similar: Ribeiro, Problem 6.3 (p. 220); True/False 14 (p. 222)

Q: Which pairing of evidence factor and its book verdict is correct?
- Size is the strongest of the five, appearing in every asset class and country ever examined.
- Size is the weakest survivor — 1.7%/yr with $t=1.3$ in the book's sample, kept mainly for history and for its role in the FF construction.
- Momentum is the weakest, since its crashes cancel its premium over long samples.
- Profitability is the weakest, since the dividend-discount identity gives it no independent content.
<!-- YW5zOjE= -->
> The book's verdicts: market not in doubt (7.2%, $t=3.7$); value real but feeble since the early 2000s; momentum statistically the most robust and the hardest to *earn* (turnover, crashes); profitability and investment replicate well with the tidiest valuation rationale; size statistically indistinguishable from zero.
> Ref: Ribeiro (2026), Ch. 6, §6.3.4 (pp. 199–201); §6.8.1 (p. 217)
> Similar: Ribeiro, True/False 16 (p. 223)

Q: The valuation rationale that RMW and CMA share starts from the dividend-discount identity. Holding book-to-market fixed, what does it predict?
- Higher expected profitability and higher expected investment both mean higher expected return.
- Higher expected profitability means lower expected return, since profitable firms are safer.
- Higher expected profitability means higher expected return; higher expected investment means lower expected return.
- The identity is silent on expected returns unless the payout ratio is also fixed.
<!-- YW5zOjI= -->
> Pure accounting turned into a prediction. Two firms priced the same relative to book: if one has a larger stream of future earnings, that stream must be discounted more heavily — a higher expected return. Symmetrically, extra book value plowed into investment must be discounted more heavily to leave the price unchanged. This is also why HML becomes partly redundant once RMW and CMA are present.
> Ref: Ribeiro (2026), Ch. 6, §6.3.4 (p. 201); §6.4.3 (p. 203)
> Similar: Ribeiro, True/False 13 (p. 222)

## ff

Q: The $2\times3$ sorts give six portfolios S/L, S/M, S/H, B/L, B/M, B/H. How are SMB and HML defined?
- SMB averages the two small-value minus the two big-growth; HML averages the three high minus the three low.
- SMB is S/H − B/L; HML is B/H − S/L, the diagonal spreads.
- SMB averages the three small minus the three big; HML averages the three high minus the three low.
- SMB averages the three small minus the three big; HML averages the two high minus the two low.
<!-- YW5zOjM= -->
> $\text{SMB}=\tfrac13(S/L+S/M+S/H)-\tfrac13(B/L+B/M+B/H)$ and $\text{HML}=\tfrac12(S/H+B/H)-\tfrac12(S/L+B/L)$. Three groups on the value dimension (30th/70th NYSE percentiles) but two on size (NYSE median) — hence thirds for SMB and halves for HML. Item 9 of the book's True/False bank is exactly this asymmetry.
> Ref: Ribeiro (2026), Ch. 6, §6.4.1 (p. 202), eqs. (6.13)–(6.14)
> Similar: Ribeiro, Problem 6.4 (p. 221); True/False 9 (p. 222)

Q: In one month the six portfolios return S/L = 1.0, S/M = 1.6, S/H = 2.2, B/L = 0.6, B/M = 0.9, B/H = 1.1 (percent). What are SMB and HML, and what does the averaging buy?
- SMB = 0.73%, HML = 0.85%; the averaging differences the size tilt out of the value factor and vice versa.
- SMB = 0.73%, HML = 0.85%; the averaging raises both premia by pooling more stocks.
- SMB = 1.60%, HML = 1.65%; the averaging is cosmetic, since the six portfolios are value-weighted anyway.
- SMB = 1.6%, HML = 1.6%; both equal the naive spread S/H − B/L.
<!-- YW5zOjA= -->
> $\text{SMB}=1.60-0.867=0.73$; $\text{HML}=1.65-0.80=0.85$. The value effect is far stronger among small firms ($1.2$) than big ($0.5$); by taking value spreads *within* each size group and then averaging, HML reports a clean value premium uncontaminated by the fact that small stocks did well. The naive $S/H-B/L=1.6$ would measure value *plus* size.
> Ref: Ribeiro (2026), Ch. 6, §6.4.1 (p. 203)
> Similar: Ribeiro, Problem 6.4 (p. 221)

Q: What does a *spanning regression* test, and what did it say about HML in the five-factor model?
- Regress the incumbents on the candidate and test the $R^2$; HML's $R^2$ is near one, so it is redundant.
- Regress the candidate on the incumbents and test its intercept; HML's alpha against MKT, SMB, RMW and CMA is small and insignificant, so it is nearly redundant.
- Test whether the candidate's own premium is significant; HML's is 3.5% with $t=2.7$, so it is retained.
- Test whether the candidate's beta on each incumbent is zero; HML loads on RMW, so it is dropped.
<!-- YW5zOjE= -->
> A spanning regression is the time-series alpha test with a *factor* as the test asset: $g$ adds pricing power beyond $f$ exactly when its own alpha against $f$ is nonzero. HML is spanned by the other four; RMW and CMA retained large alphas against the original three, which is what earned them a place. A factor model is a race against incumbents.
> Ref: Ribeiro (2026), Ch. 6, §6.4.3 (pp. 203–204)
> Similar: Ribeiro, True/False 13 (p. 222)

Q: Momentum is excluded from FF3 and FF5 but included in the Carhart benchmark. What is the tension?
- It has the weakest evidence and the cleanest risk story, so theory keeps it while the data reject it.
- It is not a traded excess return, so its price of risk cannot be read off its mean.
- It has the strongest, most pervasive evidence and the least defensible risk story — negatively skewed returns with rare, violent crashes, closer to writing insurance than buying it.
- Its premium is entirely captured by SMB and HML, so it adds nothing to FF3 in a spanning test.
<!-- YW5zOjI= -->
> Momentum delivers one of the highest Sharpe ratios of any factor, in nearly every market and asset class. But a risk factor should pay for doing badly in bad times, and momentum crashes in sharp rebounds *after* a crash, when the beaten-down losers it is short rocket up. Fama and French leave it out for that reason; practitioners keep it because a manager cannot be judged without controlling for so pervasive a tilt.
> Ref: Ribeiro (2026), Ch. 6, §6.4.3 (p. 204); Ch. 7
> Similar: Ribeiro, Problem 6.8 (p. 222); True/False 16 (p. 223)

Q: Chen, Roll and Ross (1986) used macroeconomic series as factors. What follows for how their model must be tested?
- Their factors are not traded returns, so the GRS test applies with the intercepts read as pricing errors.
- Their factors are traded once industrial production is expressed as a growth rate, so either test applies.
- No test applies, since the ICAPM licenses their factors on theoretical grounds alone.
- Their factors are not traded returns, so $\lambda$ is free and must be estimated cross-sectionally by Fama–MacBeth.
<!-- YW5zOjM= -->
> The traded/non-traded fault line decides which test is available. A traded factor pins its own price of risk, $\lambda_k=E[f_k]$, making the pricing error an observable intercept. A macroeconomic series pins nothing, so $\lambda$ becomes a vector of unknowns — which is precisely the job of the second pass. (Alternatively, mimic it first; §6.1.4.)
> Ref: Ribeiro (2026), Ch. 6, §6.4.4 (pp. 204–205); §6.1.4 (p. 193)
> Similar: Ribeiro, True/False 3–4 (p. 222)

## grs

Q: With traded factors, why *is* the time-series intercept the pricing error?
- Because $\lambda=E[f]$ is imposed by tradedness, so $\alpha_i=E[R^e_i]-\beta_i'E[f]$ is exactly the gap beta pricing says must vanish.
- Because OLS forces the residual to be orthogonal to the factors, which makes the intercept unbiased.
- Because the factors are zero-cost, so the regression has no constant to absorb the mean.
- Because the residual covariance matrix is diagonal, so each intercept is estimated independently.
<!-- YW5zOjA= -->
> Take expectations of the regression: $E[R^e_i]=\alpha_i+\beta_i'E[f]$. Tradedness supplies $\lambda=E[f]$, so $\alpha_i$ is the part of the mean excess return that the loadings, valued at the factors' own means, do not explain. Testing the model becomes testing whether a set of observable regression intercepts is zero — the whole apparatus of §6.5 rests on this convenience.
> Ref: Ribeiro (2026), Ch. 6, §6.1.1 (p. 191), §6.5.1 (pp. 205–206)
> Similar: Ribeiro, True/False 5 (p. 222)

Q: Why is "count how many of the 25 alphas are individually significant" not a test of the model?
- Because individual $t$-statistics are biased upward when the residuals are correlated.
- Because under the null that the model is true, one or two significant $t$-statistics out of 25 are expected at the 5% level.
- Because individual alphas cannot be estimated without the full residual covariance matrix.
- Because the null is that alphas are *jointly* nonzero, which no individual test can address.
<!-- YW5zOjE= -->
> With $N=25$ and a 5% threshold, a scatter of significant $t$'s neither confirms nor rejects. What is wanted is a single joint test of $\alpha_1=\cdots=\alpha_N=0$. In the book's FF3 example only 6 of 25 individual alphas are significant, and yet GRS rejects decisively — because the errors, though individually modest, are correlated and point the same way.
> Ref: Ribeiro (2026), Ch. 6, §6.5.1 (p. 206); Common pitfalls (p. 219)
> Similar: Ribeiro, Problem 6.5 (p. 221); True/False 18, 20 (p. 223)

Q: The GRS numerator is $\hat\alpha'\hat\Sigma_\varepsilon^{-1}\hat\alpha$ and the denominator is $1+\bar\mu_f'\hat\Sigma_F^{-1}\bar\mu_f$. What does the numerator equal, exactly?
- The maximum squared Sharpe ratio attainable from the test assets alone.
- The average squared alpha across the $N$ test assets, scaled by residual variance.
- The increase in the maximum squared Sharpe ratio obtained by adding the $N$ test assets to the $K$ factors.
- The share of the test assets' variance left unexplained by the factors.
<!-- YW5zOjI= -->
> The theorem is $\theta^2(f,R)-\theta^2(f)=\hat\alpha'\hat\Sigma_\varepsilon^{-1}\hat\alpha$. So a model prices the cross-section precisely when its factors already span the tangency portfolio: if the assets cannot raise the maximum Sharpe ratio, their alphas are zero, and conversely. Nonzero alphas *are* the unexploited Sharpe-ratio improvement.
> Ref: Ribeiro (2026), Ch. 6, §6.5.2 (p. 206)
> Similar: Ribeiro, Problem 6.5 (p. 221); True/False 17 (p. 223)

Q: A three-factor model on $N=25$ portfolios over $T=600$ months has $\hat\alpha'\hat\Sigma_\varepsilon^{-1}\hat\alpha=0.19$ and factor squared Sharpe $0.035$ (monthly). What is the GRS statistic and its distribution?
- $\text{GRS}=\frac{600-25-3}{25}\cdot 0.19\cdot 1.035=4.50\sim F(25,572)$ — rejected.
- $\text{GRS}=\frac{600}{25}\cdot\frac{0.19}{1.035}=4.41\sim F(25,600)$ — rejected.
- $\text{GRS}=\frac{600-25-3}{25}\cdot\frac{0.19}{0.035}=124\sim F(25,572)$ — rejected overwhelmingly.
- $\text{GRS}=\frac{600-25-3}{25}\cdot\frac{0.19}{1.035}=4.20\sim F(25,572)$ — rejected at 5%, since the critical value is about 1.53.
<!-- YW5zOjM= -->
> $(T-N-K)/N=572/25=22.88$; $0.19/1.035=0.1836$; the product is $\approx4.20$, far above $1.53$. Read the pieces: the numerator is the correlation-adjusted size of the pricing errors, the denominator normalizes by what the factors themselves already deliver, and the assets improve the maximum squared Sharpe ratio by 0.19 per month.
> Ref: Ribeiro (2026), Ch. 6, §6.5.2 (p. 206), eq. (6.17)
> Similar: Ribeiro, Problem 6.5 (p. 221)

Q: On the 25 size/value portfolios (1963–2026), CAPM gives GRS $=4.13$ ($p=1.4\times10^{-10}$, mean $|\alpha|=2.3\%$) and FF3 gives $3.58$ ($p=1.4\times10^{-8}$, mean $|\alpha|=1.1\%$). What is the honest verdict?
- FF3 prices the bulk of the cross-section that defeated the CAPM and is still statistically rejected — "rejected" and "useless" are different verdicts.
- FF3 passes, since halving the average pricing error is the operative criterion.
- Both models are useless, since both are rejected at any conventional level.
- The comparison is void, since the two tests have different denominator degrees of freedom.
<!-- YW5zOjA= -->
> Two extra factors roughly halve the pricing errors and the model is still rejected decisively. The chapter's discipline: a model can fail a sharp joint test and still be the best available description of expected returns. Mistaking rejection for uselessness is one of the chapter's named pitfalls.
> Ref: Ribeiro (2026), Ch. 6, §6.5.3, Example 6.2 (p. 207); Common pitfalls (p. 219)
> Similar: Ribeiro, True/False 20 (p. 223)

Q: FF3's worst pricing error on the 25 portfolios is the small-growth corner, $\alpha=-5.6\%$/yr with $t=-5.0$. Why does the chapter call the failure *diagnostic* rather than merely embarrassing?
- Because a single outlier can be removed without changing the joint test's verdict.
- Because the failures cluster on a recognizable economic type — small, expensive, capital-hungry firms — which tells you what the model omits and motivated RMW and CMA.
- Because the alpha is negative, and negative alphas are not exploitable by a long-only investor.
- Because the corner portfolio has the smallest market capitalization and so the least economic weight.
<!-- YW5zOjE= -->
> A model that failed on a random scatter would be a nuisance; one that fails on a coherent economic type is telling you what it left out. The failures run along the growth edge and the smaller size quintiles, their residuals are positively correlated, and so the alphas *reinforce* rather than cancel in $\hat\alpha'\hat\Sigma_\varepsilon^{-1}\hat\alpha$ — which is why GRS rejects where 6-of-25 looks benign.
> Ref: Ribeiro (2026), Ch. 6, §6.5.3 (p. 207); §6.4.3 (p. 203)
> Similar: Ribeiro, True/False 19 (p. 223)

Q: The GRS statistic requires inverting the $N\times N$ residual covariance matrix. What practical limit does that impose?
- $N>K$ only, since the residual matrix is always full rank once the factors are removed.
- $T>2N$, a rule of thumb needed for the $F$ distribution to be exact.
- $N<T-K$, and in practice $N$ comfortably below $T$ — which is why the standard test assets are a few dozen portfolios, not thousands of stocks.
- No limit, since the statistic can be computed from the diagonal of the residual matrix alone.
<!-- YW5zOjI= -->
> When $N$ is large relative to $T$, $\hat\Sigma_\varepsilon$ is noisy or singular and the test loses power. The correlation structure is essential, not optional — using only the diagonal would ignore exactly the alignment of errors that makes the joint test reject. For large $N$ the route is a Sharpe-ratio or GMM test, named above the course's OLS ceiling.
> Ref: Ribeiro (2026), Ch. 6, §6.5.2 (pp. 206–207)
> Similar: Ribeiro, Problem 6.5 (p. 221)

## fm

Q: In Fama–MacBeth, what does each pass estimate?
- First pass: the prices of risk from a pooled regression. Second pass: the betas, asset by asset.
- First pass: the betas. Second pass: a single cross-sectional regression on the full-sample average returns.
- First pass: the factor means. Second pass: the alphas, as intercepts of the cross-sectional fit.
- First pass: each asset's betas from a time-series regression. Second pass: one cross-sectional regression of returns on those betas, per period, giving a time series of $\hat\lambda_t$.
<!-- YW5zOjM= -->
> Turn the panel on its side. The regressors in the second pass are the estimated betas, one row per asset; the coefficients $\lambda_t$ are that period's realized prices of risk, and $\gamma_{0t}$ the zero-beta excess return. Running it every period yields $T$ estimates of each price of risk.
> Ref: Ribeiro (2026), Ch. 6, §6.6.1 (p. 209), eqs. (6.18)–(6.19)
> Similar: Ribeiro, Problem 6.6 (pp. 221–222); True/False 21 (p. 223)

Q: The Fama–MacBeth standard error is $\text{std}_t(\hat\lambda_{kt})/\sqrt{T}$. Why is that legitimate despite the strong cross-sectional correlation of returns within a period?
- Because whatever the within-period correlation is, it is baked into each $\hat\lambda_{kt}$, and variation across independent periods delivers a correct standard error with no covariance model needed.
- Because cross-sectional correlation cancels between the first and second passes.
- Because the betas are fixed regressors, which makes the within-period errors conditionally independent.
- Because with $T$ large the cross-sectional correlation is asymptotically negligible.
<!-- YW5zOjA= -->
> This is the device worth admiring. Each period's slope is treated as one draw; its sampling distribution already reflects however correlated the $N$ returns were that month. Averaging over time and reading the scatter gives the standard error *automatically* — one reason the procedure sits comfortably at the OLS ceiling.
> Ref: Ribeiro (2026), Ch. 6, §6.6.1 (p. 209), eq. (6.20)
> Similar: Ribeiro, Problem 6.6 (p. 222); True/False 22–23 (p. 223)

Q: In one month, four assets with betas $(0.7,\,0.9,\,1.1,\,1.3)$ realize excess returns $(0.5,\,1.4,\,1.6,\,2.5)\%$. What is that month's cross-sectional slope and intercept?
- $\lambda_{1t}=0.62\%$ and $\gamma_{0t}=1.5\%$.
- $\lambda_{1t}=3.1\%$ and $\gamma_{0t}=-1.6\%$.
- $\lambda_{1t}=1.5\%$ and $\gamma_{0t}=0.20\%$.
- $\lambda_{1t}=2.0\%$ and $\gamma_{0t}=-0.5\%$.
<!-- YW5zOjE= -->
> $\bar\beta=1.0$, deviations $(-0.3,-0.1,0.1,0.3)$ with squares summing to $0.20$; $\bar R^e=1.5$, deviations $(-1.0,-0.1,0.1,1.0)$; cross-product $0.62$. So $\lambda_{1t}=0.62/0.20=3.1\%$ and $\gamma_{0t}=1.5-3.1(1.0)=-1.6\%$. Do this every month: the swings average to $\hat\lambda$ and their scatter delivers the standard error.
> Ref: Ribeiro (2026), Ch. 6, §6.6.1 (pp. 209–210)
> Similar: Ribeiro, Problem 6.6 (pp. 221–222)

Q: Fama–MacBeth with FF3 on the 25 size/value portfolios gives $\hat\lambda_{mkt}=-6.6\%$/yr ($t=-1.8$) against the market factor's own mean of $+7.2\%$. What is the correct diagnosis?
- A coding error: a wrong-signed market premium cannot arise from correctly executed OLS.
- The market factor is not priced, and the negative estimate is the model's honest verdict.
- The 25 portfolios have market betas bunched near one, so there is almost no cross-sectional spread for the second pass to price; the coefficient is badly identified, and the flat SML reappears.
- The Shanken correction has not been applied, and applying it restores the positive sign.
<!-- YW5zOjI= -->
> A factor is identified in the cross-section only when the test assets *spread* on its beta. Size-value portfolios were built to vary on size and value, not beta. The large positive intercept, 13.9%/yr, is the flip side: it absorbs the market return the near-flat beta cannot. Sort on beta instead and the premium comes out sensibly positive — but too flat, which is what Betting-Against-Beta harvests in chapter 7.
> Ref: Ribeiro (2026), Ch. 6, §6.6.3, Example 6.3 (pp. 210–211); Common pitfalls (p. 219); Ch. 4, §4.5
> Similar: Ribeiro, True/False 24–25 (p. 223)

Q: In the same table $\hat\lambda_{HML}=3.9\%$ ($t=2.9$) against HML's own mean of 3.5%. Why is that comparison the point of the exercise?
- Because a cross-sectional estimate above the factor mean signals that HML is mispriced by the market.
- Because the two numbers must be equal exactly, and a 0.4 point gap is evidence against FF3.
- Because HML is not traded, so the cross-sectional estimate is the only available reading of its premium.
- For a traded factor beta pricing requires $\lambda=E[f]$, so the cross-sectional estimate matching the factor's mean is the model's own consistency check.
<!-- YW5zOjM= -->
> The time-series and cross-sectional tests should agree for a traded factor, and comparing them is itself a diagnostic. Value is priced *and priced about right*. The 0.4-point gap is well inside a standard error; what would be damning is the market's $-6.6\%$ against $+7.2\%$ — and that turned out to be an identification failure, not a pricing verdict.
> Ref: Ribeiro (2026), Ch. 6, §6.6.1 (p. 210), §6.6.3 (p. 211); §6.5 (p. 205)
> Similar: Ribeiro, Problem 6.4 (p. 221)

Q: The second-pass regressors are estimated betas. What are the two consequences and the standard correction?
- Attenuation of the slopes toward zero and naive standard errors that are too small; Shanken (1992) inflates the price-of-risk variances by $1+\lambda'\Sigma_F^{-1}\lambda$.
- Attenuation of the slopes and standard errors that are too large; Shanken deflates them by $1-\lambda'\Sigma_F^{-1}\lambda$.
- Inflation of the slopes away from zero and standard errors that are too small; the Newey–West correction is the fix.
- No bias in the slopes but inconsistent standard errors; using portfolios instead of individual stocks is the only remedy.
<!-- YW5zOjA= -->
> Classical errors-in-variables: a mismeasured regressor attenuates its slope, and the naive standard errors ignore first-pass estimation uncertainty. The Shanken multiplier is one plus the factors' squared Sharpe ratio — the same object as the GRS denominator. Using portfolios rather than individual stocks is the practical remedy that shrinks the problem at source.
> Ref: Ribeiro (2026), Ch. 6, §6.6.2 (p. 210), eq. (6.21)
> Similar: Ribeiro, Problem 6.6 (p. 222); True/False 27, 29 (p. 224)

Q: For FF3 the Shanken multiplier is $1.03$, so standard errors widen by about 1.5%. What is the right lesson to draw?
- The correction is a formality that can be safely omitted in applied work.
- Compute the multiplier every time and let it tell you whether it matters; it bites when factors have high Sharpe ratios or samples are short.
- The correction is always small, because squared Sharpe ratios are bounded below one.
- The correction matters only when the number of test assets exceeds the number of periods.
<!-- YW5zOjE= -->
> The multiplier grows with the factors' Sharpe ratio because errors in betas matter more when betas earn more. The FF3 monthly squared Sharpe is only about 0.03 — comfortable, but that is a fact about *these* factors, not a law. A model of many high-Sharpe factors, or short samples with poorly pinned betas, is where the naive standard errors substantially understate the truth.
> Ref: Ribeiro (2026), Ch. 6, §6.6.2 (p. 210); Common pitfalls (p. 219)
> Similar: Ribeiro, True/False 29 (p. 224)

Q: "Regression is projection" is the chapter's slogan. What do the betas and the alpha correspond to, geometrically?
- The betas are the residual and $\alpha_i$ the projection, which is why alpha carries the risk.
- The betas are the eigenvalues of $\Sigma_F$ and $\alpha_i$ the corresponding eigenvector loading.
- The betas are the coordinates of the projection of $R^e_i$ onto the factor span; $\alpha_i$ is the part of the mean lying *outside* that span.
- The betas span the tangency portfolio and $\alpha_i$ measures the distance to the minimum-variance portfolio.
<!-- YW5zOjI= -->
> Decompose $R^e_i=\beta_i'f+(\alpha_i+\varepsilon_i)$ with $\varepsilon_i\perp f$. The projection governs comovement and risk (chapter 5's job); the leftover of the mean governs pricing (chapter 6's). GRS measures the length of the mean that spills outside the factor span; Fama–MacBeth measures the slope of mean return along the beta directions. Two readings of one projection.
> Ref: Ribeiro (2026), Ch. 6, §6.6.4 (pp. 212–213), Key result (p. 213); Appendix A
> Similar: Ribeiro, Problem 6.5 (p. 221)

## zoo

Q: A researcher reports a factor with $t=2.5$, selected after the literature has tried hundreds of characteristics. Why is the Harvey–Liu–Zhu $t>3$ bar the right response, and what is it *not*?
- It is a stricter standard of proof for every test, reflecting that finance data are noisier than other fields'.
- It is a Bonferroni bound, testing each of $M$ candidates at level $0.05/M$.
- It is a requirement that the factor replicate out of sample, expressed as a $t$-statistic.
- It is a correction for the multiplicity of the search, calibrated to keep the false-discovery rate small — not a stricter standard of proof for a single pre-specified test.
<!-- YW5zOjM= -->
> A pre-specified single test at $t>2$ remains perfectly valid. What is invalid is reading a *selected* $t$ as if it were pre-specified. Of 300 null candidates, the 5% bar certifies about 15 spurious discoveries and the $t>3$ bar under one — the false-discovery rate collapses from roughly 30% to a few percent while almost all genuine factors survive.
> Ref: Ribeiro (2026), Ch. 6, §6.7.1 (pp. 213–214); Common pitfalls (p. 219)
> Similar: Ribeiro, Problem 6.7 (p. 222); True/False 26, 30 (pp. 223–224)

Q: The book's placebo experiment sorts 48 industry portfolios on a random score 2000 times. What happened, and what does the excess over the nominal rate teach?
- 10.5% cleared $|t|>1.96$ and 0.9% cleared $t>3$; real returns are fatter-tailed and more cross-correlated than the normal null, so naive $t$-tests over-reject even more than the arithmetic says.
- Exactly 5% cleared $|t|>1.96$, confirming the null and showing the $t>3$ bar is unnecessary.
- 10.5% cleared $|t|>1.96$ because the random scores were correlated with returns by construction.
- 0.9% cleared $t>3$, which is below the nominal rate, showing that industry portfolios are unusually well behaved.
<!-- YW5zOjA= -->
> The nominal rates are about 4.6% and 0.27%; the realized ones are 10.5% and 0.9%, and the largest placebo $t$ reaches 4.4. Sorting on pure noise produces a "significant" strategy one time in ten. A literature mining thousands of real characteristics will certify hundreds of spurious factors, and the figure shows even the $t>3$ bar is only a partial defence.
> Ref: Ribeiro (2026), Ch. 6, §6.7.1, Example 6.4 (p. 214), Figure 6.4 (p. 215)
> Similar: Ribeiro, Problem 6.7 (p. 222); True/False 28 (p. 224)

Q: The "garden of forking paths" is the subtle form of p-hacking. Why does it ensnare honest researchers who run a single analysis?
- Because a single analysis has no multiplicity, so the problem is really publication bias in disguise.
- Because the reported $t$ treats the realized path as the only one, while the true sampling distribution is over all the defensible choices that would have been made in other datasets.
- Because pre-registration removes the problem entirely, so any unregistered study is dishonest.
- Because researchers systematically choose equal weighting, which inflates every premium.
<!-- YW5zOjE= -->
> Sample period, breakpoints, weighting, lag length, whether to exclude financials or micro-caps — dozens of defensible choices, each of which would have been made differently had the data come out differently. That wider distribution has fatter tails, so the true $t$ is smaller than the reported one even with no cherry-picking. Fresh data collapses all the forking paths into one.
> Ref: Ribeiro (2026), Ch. 6, §6.7.2 (pp. 214–216)
> Similar: Ribeiro, Problem 6.7 (p. 222)

Q: McLean and Pontiff (2016) and Hou, Xue and Zhang (2020) are the chapter's empirical arbiters. What did they find?
- Premia decay about 58% out of sample and 26% post-publication; and about 35% of anomalies fail to replicate.
- Premia are stable out of sample but halve after publication; and all anomalies replicate under value weighting.
- Premia decay about 26% out of sample and 58% post-publication; and about 65% of nearly 450 re-tested anomalies fail $|t|>1.96$ under a micro-cap-robust, value-weighted protocol.
- Premia rise after publication as capital crowds in; and re-testing confirms about 65% of anomalies.
<!-- YW5zOjI= -->
> Decay out of sample points to over-fitting (the in-sample premium was partly luck); decay after publication points to arbitrage (capital floods in). Either way the published number is a high-water mark, not an expectation. Hou–Xue–Zhang show most of the zoo was inflated by micro-cap tilts and equal weighting. This is why the survivor list of §6.8.1 is so short.
> Ref: Ribeiro (2026), Ch. 6, §6.7.2 (p. 216); §6.8.1 (p. 217)
> Similar: Ribeiro, Problem 6.3 (p. 220); True/False 26 (p. 223)

Q: Suppose a factor survives every multiple-testing correction and replicates out of sample. What have the chapter's tests settled?
- Both its statistical reality and that it is a risk premium, since replication rules out mispricing.
- Neither, since replication on new data is itself a form of data-snooping.
- Its cause but not its magnitude, which requires a structural model of marginal utility.
- Its statistical reality, but not its cause — risk or mispricing remains open, and the tests are silent on it.
<!-- YW5zOjM= -->
> The chapter delivers a method, a verdict on the leading models, and an unresolved interpretation — and carrying all three at once is the mark of understanding it. The behavioural reading carries the extra obligation of explaining why arbitrageurs have not competed the premium away, which is where limits to arbitrage enter and where the two views make *different* predictions about where a premium should be found.
> Ref: Ribeiro (2026), Ch. 6, §6.7.3 (pp. 216–217); §6.8 (pp. 218–219); §6.2.4 (p. 197)
> Similar: Ribeiro, True/False 7 (p. 222)

Q: What is the bridge to chapter 7, stated exactly?
- Factor premia are available to anyone for the cost of holding the factor portfolios, so a fund's return splits into a replicable $\beta'\lambda$ and a residual $\alpha$ — the sharpened definition of skill.
- Factor premia are unavailable to retail investors, so a fund's whole excess return measures skill.
- A fund's Sharpe ratio replaces alpha once multiple factors are present, since alpha is not scale-free.
- Chapter 7 abandons factor models in favour of raw excess returns, since factor benchmarks are rejected.
<!-- YW5zOjA= -->
> Skill is not beating the market; it is beating what the fund's factor tilts would have delivered mechanically. Chapter 5 restricted $\Sigma$ and left $E[R]$ free; chapter 6 restricted $E[R]$ and built the tests; chapter 7 turns the same time-series regression on managers. Betting-Against-Beta is §6.6.3's flat SML made tradeable.
> Ref: Ribeiro (2026), Ch. 6, §6.8.2 (p. 218), Key result (p. 218)
> Similar: Ribeiro, Problem 6.8 (p. 222)

Q: The commonest error carried in from chapter 5 is the confusion of the two jobs. Which pair of facts refutes it in both directions?
- Industry factors are priced but useless for covariance; principal components are the only factors that do both jobs.
- Industry factors are essential for risk and carry no premium; a factor with tiny variance can be priced yet irrelevant to any portfolio's covariance.
- A factor that structures $\Sigma$ must be priced, but a priced factor need not structure $\Sigma$.
- A priced factor must structure $\Sigma$, but a covariance factor need not be priced.
<!-- YW5zOjE= -->
> The two jobs are logically independent, and the refutation runs both ways. Chapter 6 tests *pricing*; whether a factor also belongs in a risk model is a separate question with a separate answer. This is the book's first-listed common pitfall for chapter 6 and item 6 of its True/False bank.
> Ref: Ribeiro (2026), Ch. 6, Common pitfalls (p. 219); Ch. 5, §5.1
> Similar: Ribeiro, True/False 6 (p. 222)
