---
quiz: "Session 5 — Factor Models for Risk (conceptual, no arithmetic)"
tags:
  jobs: "1 · The Two Jobs and the Discount Factor"
  diag: "2 · Rank-One Plus Diagonal"
  port: "3 · Portfolio Risk, Diversification, and Active Risk"
  multi: "4 · Multifactor Risk Models"
  payoff: "5 · The Payoff and Its Limit"
  notclaim: "6 · What a Risk Model Does Not Claim"
---

## jobs

Q: A colleague sums up chapter 5 as "knowing which moment you are restricting." Which moment does a risk model restrict, and what does it leave free?
- It restricts the first moments $E[R^e]$ and leaves the second moments $\Sigma$ free to any estimator.
- It restricts both moments at once, since one regression delivers the betas and the intercepts together.
- It restricts the second moments $\Sigma$ and leaves expected returns and alphas entirely free.
- It restricts the discount factor $m_{t+1}$, from which both moments follow once preferences are fixed.
<!-- YW5zOjI= -->
> A risk model is a claim about $\Sigma$ and nothing else. The intercepts $\alpha_i$ of the factor regression are free parameters the risk model neither estimates nor constrains; restricting them is chapter 6's job. The regression is shared, the claims are not.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153), §5.6.1 (p. 178)
> Similar: Ribeiro, Problem 5.4 (p. 184); True/False 1–30 (pp. 185–187)

Q: In the language of $p_t = E_t[m_{t+1}x_{t+1}]$, where does a risk model sit?
- It describes the joint distribution of the payoffs $x_{t+1}$ and says nothing at all about $m_{t+1}$.
- It specifies $m_{t+1}$ as a linear function of the factors and leaves the payoff distribution free.
- It fixes the covariance term $\text{cov}_t(m_{t+1},x_{t+1})$ and lets the risk-free rate absorb the rest.
- It restricts neither object, since a covariance matrix is a statistic outside the pricing equation.
<!-- YW5zOjA= -->
> Every pricing model — consumption, CAPM, multifactor — is a theory of $m_{t+1}$, hence of first moments. A risk model is a statement about how the payoffs move together, and it stands whether the market is efficient, inefficient, rational or mad.
> Ref: Ribeiro (2026), Ch. 5, §5.1.3 (p. 154); Ch. 1, §1.4; Cochrane (2005), Ch. 9
> Similar: Ribeiro, Problem 5.4 (p. 184)

Q: A factor model reproduces realized correlations closely but leaves large systematic intercepts in the time-series regressions. Judged as a risk model and then as a returns model, what verdict does each job return?
- It fails both, since intercepts and correlation errors are two readings of one misspecification.
- It fails as a risk model and passes as a returns model, since intercepts are what measure covariance fit.
- It passes both, since a factor model is never asked to deliver zero intercepts in any application.
- It passes as a risk model and fails as a returns model, since each job is judged on a different moment.
<!-- YW5zOjM= -->
> Correlation fit is the second-moment test; systematic alphas condemn the first-moment claim. A model can pass one and fail the other, which is why the chapter insists on naming the job before pronouncing the verdict.
> Ref: Ribeiro (2026), Ch. 5, §5.1.1 (p. 153); Common pitfalls (p. 182)
> Similar: Ribeiro, Problem 5.4 (p. 184)

Q: Chapter 4 found the empirical security market line too flat. Why does that not condemn the single-index model as a risk model?
- It does condemn it: a flat security market line refutes the market factor for both jobs at once.
- A flat line condemns the market factor's pricing claim, not its power to generate covariances.
- A flat line means the betas are mismeasured, so the covariance matrix built from them is wrong too.
- A flat line makes the market portfolio inefficient, which leaves $\sigma_m^2\beta\beta^\top+D$ singular.
<!-- YW5zOjE= -->
> The flat line is a statement about the cross-section of *means*: high-beta assets do not earn what the model promises. The same betas can still organize $\Sigma$ beautifully. The single-index model is the canonical example of a fine risk model and a failed returns model.
> Ref: Ribeiro (2026), Ch. 5, Common pitfalls (p. 182); Ch. 4, §4.6
> Similar: Ribeiro, Problems 5.4 (p. 184), 4.5 (p. 146)

