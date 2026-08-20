---
quiz: "Session 5 — Factor Models for Risk (relevance-weighted follow-up)"
tags:
  twojobs: "1 · Two Jobs for a Factor Model"
  single: "2 · The Single-Index Model as a Risk Model"
  portfolio: "3 · Systematic and Idiosyncratic at Portfolio Level"
  multi: "4 · Multifactor Risk Models"
  payoff: "5 · Rebuilding the Portfolios"
  notclaim: "6 · What a Risk Model Does Not Claim"
---

## twojobs

Q: A factor model can be asked to do two different jobs. What are they, and which one does chapter 5 take up?
- Restrict the number of traded assets, and restrict the number of states; chapter 5 takes the state-space job.
- Restrict expected returns, and restrict the risk-free rate; chapter 5 takes the expected-return job for later testing.
- Restrict the covariance matrix, and restrict the cross-section of expected returns; chapter 5 takes the covariance job.
- Restrict the discount factor, and restrict investor preferences; chapter 5 takes the preference job first of all.
<!-- YW5zOjI= -->
> A risk model constrains $\Sigma$, the second moments. A returns model constrains $E[R^e]$, the first moments. Chapter 5 is entirely about the first job; chapter 6 takes the second. Keeping them apart is this chapter's central discipline.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153)
> Similar: Ribeiro, Problem 5.4 (p. 184)

Q: "A good risk model is automatically a good returns model." Is that right?
- Right: any model reproducing the covariance matrix must reproduce expected returns, since both are moments of one distribution.
- Wrong: a statistical factor can capture covariation while saying nothing about premia, and a priced one the reverse.
- Right, provided the factors are traded portfolios, since a traded factor carries its own risk premium by construction.
- Wrong, but only because estimation error differs; with a long enough sample the two jobs coincide in the limit.
<!-- YW5zOjE= -->
> Principal components can span the covariance structure with factors nobody is paid to bear. Conversely a priced factor may explain premia while capturing little covariance. The two jobs are logically independent — this is the canonical true/false of the chapter.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153); Cochrane (2005), Ch. 9
> Similar: Ribeiro, Problem 5.4 (p. 184); True/False 1–30 (pp. 185–187)

Q: Does a risk model require its factors to be priced?
- No, since it claims only that returns co-move through the factors, which is a second-moment statement.
- Yes, since the model's covariance matrix is derived from the beta representation of expected returns.
- Yes, since an unpriced factor contributes no variance to any portfolio built on the model.
- No, but only if the factors are orthogonal, since correlated factors reintroduce the pricing requirement.
<!-- YW5zOjA= -->
> Pricing is a first-moment claim. A risk model asserts co-movement, and co-movement is a second-moment claim. An industry dummy may drive covariance while carrying no premium at all.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153)
> Similar: Ribeiro, Problem 5.7 (p. 185)

Q: A researcher runs one time-series regression of an asset's excess return on a factor and obtains a high $R^2$ and a large $t$-statistic on the slope. Which conclusion is licensed?
- That the factor is priced, since a significant slope means the factor earns a premium in the cross-section.
- That the model's alphas are zero, since a high $R^2$ leaves no room for systematic pricing errors to survive.
- That the factor explains this asset's variance well; whether it carries a premium is a separate question.
- That the factor belongs in a returns model, since explanatory power in one regression transfers to the cross-section.
<!-- YW5zOjI= -->
> The slope and $R^2$ speak to co-movement — the risk job. A premium is a statement about the *mean* of the factor and about cross-sectional alphas, which this regression never tests. This is the chapter-4 distinction between estimation vehicle and equilibrium restriction, one level up.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153); Ch. 4, §4.4 (p. 129)
> Similar: Ribeiro, Problems 5.4 (p. 184), 4.4 (p. 147)