Q: Industry factors are among the most important factors in any risk model and are safely omitted from an expected-return model. What does that pair illustrate?
- That a risk factor earns its place by cutting residual comovement, a returns factor by carrying a premium.
- That industry factors are priced in the cross-section while contributing little to the covariance of returns.
- That the criterion is the same for both jobs, and industries happen to pass it only in large cross-sections.
- That a factor with no premium cannot belong in any correctly specified model of second moments.
<!-- YW5zOjA= -->
> There is no robust "industry premium", yet industry membership is the single largest source of residual comovement the market factor misses. Two criteria, two jobs, one concrete modelling choice decided by which job is being done.
> Ref: Ribeiro (2026), Ch. 5, §5.4.5 (p. 171), §5.4.7 (p. 172)
> Similar: Ribeiro, Problem 5.7 (p. 185)

Q: Why can a set of principal components span nearly all of $\Sigma$ and still be worthless as a pricing model?
- Because principal components are not tradable portfolios, so no investor can earn a premium on them.
- Because eigenvectors are mutually orthogonal, and orthogonal factors carry no premium in equilibrium.
- Because they are extracted in sample, and any in-sample factor has zero premium by construction.
- Because explained variance is a second-moment criterion, and nothing makes a high-variance direction pay.
<!-- YW5zOjM= -->
> Principal components are the best $K$-factor approximation to $\Sigma$ in a least-squares sense — that is a statement about variance, not about reward. Nobody is obliged to pay you for bearing the direction of largest variance.
> Ref: Ribeiro (2026), Ch. 5, §5.1.1 (p. 153), §5.4.5 (p. 170); Cochrane (2005), Ch. 9
> Similar: Ribeiro, Problems 5.4 (p. 184), 5.7 (p. 185)

## diag

Q: The single-index covariance matrix is $\Sigma=\sigma_m^2\beta\beta^\top+D$. What does the rank-one systematic block encode?
- That the market portfolio is mean–variance efficient, which forces every covariance onto a single line.
- That one common shock drives all cross-asset comovement, so the systematic block has one direction.
- That $D$ must be proportional to the identity, since a rank-one update admits only a single scale.
- That betas are estimated jointly rather than asset by asset, which collapses the estimator's rank.
<!-- YW5zOjE= -->
> Rank one is the algebraic image of "there is exactly one shared driver". Efficiency of the market is a pricing claim and is nowhere used here; $D$ is free to differ across assets; and the betas come from $N$ separate OLS regressions.
> Ref: Ribeiro (2026), Ch. 5, §5.2.1 (p. 155); BKM 13e, §8.2 (p. 254)
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: Why does the single-index parameter count grow linearly in $N$ while the sample covariance matrix's grows quadratically?
- Because the sample matrix stores a covariance and a correlation per pair, while the model stores correlations only.
- Because the model estimates betas in one pooled regression, and pooling always brings counts down to order $N$.
- Because every off-diagonal entry is a product of per-asset quantities, so no pair needs its own parameter.
- Because the model drops the diagonal entirely, and only the off-diagonal block scales with the cross-section.
<!-- YW5zOjI= -->
> $\sigma_{ij}=\beta_i\beta_j\sigma_m^2$ means the pairs are not free: they are manufactured from $N$ betas and one market variance. The sample matrix, by contrast, spends one parameter per pair, which is where $N(N+1)/2$ comes from.
> Ref: Ribeiro (2026), Ch. 5, §5.2.2 (p. 157), Example 5.1
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: What does assuming $D$ diagonal assert about the news that moves firms?
- That once the market's move is stripped out, whatever remains in each firm is genuinely its own.
- That every firm's news carries the same variance, so no single name dominates the residual block.
- That firm-specific news is unforecastable over time, so the residuals show no autocorrelation.
- That firm-specific news is normally distributed, so second moments describe it completely.
<!-- YW5zOjA= -->
> The assumption is cross-sectional, not temporal: news moving Pfizer and news moving Exxon share nothing beyond the aggregate market. Equal variances would be a homoscedasticity assumption, and $D$ is explicitly allowed to differ across assets.
> Ref: Ribeiro (2026), Ch. 5, §5.2.3 (p. 156)
> Similar: Ribeiro, Problems 5.1 (p. 183), 5.3 (p. 184)

Q: Residual correlations among industry portfolios are on average positive rather than zero. Which way does that bias the single-index model's risk numbers, and why does the direction matter?
- It overstates covariances and so overstates concentrated portfolios' risk, which is merely conservative.
- It leaves covariances unbiased but inflates their standard errors, which matters only in short samples.
- It overstates covariances for tilted books and understates them for broad ones, so the sign is indeterminate.
- It understates covariances and so overstates diversification, which is the direction that invites concentration.
<!-- YW5zOjM= -->
> Positive residual correlation is comovement the model records as zero, so covariances come out too low and the book looks better diversified than it is. A model erring the other way would only be conservative; this one erring invites the concentration that blows up.
> Ref: Ribeiro (2026), Ch. 5, §5.2.3 (pp. 156–160)
> Similar: Ribeiro, Problems 5.1 (p. 183), 5.3 (p. 184)

Q: Why is the single-index $\Sigma$ guaranteed invertible and well conditioned however large the cross-section grows?
- Because $\beta\beta^\top$ is positive definite, and adding a diagonal matrix preserves positive definiteness.
- Because the systematic block is positive semi-definite and $D$ is strictly positive along its diagonal.
- Because Sherman–Morrison applies to any square matrix, so a closed-form inverse always exists.
- Because the model uses fewer parameters than observations, and that ratio alone fixes conditioning.
<!-- YW5zOjE= -->
> $\beta\beta^\top$ is only rank one, hence semi-definite, never definite. Positive definiteness comes from $D$: strictly positive idiosyncratic variances bound the smallest eigenvalue away from zero, which is exactly the near-singularity chapter 3 could not avoid.
> Ref: Ribeiro (2026), Ch. 5, §5.2.4 (p. 158); Ch. 3, §3.5; App. A
> Similar: Ribeiro, Problems 5.1 (p. 183), A.2 (p. 349)

Q: An analyst adds an asset's systematic risk $\beta_i\sigma_m$ to its idiosyncratic risk $\sigma(\varepsilon_i)$ and reports the sum as total risk. What is wrong?
- The two are measured against different benchmarks, so both need rescaling by beta before adding.
- The systematic term should use the asset's own volatility, not the market's, after which the sum holds.
- Volatilities do not add; the decomposition is additive in variances, so the two combine in quadrature.
- Nothing is wrong, provided the residual is uncorrelated with the market, which OLS guarantees.
<!-- YW5zOjI= -->
> The decomposition $\sigma_i^2=\beta_i^2\sigma_m^2+\text{var}(\varepsilon_i)$ is additive in *variances*. Standard deviations combine as the square root of the sum of squares, so adding them straight overstates total risk.
> Ref: Ribeiro (2026), Ch. 5, §5.2.1 (p. 155); Ch. 4, §4.4
> Similar: Ribeiro, Problems 5.1 (p. 183), 4.3 (p. 146)

## port

Q: The idiosyncratic term of portfolio variance vanishes as a portfolio grows. What exactly must go to zero, and what is the common misreading?
- The largest single weight must vanish; the misreading is that the count of names matters at all.
- The average residual variance must vanish; the misreading is that residual variances stay bounded.
- The portfolio beta must vanish; the misreading is that systematic risk diversifies alongside specific risk.
- The sum of squared weights must vanish; the misreading is that counting holdings measures diversification.
<!-- YW5zOjM= -->
> It is $\sum_i w_i^2$ that must go to zero, which requires the weights to be *spread*. Ninety percent in one name plus a long tail of tiny positions keeps that sum near one, however many tickers appear on the statement.
> Ref: Ribeiro (2026), Ch. 5, §5.3.2 (p. 162), §5.3.4 (p. 164); Common pitfalls (p. 182)
> Similar: Ribeiro, Problem 5.2 (p. 183)