Q: Two analysts disagree. One says the model failed because implied correlations do not match realized ones; the other says it failed because assets show systematic alphas. What has each diagnosed?
- Neither diagnosed a failure, since correlation mismatch and alphas are both artefacts of finite samples.
- Both diagnosed the same failure, since alphas and correlation errors are two views of one misspecification.
- The first diagnosed a failed returns model, the second a failed risk model; the labels are conventionally the other way round.
- The first diagnosed a failed risk model, the second a failed returns model; a model can fail either test independently.
<!-- YW5zOjM= -->
> Correlation mismatch condemns the second-moment claim; systematic alphas condemn the first-moment claim. A model can pass one and fail the other, which is exactly why the chapter insists on naming which job is being judged.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153)
> Similar: Ribeiro, Problem 5.4 (p. 184)

## single

P: A single-index risk model has market variance $\sigma^2_{mkt}=0{,}04$. Asset A has $\beta_A=1{,}5$ and idiosyncratic variance 0,0325; asset B has $\beta_B=0{,}5$ and idiosyncratic variance 0,1000; asset C has $\beta_C=1{,}0$ and idiosyncratic variance 0,0500. Residuals are uncorrelated across assets.

Q: What is the model's covariance between assets A and B, and what is A's total variance?
- Covariance 0,1225 and total variance 0,1525, from the shared market term plus the sum of both assets' idiosyncratic variances.
- Covariance 0,7500 and total variance 0,3500, from $\beta_A\beta_B$ and the square root of the summed variances.
- Covariance 0,0300 and total variance 0,0900, from $\beta_A\beta_B\sigma^2_{mkt}$ and the systematic term alone.
- Covariance 0,0300 and variance 0,1225, from $\beta_A\beta_B\sigma^2_{mkt}$ and $\beta_A^2\sigma^2_{mkt}+\text{var}(\varepsilon_A)$.
<!-- YW5zOjM= -->
> Off-diagonal: $1{,}5(0{,}5)(0{,}04)=0{,}03$ — idiosyncratic terms never enter a covariance, since residuals are uncorrelated. Diagonal: $2{,}25(0{,}04)+0{,}0325=0{,}09+0{,}0325=0{,}1225$, so $\sigma_A=0{,}35$.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155); BKM 13e, §8.2 (p. 254)
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: In this model, what is the correlation between assets A and C?
- 0,571, since $\text{cov}=0{,}06$ with deviations $\sqrt{0{,}1225}=0{,}35$ and $\sqrt{0{,}09}=0{,}30$.
- 0,667, since $\text{cov}=0{,}06$ and both standard deviations equal 0,30 in a single-index model.
- 0,150, since $\text{cov}=0{,}06$ divided by the product of the two variances 0,1225 and 0,09.
- 0,667, since correlation equals the ratio of the betas when both load on one common factor.
<!-- YW5zOjA= -->
> $\text{cov}(A,C)=1{,}5(1{,}0)(0{,}04)=0{,}06$. C's variance is $1{,}0(0{,}04)+0{,}05=0{,}09$, so $\sigma_C=0{,}30$; $\sigma_A=0{,}35$. Then $0{,}06/(0{,}35\times0{,}30)=0{,}571$. Dividing by variances rather than standard deviations is the standard slip.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: For 500 assets, how many parameters does a full covariance matrix need, and how many does a single-index model need?
- 250.000 against 500, since the full matrix has $N^2$ entries and the index model needs one beta each.
- 125.250 against 501, since the index model needs one beta per asset plus the market variance only.
- 125.250 against 1.001, since the full matrix holds $N(N+1)/2$ entries and the index model $2N+1$.
- 1.000.000 against 1.001, since every pair needs both a covariance and a correlation stored separately.
<!-- YW5zOjI= -->
> $500(501)/2=125.250$ distinct entries against $2(500)+1=1.001$ — 500 betas, 500 idiosyncratic variances, one market variance. That collapse is the whole practical point of the model.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: What does the assumption that $D$ is diagonal mean economically, and where does it fail?
- That residuals are uncorrelated over time, so the model has no autocorrelation; it fails at high sampling frequencies.
- That residuals have equal variance across assets, so the model is homoscedastic; it fails whenever firm sizes differ materially.
- That residuals are uncorrelated across assets, so co-movement runs through the factor; it fails on industry shocks.
- That residuals are normally distributed, so the covariance fully describes them; it fails when returns show fat tails.
<!-- YW5zOjI= -->
> A diagonal $D$ says the market is the *only* shared driver. Two oil firms move together beyond their market betas, so their residuals correlate and the model understates their joint risk. That failure is precisely what motivates a second factor.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problems 5.1 (p. 183), 5.3 (p. 184)