Q: A fund holds fifty oil stocks. Its single-index residual variance looks small, yet the fund is not diversified against oil. What has the model got wrong?
- It dropped the residual cross terms, which do not vanish when residual covariances are positive.
- It used equal weights, whereas the $1/N$ result holds exactly only under value weighting.
- It estimated the betas on too short a window, so every residual variance comes out biased downward.
- It treated oil as a factor although oil carries no premium, so those loadings should have been zero.
<!-- YW5zOjA= -->
> With correlated residuals the portfolio residual variance carries $\sum_{i\neq j} w_iw_j\,\text{cov}(\varepsilon_i,\varepsilon_j)$, and that sum does not die as names are added. The fifty-first oil stock adds a name, not diversification.
> Ref: Ribeiro (2026), Ch. 5, §5.3.4 (p. 164), eq. (5.15)
> Similar: Ribeiro, Problems 5.2 (p. 183), 5.3 (p. 184)

Q: As a spread portfolio adds names without limit, what does its volatility approach, and what sets that floor?
- Zero, provided residuals are uncorrelated, since every source of variance is diversifiable in the limit.
- The average volatility of its constituents, since averaging the weights preserves the average risk.
- The magnitude of its beta times market volatility, so the floor is set by factor exposure alone.
- The average pairwise residual covariance, which is what survives once the factor term is removed.
<!-- YW5zOjI= -->
> The systematic term $\beta_p^2\sigma_m^2$ carries no $1/N$ and does not shrink, so $\sigma_p \to |\beta_p|\sigma_m$. This reproduces chapter 3's average-covariance floor, now read through a factor structure.
> Ref: Ribeiro (2026), Ch. 5, §5.3.2 (p. 162), eq. (5.13); Ch. 3, §3.3
> Similar: Ribeiro, Problem 5.2 (p. 183)

Q: The chapter says diversification annihilates idiosyncratic risk for those who practise it. What does that establish, and where does it stop?
- It establishes that idiosyncratic risk earns no premium, stopping short of how large that premium would be.
- It establishes who feels idiosyncratic risk, stopping short of any claim about what it earns.
- It establishes that undiversified investors are irrational, stopping short of prescribing their remedy.
- It establishes that the market portfolio is efficient, stopping short of naming the tangency weights.
<!-- YW5zOjE= -->
> The risk model supplies the premise — the marginal, diversified investor bears none of it — and the pricing model supplies the conclusion that it commands no premium. Sliding from premise to conclusion inside chapter 5 crosses the two-jobs boundary.
> Ref: Ribeiro (2026), Ch. 5, §5.3.6 (p. 165); Ch. 4, §4.4
> Similar: Ribeiro, Problems 5.2 (p. 183), 5.4 (p. 184)

Q: Tracking error is the volatility of the portfolio's return minus the benchmark's. Under a factor model, which two sources produce it?
- Total beta and total residual variance, since the benchmark contributes no risk of its own to the difference.
- The benchmark's beta and the portfolio's alpha, systematic and specific respectively by construction.
- Estimation error in the betas and in the residual variances, the only two inputs the model actually has.
- Active beta against the benchmark and the residual risk of the active weights, systematic then selection.
<!-- YW5zOjM= -->
> Equation (5.16) is the portfolio decomposition with active weights $w_a=w_p-w_b$ in place of raw ones: $(\beta_p-\beta_b)^2\sigma_m^2$ plus the residual variance of the active bets. A beta-neutral stock-picker zeroes the first term by design.
> Ref: Ribeiro (2026), Ch. 5, §5.3.5 (p. 165), eq. (5.16)
> Similar: Ribeiro, Problems 5.5 (p. 184), 5.6 (p. 185)

Q: Can a portfolio carry high total volatility and low tracking error at the same time?
- Yes, if it holds the benchmark plus small active bets, since active risk uses active weights only.
- No, because tracking error is bounded below by the portfolio's volatility less the benchmark's.
- Yes, but only with a negative active beta, which lets the two volatility terms offset each other.
- No, because a volatile portfolio must depart from a calmer benchmark by at least that margin.
<!-- YW5zOjA= -->
> Total risk uses $w_p$, active risk uses $w_a=w_p-w_b$. A volatile book that is essentially the index plus small tilts tracks closely; a calm book with one big beta bet is the reverse. Reading tracking error as total risk mismeasures every active manager.
> Ref: Ribeiro (2026), Ch. 5, §5.3.5 (p. 165); Common pitfalls (p. 182)
> Similar: Ribeiro, Problems 5.5 (p. 184), 5.6 (p. 185)

## multi

Q: What does adding a well-chosen second factor actually do to the covariance matrix?
- It raises the rank of $D$, letting residual variances differ across assets instead of sharing one value.
- It shrinks each estimated beta toward one, which stabilizes the systematic block against outliers.
- It moves shared variation out of the off-diagonal residuals and into the systematic block $B\Sigma_FB^\top$.
- It orthogonalizes residuals against the market, something the one-factor regression fails to achieve.
<!-- YW5zOjI= -->
> The extra factor does not repair estimation noise; it repairs *misspecification*. Comovement the market missed stops leaking into $D$ and is recorded where it belongs, which is why residual correlations fall as factors are added.
> Ref: Ribeiro (2026), Ch. 5, §5.4.2 (p. 168), §5.4.7 (p. 172)
> Similar: Ribeiro, Problems 5.3 (p. 184), 5.7 (p. 185)

Q: A $K$-factor risk model estimates $B$, $\Sigma_F$ and $D$. Which pieces keep the total count linear in $N$, and which is the one dense matrix?
- $D$ keeps it linear because it is diagonal; $B$ is dense and so contributes a term of order $N^2$.
- $B$ and $D$ each grow linearly in $N$; $\Sigma_F$ is dense but its size depends only on $K$.
- $\Sigma_F$ keeps it linear because factors are few; $B$ is dense and supplies the quadratic term.
- All three grow linearly, which is why a factor count can never approach the sample matrix's.
<!-- YW5zOjE= -->
> $B$ holds $K$ loadings per asset and $D$ one variance per asset — both order $N$ with $K$ fixed. $\Sigma_F$ is the only dense block, and it is small because it is $K\times K$, estimated from well-measured factor series.
> Ref: Ribeiro (2026), Ch. 5, §5.4.2 (p. 168), §5.4.4 (p. 170), Example 5.8
> Similar: Ribeiro, Problems 5.3 (p. 184), 5.7 (p. 185)

Q: Why should returns exhibit a factor structure in the first place?
- Because much of the news that moves prices is shared, being common cash-flow and discount-rate shocks.
- Because the covariance matrix of any large cross-section is mathematically forced toward low rank.
- Because rational pricing requires comovement, so factor structure disappears if traders are irrational.
- Because index funds trade the same names together, and that trading manufactures the comovement.
<!-- YW5zOjA= -->
> The reason is economic, not statistical. Oil prices, rates and the cycle move whole groups of firms at once. Factor structure is a shadow cast by the economy that links firms, and it would appear even in a market of purely irrational traders.
> Ref: Ribeiro (2026), Ch. 5, §5.4.3 (p. 169)
> Similar: Ribeiro, Problem 5.7 (p. 185)