Q: An analyst reports asset A's systematic risk as 0,30 and its idiosyncratic risk as 0,05, in a model where $\beta_A=1{,}5$, $\sigma_{mkt}=0{,}20$ and $\sigma_A=0{,}35$. What is wrong?
- Nothing is wrong: 0,30 is $\beta\sigma_{mkt}$ and 0,05 is the residual, and the two sum to the total 0,35.
- The idiosyncratic figure should be zero, since a single-factor model leaves no residual once beta has been estimated.
- The systematic figure should be 0,45, since systematic risk is beta times the asset's own standard deviation rather than the market's.
- The two figures are in standard-deviation units and are being treated as if they add; in variance units they are 0,0900 and 0,0325.
<!-- YW5zOjM= -->
> $0{,}30=\beta\sigma_{mkt}$ is a standard deviation and does not add to anything. In variance: systematic $2{,}25(0{,}04)=0{,}09$, total $0{,}35^2=0{,}1225$, residual $0{,}0325$. Standard deviations combine in quadrature: $\sqrt{0{,}09+0{,}0325}=0{,}35$.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155); Ch. 4, §4.4 (p. 129)
> Similar: Ribeiro, Problems 5.1 (p. 183), 4.3 (p. 147)

Q: Why does the single-index model's covariance matrix have rank structure $\beta\beta^\top\sigma^2_{mkt}+D$ rather than an unrestricted matrix?
- Because the model asserts one common source of co-movement, so the systematic part has rank one and $D$ carries the rest.
- Because the model requires the market to be mean-variance efficient, which forces the rank of the systematic block to one.
- Because $\Sigma$ must be invertible, and only a rank-one systematic block guarantees that the sum is positive definite.
- Because betas are estimated by OLS, and OLS residuals are orthogonal, which mechanically produces a rank-one matrix.
<!-- YW5zOjA= -->
> One factor means every pair covaries only through that factor, which is exactly a rank-one outer product $\beta\beta^\top\sigma^2_{mkt}$. The diagonal $D$ then holds what the factor does not explain. Invertibility is a welcome by-product of $D$ being positive, not the reason for the structure.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155); H&L, Ch. 4 §4.20–4.25 (pp. 105–113)
> Similar: Ribeiro, Problem 5.1 (p. 183)

## portfolio

P: In a single-index model with $\sigma^2_{mkt}=0{,}04$, an equally weighted portfolio holds assets A, B and C with betas 1,5, 0,5 and 1,0 and idiosyncratic variances 0,0325, 0,1000 and 0,0500. Residuals are uncorrelated.

Q: What are the portfolio's beta and total variance?
- Beta 1,0 and variance 0,0603, from systematic $1{,}0^2(0{,}04)=0{,}0400$ plus idiosyncratic $0{,}1825/9=0{,}0203$.
- Beta 1,0 and variance 0,1008, from systematic $0{,}0400$ plus the simple average of the three residual variances.
- Beta 3,0 and variance 0,3600, from summing the three betas and squaring before applying $\sigma^2_{mkt}=0{,}04$.
- Beta 1,0 and variance 0,0400, since $\text{var}(\varepsilon_p)$ vanishes entirely in a portfolio of several assets.
<!-- YW5zOjA= -->
> $\beta_p$ is the weighted average, $(1{,}5+0{,}5+1{,}0)/3=1{,}0$. Systematic $=1(0{,}04)=0{,}04$. Independent residuals enter with weight squared: $(1/9)(0{,}0325+0{,}1000+0{,}0500)=0{,}0203$. Total 0,0603, so $\sigma_p=0{,}2455$.
> Ref: Ribeiro (2026), Ch. 5, §5.3 (p. 161)
> Similar: Ribeiro, Problem 5.2 (p. 183)

Q: Hold the betas fixed and add ever more assets with comparable idiosyncratic variances. What happens to portfolio variance?
- It falls towards zero, since diversification eventually removes every source of $\sigma^2_p$ there is.
- It falls towards the average $\text{var}(\varepsilon_i)$, the limit of the weighted residual sum.
- It falls towards the systematic floor $\beta_p^2\sigma^2_{mkt}$, which diversification never removes.
- It stays constant, since added assets raise covariance terms as fast as they dilute $\text{var}(\varepsilon_i)$.
<!-- YW5zOjI= -->
> The residual term carries $1/N$ and vanishes; the systematic term does not depend on $N$ at all. Here that floor is $1(0{,}04)=0{,}04$, against the three-asset total of 0,0603. Diversification buys the difference and nothing more.
> Ref: Ribeiro (2026), Ch. 5, §5.3 (p. 161); BKM 13e, §8.2 (p. 254)
> Similar: Ribeiro, Problem 5.2 (p. 183)

Q: With 100 equally weighted assets each having idiosyncratic variance 0,0900 and uncorrelated residuals, what is the portfolio's residual volatility?
- 0,0009, since residual volatility is $\text{var}(\varepsilon_p)$ divided by the number of holdings.
- 0,0300, since residual variance is $0{,}0900/100=0{,}0009$ and volatility is its square root.
- 0,3000, since residual volatility equals the common $\sigma(\varepsilon_i)$, unchanged by pooling.
- 0,0090, since residual volatility falls linearly with $N$, from 0,90 down to 0,009 here.
<!-- YW5zOjE= -->
> Variance falls with $N$: $0{,}0900/100=0{,}0009$. Volatility falls with $\sqrt N$: $\sqrt{0{,}0009}=0{,}03$, down from 0,30. Confusing which of the two falls with $N$ is the recurring slip in this material.
> Ref: Ribeiro (2026), Ch. 5, §5.3 (p. 161)
> Similar: Ribeiro, Problem 5.2 (p. 183)

Q: Two portfolios have the same total volatility, but one is a concentrated holding of five names and the other a broad index. What does the risk model say distinguishes them?
- Their composition of that volatility: the concentrated one carries a large residual share, the index almost none.
- Nothing, since total volatility is the complete description of a portfolio's risk in any factor model.
- The concentrated portfolio must have the higher beta, since fewer names always means more systematic exposure.
- The index must have the higher expected return, since breadth is compensated in equilibrium by a diversification premium.
<!-- YW5zOjA= -->
> Equal totals can decompose very differently. The model's content is the split into $\beta_p^2\sigma^2_{mkt}$ and residual, and that split — not the total — is what drives hedging, tracking error and the behaviour of the portfolio under a market shock.
> Ref: Ribeiro (2026), Ch. 5, §5.3 (p. 161)
> Similar: Ribeiro, Problems 5.2 (p. 183), 5.6 (p. 185)

Q: A manager holds the concentrated portfolio and argues she should be compensated for its full volatility. What does chapter 5 let you say, and what does it not?
- The model cannot decompose a concentrated portfolio at all, since the decomposition requires a large number of holdings.
- The model shows she is compensated for the systematic part only, since residual risk is diversifiable and therefore unpriced.
- The model shows she is compensated for total volatility, since her own portfolio is the relevant risk from her perspective.
- The model splits her risk into systematic and residual parts; whether either is compensated it does not answer.
<!-- YW5zOjM= -->
> This is the chapter's own boundary. A risk model measures and decomposes risk; it makes no claim about what earns a premium. That claim needs a returns model, which is chapter 6. Answering the compensation question here is exactly the overreach §5.6 warns against.
> Ref: Ribeiro (2026), Ch. 5, §5.3 (p. 161); §5.6 (p. 178)
> Similar: Ribeiro, Problem 5.4 (p. 184)