Q: Fundamental factors read a firm's loading off its characteristics rather than estimating it from returns. What does that buy?
- Unbiased loadings, since characteristics are observed without the sampling error a regression brings.
- Priced factors, since size and book-to-market are exactly the characteristics that command premia.
- Orthogonal factors, since firm characteristics are measured independently of one another.
- Coverage from day one, since a new listing has a size and an industry before it has a return history.
<!-- YW5zOjM= -->
> Inverting the regression — loadings observed, factor returns recovered cross-sectionally — is the barra tradition's practical edge: stable, forward-looking loadings available immediately, which is what portfolio construction needs. Whether those factors are priced is chapter 6's question.
> Ref: Ribeiro (2026), Ch. 5, §5.4.5 (p. 171)
> Similar: Ribeiro, Problem 5.7 (p. 185)

Q: Every extra factor lowers residual comovement, so why is a very large $K$ a bad idea for a risk model?
- Because factor covariances are estimated jointly, and a large $\Sigma_F$ turns singular before $B$ does.
- Because each factor brings $N$ new loadings, injecting the sampling variance the structure was meant to cure.
- Because factors past the first few are unpriced, adding covariance structure that no premium supports.
- Because $D$ stops being diagonal once the factor count exceeds the number of distinct industries.
<!-- YW5zOjE= -->
> This is the bias–variance trade-off applied to $K$ itself: too few factors and real comovement is missed, too many and sampling flukes are dressed up as factors. A handful of interpretable factors captures nearly all the estimable comovement.
> Ref: Ribeiro (2026), Ch. 5, §5.4.6 (p. 172)
> Similar: Ribeiro, Problems 5.3 (p. 184), 5.7 (p. 185)

## payoff

Q: Why is the global minimum-variance portfolio the decisive test of a covariance model?
- Because it sits at the frontier's leftmost point, where estimation error in $\Sigma$ is at its smallest.
- Because it is the only frontier portfolio whose weights sum to one without a risk-free asset.
- Because it needs no expected returns, so it isolates the covariance problem from the means problem.
- Because it is what a risk-averse investor would actually hold, making the test economically relevant.
<!-- YW5zOjI= -->
> Its weights depend on $\Sigma$ and nothing else, so a failure can only be the covariance model's. That is precisely why it is the pure experiment, and why the tangency portfolio is not.
> Ref: Ribeiro (2026), Ch. 5, §5.5.1 (p. 173), eq. (5.20); Ch. 3, eq. (3.13)
> Similar: Ribeiro, Problem 5.5 (p. 184)

Q: What does a minimum-variance optimizer do when handed a noisy sample covariance matrix?
- It drifts toward equal weighting, since noise averages out across a large enough cross-section.
- It concentrates on the lowest-variance names, whose variances are the entries measured most precisely.
- It refuses to solve, because a matrix with fewer observations than assets cannot be inverted at all.
- It loads on pairs sampling error made look like hedges, and the phantom cancellations fail out of sample.
<!-- YW5zOjM= -->
> This is error maximization in the covariance matrix — the exact twin of what wrecked chapter 3's tangency portfolio. The in-sample volatility it reports is a fiction; the factor matrix cannot be fooled this way because it has no spurious off-diagonal flukes to find.
> Ref: Ribeiro (2026), Ch. 5, §5.5.3 (p. 176); Ch. 3, §3.5
> Similar: Ribeiro, Problem 5.5 (p. 184)

Q: On a small cross-section with a long estimation window, the factor-matrix portfolio can realize slightly higher out-of-sample volatility than the sample-matrix portfolio. Which principle is that?
- Structure helps when data are scarce relative to what is estimated, and costs accuracy when abundant.
- Factor models are biased, so they are dominated whenever the sample matrix is invertible at all.
- Out-of-sample tests are noisy at small $N$, so the ordering there carries no information either way.
- The single-index model needs a long window for its betas, so it improves as the window shortens.
<!-- YW5zOjA= -->
> The relevant scarcity measure is $N/T$. At low $N/T$ the sample matrix is well estimated and the factor model's rigidity is a small tax; at high $N/T$ that same rigidity is a rescue. The wrinkle is stated, not hidden.
> Ref: Ribeiro (2026), Ch. 5, §5.5.3 (p. 177)
> Similar: Ribeiro, Problem 5.5 (p. 184)