Q: Under the single-index model, what is the covariance between two assets whose betas are 1,2 and 0,8 when the market variance is 0,04?
- 0,0384, from $\beta_1\beta_2\sigma^2_{mkt}$ plus the product of their idiosyncratic standard deviations.
- 0,0384, from $\beta_1\beta_2\sigma^2_{mkt}=1{,}2(0{,}8)(0{,}04)$, with residuals contributing nothing.
- 0,9600, from the product of the betas divided by the market variance.
- 0,0400, from the market variance alone, since betas affect variances but not covariances.
<!-- YW5zOjE= -->
> $1{,}2(0{,}8)(0{,}04)=0{,}0384$. Two options give the right number with wrong reasoning or wrong additions attached — the covariance in this model is exactly the product of the betas and the factor variance, with no residual contribution whatever.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problem 5.1 (p. 183)

## multi

Q: Write the multifactor risk model's covariance matrix and say what each piece does.
- $\Sigma=B^\top FB+D$, where $B$ holds the factor returns, $F$ the loadings and $D$ the total variances of the assets.
- $\Sigma=BFB^\top+D$, where $B$ holds the loadings, $F$ the factor covariance matrix and $D$ the diagonal residual variances.
- $\Sigma=BFB^\top$, since a multifactor model with enough factors leaves no residual variance to record.
- $\Sigma=BB^\top+FD$, where $B$ holds the loadings and the product $FD$ carries the whole systematic block.
<!-- YW5zOjE= -->
> $B$ is $N\times K$, $F$ is $K\times K$ and $D$ is $N\times N$ diagonal. The systematic block has rank at most $K$; $D$ holds what the factors leave. This is the object the second project builds directly.
> Ref: Ribeiro (2026), Ch. 5, §5.4 (p. 167); BKM 13e, §10.4 (p. 326)
> Similar: Ribeiro, Problem 5.3 (p. 184)

Q: Why does adding a second factor help where a single-index model fails?
- Because it guarantees that every asset's alpha becomes zero once the second source of premium is accounted for.
- Because it lowers the number of parameters, making the covariance matrix easier to estimate from short samples.
- Because it raises the rank of the systematic block, so residuals correlated under one factor decorrelate.
- Because it makes $D$ non-diagonal, which is what allows industry effects to be captured by the model at all.
<!-- YW5zOjI= -->
> The single-index model fails when residuals share a driver — an industry shock, say. Promoting that driver to a factor moves it from $D$ into $BFB^\top$, restoring the diagonal assumption. Note it *increases* the parameter count and leaves $D$ diagonal by construction.
> Ref: Ribeiro (2026), Ch. 5, §5.4 (p. 167)
> Similar: Ribeiro, Problems 5.3 (p. 184), 5.7 (p. 185)

Q: For 500 assets and a five-factor model, roughly how many parameters does $\Sigma=BFB^\top+D$ require?
- About 3.015, from 2.500 loadings, 15 distinct entries of $F$ and 500 residual variances.
- About 125.250, since any model of 500 assets must still specify the full covariance matrix.
- About 505, from 500 residual variances plus five factor variances, the loadings being estimated jointly.
- About 2.500, from the loadings alone, since $F$ and $D$ are normalised away in estimation.
<!-- YW5zOjA= -->
> $B$ is $500\times5=2.500$; $F$ is symmetric $5\times5$, so $5(6)/2=15$; $D$ contributes 500. Total 3.015 against 125.250 unrestricted — still an enormous saving, and more than the 1.001 a single factor needs.
> Ref: Ribeiro (2026), Ch. 5, §5.4 (p. 167)
> Similar: Ribeiro, Problem 5.3 (p. 184)

Q: How should factors be chosen for a risk model, and what is the trade-off?
- By statistical significance in the cross-section; only factors with significant premia belong in a covariance model.
- By whether they carry risk premia; factors without premia contribute nothing to the covariance matrix.
- By whether they capture common co-movement; more factors fit the sample better but are estimated with more error.
- By economic theory alone; a factor with no theoretical motivation cannot improve a covariance forecast.
<!-- YW5zOjI= -->
> The criterion is co-movement, not premia. The trade-off is the familiar one: each added factor absorbs more shared variation in-sample while adding parameters that must be estimated, so out-of-sample performance can worsen. Statistical and fundamental factors are both legitimate here.
> Ref: Ribeiro (2026), Ch. 5, §5.4 (p. 167)
> Similar: Ribeiro, Problem 5.7 (p. 185)

Q: A statistical factor model built from principal components explains 95% of return variation but its factors have no economic interpretation. Is it a valid risk model?
- No, since a factor must be interpretable for its loadings to be estimated consistently from returns data.
- Yes for the risk job, since capturing co-movement is what a risk model is asked to do.
- Yes, and it is also a valid returns model, since factors capturing most variation necessarily capture most premia.
- No, since principal components are orthogonal by construction and real factors are correlated.
<!-- YW5zOjE= -->
> Principal components are a legitimate answer to the covariance question. What they do *not* deliver is a premium story — that is chapter 6's problem. Interpretability matters for communication and for stability out of sample, not for validity as a risk model.
> Ref: Ribeiro (2026), Ch. 5, §5.4 (p. 167); §5.1 (p. 153)
> Similar: Ribeiro, Problem 5.7 (p. 185)

## payoff

Q: A minimum-variance portfolio is built from a factor-model $\Sigma$ rather than the sample covariance matrix. What is the usual out-of-sample result, and why?
- The two perform identically, because both are unbiased estimates of the same population covariance matrix.
- The sample matrix portfolio typically does better, because it uses all the information in the data without imposing false structure.
- The factor-model portfolio typically does better, because its structure suppresses estimation error in the off-diagonals.
- The factor-model portfolio typically does worse in variance but better in return, trading one objective for the other.
<!-- YW5zOjI= -->
> The sample matrix has $N(N+1)/2$ noisy entries, and optimisation loads precisely on the noisiest. The factor model trades a little bias for a large variance reduction in the estimate itself. This is the same error-maximisation logic that the frontier chapter raises.
> Ref: Ribeiro (2026), Ch. 5, §5.5 (p. 173); Ch. 3, §3.5 (p. 100)
> Similar: Ribeiro, Problem 5.5 (p. 184)

Q: Define tracking error against a benchmark and say which part of the risk model produces it.
- The difference in Sharpe ratios; it comes from the factor covariance matrix once residual risk has been diversified.
- The volatility of the portfolio itself; it comes from the systematic block, since the benchmark contributes no variance of its own.
- The average absolute return difference against the benchmark; it comes from the residual block only, tilts being benchmark-neutral.
- The volatility of the return difference against the benchmark; it comes from active tilts and from residuals alike.
<!-- YW5zOjM= -->
> Tracking error is $\sigma(R_p-R_b)$, computed on the active weights $w_p-w_b$ through the same $\Sigma$. Both a factor tilt and undiversified residual risk contribute; a portfolio matching the benchmark's factor exposures can still have tracking error from stock-specific bets.
> Ref: Ribeiro (2026), Ch. 5, §5.5 (p. 173)
> Similar: Ribeiro, Problem 5.6 (p. 185)

Q: A portfolio matches its benchmark's factor exposures exactly. What is its tracking error?
- Zero, since identical factor exposures mean identical returns period by period.
- Not necessarily zero: residual risk from stock-specific active positions still contributes.
- Zero only if the benchmark is the market portfolio, in which case beta matching suffices.
- Undefined, since tracking error requires a difference in factor exposures to be computed at all.
<!-- YW5zOjE= -->
> Matching $B$ removes the systematic component of active risk and leaves the $D$ component. A manager holding very different names with the same exposures still deviates. That residual is the active-risk budget the chapter asks you to size.
> Ref: Ribeiro (2026), Ch. 5, §5.5 (p. 173)
> Similar: Ribeiro, Problem 5.6 (p. 185)