Q: A factor covariance matrix rescues the minimum-variance portfolio but barely helps the tangency portfolio. Why?
- Because the tangency portfolio needs a risk-free rate, which a covariance model does not supply.
- Because the tangency weights run through $\Sigma^{-1}$, and the factor inverse is the more biased of the two.
- Because the tangency portfolio also needs expected returns, and those remain as noisy as ever.
- Because maximizing a Sharpe ratio is a first-moment problem in which the covariance matrix plays no part.
<!-- YW5zOjI= -->
> This is the two-jobs distinction made numerate. Fix the second moments beautifully and you still do not know which assets are cheap, so the maximum-Sharpe portfolio stays a guess. Fixing risk is necessary but not sufficient for the full Markowitz problem.
> Ref: Ribeiro (2026), Ch. 5, §5.5.4 (p. 177); Ch. 3, §3.5, eq. (3.19)
> Similar: Ribeiro, Problems 5.4 (p. 184), 5.5 (p. 184)

## notclaim

Q: Two stocks have identical rows of $B$ and identical idiosyncratic variance, but one is fairly priced and the other is a bubble. What does the risk model report, and is it right?
- That the bubble stock is riskier, and rightly so, since a price far above value adds variance the loadings miss.
- That they are the same asset, and rightly so, because they genuinely do carry the same risk.
- That the bubble stock has the higher alpha, and rightly so, since the intercepts absorb any mispricing.
- That the model is misspecified, and rightly so, since a covariance matrix must separate cheap from dear.
<!-- YW5zOjE= -->
> Same loadings, same specific variance, same contribution to any portfolio's covariance. The difference between them is a difference in expected returns, visible only to a theory of first moments. The blindness is the boundary of competence, not a defect.
> Ref: Ribeiro (2026), Ch. 5, §5.6.1 (p. 179)
> Similar: Ribeiro, Problems 5.4 (p. 184), 5.7 (p. 185)

Q: Which family of portfolios can be built knowing $\Sigma$ alone, with no view on expected returns?
- Minimum variance, risk parity, and the value-weighted index — none takes a position on which assets are cheap.
- Tangency, minimum variance, and the zero-beta portfolio — each solves a quadratic program in $\Sigma$.
- Every portfolio on the efficient frontier, since the frontier is generated by the covariance matrix alone.
- Equal weighting and momentum — both are mechanical rules that never consult an expected return.
<!-- YW5zOjA= -->
> These are the strategies for the honest agnostic about returns: minimize $w^\top\Sigma w$, equalize risk contributions, or hold the market. The tangency portfolio and momentum both require a view on means, and the frontier beyond its leftmost point does too.
> Ref: Ribeiro (2026), Ch. 5, §5.6.2 (p. 179), §5.3.7 (p. 166)
> Similar: Ribeiro, Problems 5.5 (p. 184), 5.6 (p. 185)

Q: Two portfolios report the same factor value-at-risk. What does the factor decomposition reveal that the headline number cannot?
- Whether the normal approximation holds, since the decomposition inspects each factor's tails directly.
- Which portfolio has the higher expected return, since contributions and premia are read off the same $B$.
- Whether either portfolio is mispriced, since a correct value-at-risk implies a correct discount factor.
- Where the risk lives — a market bet, industry bets, or name concentration — which one number hides.
<!-- YW5zOjM= -->
> Because $w^\top\Sigma w$ splits into a systematic part and a sum of specific parts, a risk report can attribute the loss. Two books can share a value-at-risk and be utterly different underneath; none of this requires a single expected return.
> Ref: Ribeiro (2026), Ch. 5, §5.6.3 (p. 180), Example 5.10; §5.3.7 (p. 166)
> Similar: Ribeiro, Problems 5.5 (p. 184), 5.6 (p. 185)