Q: Why does imposing factor structure on $\Sigma$ help even when the true covariance matrix is not exactly of that form?
- Because bias in the covariance matrix does not affect portfolio weights, only the level of estimated portfolio variance.
- Because any covariance matrix can be written exactly in factor form, so no bias is introduced at any point.
- Because the imposed structure guarantees the estimate is positive definite, which is the only property optimisation requires.
- Because the bias introduced is small beside the estimation variance it removes, when assets are many and samples short.
<!-- YW5zOjM= -->
> A bias–variance trade in estimation. With $N$ large relative to $T$, the sample matrix is badly conditioned and the optimiser exploits its errors. A slightly wrong but stable $\Sigma$ produces better portfolios than an unbiased but noisy one.
> Ref: Ribeiro (2026), Ch. 5, §5.5 (p. 173); Ledoit–Wolf (2003, 2004)
> Similar: Ribeiro, Problem 5.5 (p. 184)

Q: A hundred years of monthly data would fix the estimation problem for a 500-asset covariance matrix. True?
- False: 500 assets give 125.250 entries, and 1.200 monthly observations leave it badly conditioned.
- True, since the sample covariance matrix is consistent and 1.200 observations comfortably exceed 500 assets.
- True, provided returns are i.i.d., in which case the estimate converges at the usual root-$T$ rate.
- False, but only because a century of data spans regime changes, not because of any dimensionality problem.
<!-- YW5zOjA= -->
> The problem is dimensional, not merely a matter of span. $T=1.200$ against 125.250 parameters leaves the sample matrix nearly singular, and its inverse — what the optimiser uses — wildly unstable. Regime change is a real but separate worry.
> Ref: Ribeiro (2026), Ch. 5, §5.5 (p. 173)
> Similar: Ribeiro, Problem 5.5 (p. 184)

## notclaim

Q: What does a risk model explicitly not claim?
- That its covariance forecasts are stable over time, which is the only limitation the chapter records.
- That its factors are priced, that alphas are zero, or that expected return follows from exposures.
- That residual risk exists at all, since a complete model would leave nothing outside the factor block.
- That its factors are uncorrelated with one another, which is what distinguishes it from a returns model.
<!-- YW5zOjE= -->
> Everything a risk model says lives in second moments. Reading a premium off a factor loading is importing the first-moment claim it never made. The chapter closes by naming this boundary precisely because the temptation is strong.
> Ref: Ribeiro (2026), Ch. 5, §5.6 (p. 178)
> Similar: Ribeiro, Problem 5.4 (p. 184); True/False 1–30 (pp. 185–187)

Q: An analyst finds a factor with a high loading on a stock and concludes the stock should earn a high expected return. What has gone wrong?
- The loading should have been squared before being converted into an expected-return contribution.
- The loading was estimated from a time-series regression, which is inconsistent when the factor is not traded.
- Nothing has gone wrong, provided the loading is statistically significant at conventional levels.
- A loading is a second-moment object and a premium a first-moment one; moving between needs a returns model.
<!-- YW5zOjM= -->
> $\beta$ measures how much a stock moves with the factor. Whether that movement is compensated depends on the factor's premium, which no covariance model determines. The same confusion, one chapter earlier, was reading the security market line off total risk.
> Ref: Ribeiro (2026), Ch. 5, §5.6 (p. 178); Ch. 4, §4.2 (p. 120)
> Similar: Ribeiro, Problems 5.4 (p. 184), 4.1 (p. 146)

Q: Chapter 1 writes $E[R^i]=R_f+\beta_{i,m}\lambda_m$ with $\lambda_m<0$, while a risk model reports positive factor loadings and positive factor variances. Is there a contradiction?
- No: $\lambda_m$ prices risk on the discount factor, while a risk model reports covariances, carrying no such sign.
- Yes: a negative price of risk is inconsistent with the positive definiteness that any covariance matrix must satisfy.
- No, but only because $\lambda_m$ is conventionally reported with the opposite sign in empirical work.
- Yes: the discount factor representation and the factor risk model cannot both hold in the same economy.
<!-- YW5zOjA= -->
> Different objects. $\lambda_m=-\sigma^2(m)/E[m]$ is negative because assets loading on $m$ pay when you need it most and so earn less. A covariance matrix is positive definite and its entries carry no premium interpretation at all. Keeping first and second moments apart resolves it.
> Ref: Ribeiro (2026), Ch. 5, §5.6 (p. 178); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problems 5.4 (p. 184), 1.4 (p. 37)
