---
quiz: "Full-Course Review — Round 3 of 5"
tags:
  sdf: "S01 · From State Prices to the SDF"
  consumo: "S02 · Consumption Beta and the Equity Premium"
  fronteira: "S03 · Frontier Geometry and the Tangency Portfolio"
  capm: "S04 · Linear SDF, Beta Pricing and Alpha"
  fatores-risco: "S05 · Tracking Error and Risk Budgeting"
  grs: "S06 · The GRS Test"
  performance: "S07 · Statistics of Alpha and Biases"
  renda-fixa: "S08 · Expectations Hypothesis and the Term Premium"
  eventos: "S09 · Event Studies"
  primer-c: "Primer C · Bonds, Yields and Credit"
---

## sdf

Q: Two states $s\in\{1,2\}$ occur with probabilities $\pi(1),\pi(2)>0$. A bond costs $p_b$ and pays 1 in both states; a stock costs $p_s>0$ and pays $x(1)>x(2)>0$. The market is complete. Which pair gives the stochastic discount factor in state 1 and the exact condition under which a strictly positive discount factor exists?
- $m(1)=\dfrac{p_s-x(2)\,p_b}{x(1)-x(2)}$, and a positive $m$ exists if and only if $\dfrac{x(2)}{p_s}<\dfrac{1}{p_b}<\dfrac{x(1)}{p_s}$
- $m(1)=\dfrac{x(1)\,p_b-p_s}{\pi(1)[x(1)-x(2)]}$, and a positive $m$ exists if and only if $\dfrac{x(2)}{p_s}<\dfrac{1}{p_b}<\dfrac{x(1)}{p_s}$
- $m(1)=\dfrac{p_s-x(2)\,p_b}{\pi(1)[x(1)-x(2)]}$, and a positive $m$ exists if and only if $\dfrac{x(2)}{p_s}<\dfrac{1}{p_b}<\dfrac{x(1)}{p_s}$
- $m(1)=\dfrac{p_s-x(2)\,p_b}{\pi(1)[x(1)-x(2)]}$, and a positive $m$ exists if and only if $\dfrac{\pi(1)x(1)+\pi(2)x(2)}{p_s}>\dfrac{1}{p_b}$
<!-- YW5zOjI= -->
> Solve for the state prices first: $q(1)+q(2)=p_b$ and $q(1)x(1)+q(2)x(2)=p_s$ give $q(1)=\frac{p_s-x(2)p_b}{x(1)-x(2)}$ and $q(2)=\frac{x(1)p_b-p_s}{x(1)-x(2)}$. Then $m(s)=q(s)/\pi(s)$. The first option stops at $q(1)$ and forgets to divide by the probability. The second puts $q(2)$'s numerator in state 1. Positivity: $m(1)>0\iff p_s>x(2)p_b\iff x(2)/p_s<R_f$, and $m(2)>0\iff R_f<x(1)/p_s$. So no arbitrage means exactly that the riskless return lies strictly between the stock's two state returns. If it did not, one asset would dominate the other state by state, and a long–short position would be a free lottery. A positive expected excess return (last option) is neither necessary nor sufficient. It depends on the probabilities, and no-arbitrage does not.
> Ref: Ribeiro (2026), Ch. 1, §1.5.1 (p. 22), §1.5.4 (p. 24), §1.6.1 (p. 25)
> Similar: Ribeiro, Problems, Ch. 1 (p. 36); Cochrane, Asset Pricing, Ch. 4

## consumo

Q: Under power utility with relative risk aversion $\gamma$, the linearized consumption model gives $E[R^e]\approx\gamma\,\mathrm{cov}(\Delta\ln c,R^e)$ for an excess return $R^e$. Let $\beta_{\Delta c}=\mathrm{cov}(R^e,\Delta\ln c)/\mathrm{var}(\Delta\ln c)$ be the asset's consumption beta, $\sigma_c$ the volatility of log consumption growth, $\sigma_R$ the volatility of $R^e$ and $\rho$ their correlation. Which expression is the risk aversion implied by a measured premium, and how does it respond when consumption is measured by a smoother, time-averaged series?
- $\gamma=\dfrac{E[R^e]}{\beta_{\Delta c}\,\sigma_c^2}=\dfrac{E[R^e]}{\rho\,\sigma_c\,\sigma_R}$; a smaller $\sigma_c$ and a lower $\rho$ both raise the implied $\gamma$
- $\gamma=\dfrac{E[R^e]}{\beta_{\Delta c}\,\sigma_c}=\dfrac{E[R^e]}{\rho\,\sigma_R}$; only a lower $\rho$ raises the implied $\gamma$, since $\sigma_c$ cancels out
- $\gamma=\dfrac{E[R^e]}{\beta_{\Delta c}\,\sigma_c^2}=\dfrac{E[R^e]}{\rho\,\sigma_c\,\sigma_R}$; a smaller $\sigma_c$ raises $\beta_{\Delta c}$ enough to leave $\gamma$ unchanged
- $\gamma=\dfrac{\rho\,E[R^e]}{\beta_{\Delta c}\,\sigma_c^2}=\dfrac{E[R^e]}{\sigma_c\,\sigma_R}$; a smaller $\sigma_c$ raises the implied $\gamma$, while $\rho$ drops out
<!-- YW5zOjA= -->
> The consumption CAPM writes the premium as $\lambda_{\Delta c}\beta_{\Delta c}$ with $\lambda_{\Delta c}=\gamma\,\mathrm{var}(\Delta\ln c)$, so $\gamma=E[R^e]/(\beta_{\Delta c}\sigma_c^2)$. Substituting $\beta_{\Delta c}=\rho\sigma_R/\sigma_c$ gives $E[R^e]/(\rho\sigma_c\sigma_R)$. A smaller $\sigma_c$ does raise the beta, but only by $1/\sigma_c$ while the denominator carries $\sigma_c^2$, so on net it falls and $\gamma$ rises. That is why nondurables-and-services consumption, which is smoother, makes the puzzle *worse*. Time averaging lowers the measured $\rho$ and pushes the same way. With postwar data the market's beta is about 3.3 and the implied $\gamma$ is near 69. The puzzle is about both **smoothness** and **weak comovement**, and the formula shows each one separately.
> Ref: Ribeiro (2026), Ch. 2, §2.3.1 (p. 51), §2.3.3 (p. 52), §2.4.1 (pp. 55–57)
> Similar: Ribeiro, Problems, Ch. 2 (p. 72); Cochrane, Asset Pricing, Ch. 1 and Ch. 21

## fronteira

Q: $N$ risky assets have mean vector $\mu$ and invertible covariance matrix $\Sigma$, with frontier constants $A=\mathbf 1'\Sigma^{-1}\mathbf 1$, $B=\mathbf 1'\Sigma^{-1}\mu$, $C=\mu'\Sigma^{-1}\mu$ and $D=AC-B^2>0$. For a frontier portfolio $p$ with mean $m_p\neq B/A$, which expression is the mean $m_z$ of its zero-beta frontier companion, and what does it give when $p$ is the tangency portfolio for a riskless rate $R_f<B/A$?
- $m_z=\dfrac{B}{A}+\dfrac{D/A^2}{m_p-B/A}$; for the tangency portfolio $m_z=R_f$, and the companion lies on the efficient upper branch
- $m_z=\dfrac{B}{A}-\dfrac{D/A}{m_p-B/A}$; for the tangency portfolio $m_z=R_f$, and the companion lies on the inefficient lower branch
- $m_z=\dfrac{B}{A}-\dfrac{D/A^2}{m_p-B/A}$; for the tangency portfolio $m_z=B/A$, so the companion is the global minimum-variance portfolio
- $m_z=\dfrac{B}{A}-\dfrac{D/A^2}{m_p-B/A}$; for the tangency portfolio $m_z=R_f$, and the companion lies on the inefficient lower branch
<!-- YW5zOjM= -->
> The covariance of two frontier portfolios is $\frac1A+\frac AD(m_p-\frac BA)(m_q-\frac BA)$. Setting it to zero gives $m_z=\frac BA-\frac{D/A^2}{m_p-B/A}$. The tangency mean is $\mu_{tan}=\frac{C-R_fB}{B-R_fA}$, so $\mu_{tan}-\frac BA=\frac{D}{A(B-R_fA)}$. The fraction then becomes $\frac{B-R_fA}{A}=\frac BA-R_f$, and $m_z=R_f$. The zero-beta companion of the tangency portfolio earns the riskless rate. Geometrically, this is where the tangent line meets the vertical axis, and it is the seed of Black's zero-beta CAPM. Because $R_f<B/A$, the companion sits below the vertex, on the inefficient branch. The global minimum-variance portfolio is a trap: its covariance with every frontier portfolio is $1/A$, not zero.
> Ref: Ribeiro (2026), Ch. 3, §3.2.10 (p. 89), §3.3.3–3.3.4 (pp. 92–93)
> Similar: Ribeiro, Problems, Ch. 3 (p. 109); Cochrane, Asset Pricing, Ch. 5

## capm

Q: Let $m=a+b\,R_{mkt}$, with $a$ and $b$ chosen so that $m$ prices the riskless asset ($E[m]=1/R_f$) and the market ($E[m\,R_{mkt}]=1$). For an asset $i$ with excess return $R^e_i=R_i-R_f$, define its SDF pricing error $e_i\equiv E[m\,R^e_i]$ and its market beta $\beta_i=\mathrm{cov}(R_i,R_{mkt})/\mathrm{var}(R_{mkt})$. Which expression is asset $i$'s Jensen alpha $\alpha_i=E[R^e_i]-\beta_i\,(E[R_{mkt}]-R_f)$?
- $\alpha_i=e_i/R_f$, so a positive SDF pricing error is discounted one period into a smaller positive alpha
- $\alpha_i=R_f\,e_i$, so a positive SDF pricing error is compounded one period into a larger positive alpha
- $\alpha_i=e_i-R_f(1-\beta_i)$, so a zero SDF pricing error still leaves an alpha whenever $\beta_i\neq1$
- $\alpha_i=-b\,\sigma^2_{mkt}\,e_i$, so the SDF pricing error is scaled by the market premium into the alpha
<!-- YW5zOjE= -->
> Expand: $e_i=E[m]E[R^e_i]+\mathrm{cov}(m,R^e_i)=E[R^e_i]/R_f+b\,\mathrm{cov}(R_{mkt},R_i)$. With $b=-(E[R_{mkt}]-R_f)/(R_f\sigma^2_{mkt})$ the second term is $-\beta_i(E[R_{mkt}]-R_f)/R_f$, so $e_i=\alpha_i/R_f$ and $\alpha_i=R_f\,e_i$. This is the three-way equivalence at work. $\alpha_i=0$ for every asset exactly when the market-linear SDF prices every excess return, which in turn holds exactly when the market is mean–variance efficient. The alpha is the SDF pricing error expressed in return units. The option with $R_f(1-\beta_i)$ mixes in the raw-return regression trap, where the CAPM predicts a nonzero intercept $R_f(1-\beta_i)$ in a regression of *raw* returns. That term has nothing to do with the SDF error.
> Ref: Ribeiro (2026), Ch. 4, §4.3.1–4.3.3 (pp. 126–128), §4.4.1 (p. 129), §4.4.3 (p. 130)
> Similar: Ribeiro, Problems, Ch. 4 (p. 146); Cochrane, Asset Pricing, Ch. 6

## fatores-risco

Q: A manager is measured against a benchmark. Her active weights $w_a=w_p-w_b$ sum to zero, stocks have market betas $\beta_i$ and idiosyncratic variances $\sigma^2(\varepsilon_i)$, residuals are uncorrelated across stocks, and the market variance is $\sigma_m^2$. She runs one large underweight in a low-idiosyncratic-risk stock, funding two small overweights in high-idiosyncratic-risk stocks, and her active beta $\beta'w_a$ is close to zero. Which reading of her risk budget is correct?
- Tracking error is close to her total volatility $\sqrt{w_p'\Sigma w_p}$, since a beta-neutral book strips out market risk, and the volatile overweights dominate because risk follows each name's volatility
- Tracking error is dominated by the market term $(\beta_p^2-\beta_b^2)\,\sigma_m^2$, since the underweight lowers the portfolio's beta while the benchmark's is unchanged, leaving an unhedged market bet
- Tracking error is almost all selection risk $\sum_i w_{a,i}^2\,\sigma^2(\varepsilon_i)$, and the large underweight can dominate it, because each position enters through its squared active weight
- Tracking error is almost all selection risk $\sum_i |w_{a,i}|\,\sigma(\varepsilon_i)$, and the overweights dominate it, because an underweight partly hedges its own idiosyncratic risk
<!-- YW5zOjI= -->
> Under the factor model $TE^2=(\beta_p-\beta_b)^2\sigma_m^2+\sum_i w_{a,i}^2\sigma^2(\varepsilon_i)$. The market term uses the *square of the active beta*, not a difference of squared betas, and it vanishes here because $\beta'w_a\approx0$. What remains is selection risk. Each position contributes $w_{a,i}^2\sigma^2(\varepsilon_i)$, so risk follows the size of the bet *squared*. In Example 5.5 the −10% underweight in the least volatile name contributes about half the selection variance. Total volatility is a different object: it keeps the full $\beta_p^2\sigma_m^2$ that the benchmark-relative view removes. Summing $|w|\sigma$ adds volatilities as if residuals were perfectly correlated, which contradicts the uncorrelated-residual assumption in the stem.
> Ref: Ribeiro (2026), Ch. 5, §5.3.5 (p. 165), §5.3.7 and Example 5.5 (p. 166)
> Similar: Ribeiro, Problems, Ch. 5 (p. 183); BKM 13e, Ch. 8

## grs

Q: Two traded-factor models, M1 and M2, are tested on the same $N$ assets over the same $T$ periods with $GRS=\frac{T-N-K}{N}\cdot\frac{\hat\alpha'\hat\Sigma^{-1}\hat\alpha}{1+\bar f'\hat\Omega^{-1}\bar f}$, where $\hat\alpha$ holds the intercepts, $\hat\Sigma$ is the residual covariance, $\bar f$ and $\hat\Omega$ are the factors' sample mean and covariance, and $K$ is the number of factors. Both models use $K$ factors and deliver identical $\hat\alpha$ and $\hat\Sigma$, but M2's factors reach a higher maximum Sharpe ratio. How do the two statistics compare, and why?
- M2's statistic is lower, since the same Sharpe-ratio gain $\theta^2(f,R)-\theta^2(f)$ is scaled by a larger $1+\theta^2(f)$, so given alphas are less surprising against it
- M2's statistic is higher, since factors with a higher Sharpe ratio $\theta(f)$ make the same alphas more precisely estimated, so they look more significant against it
- The statistics are equal, since rejection depends only on $\hat\alpha'\hat\Sigma^{-1}\hat\alpha$ and the factors' Sharpe ratio $\theta(f)$ enters only through the degrees of freedom
- M2's statistic is lower, since factors with a higher Sharpe ratio $\theta(f)$ must span the tangency portfolio of factors plus assets, which forces its alphas to zero
<!-- YW5zOjA= -->
> The numerator $\hat\alpha'\hat\Sigma^{-1}\hat\alpha$ equals $\theta^2(f,R)-\theta^2(f)$. This is how much the maximum squared Sharpe ratio rises when the test assets are added to the factors, and it is what drives rejection. The denominator $1+\theta^2(f)$ normalizes that gain. The same term inflates the standard error of an alpha, $se(\hat\alpha)\propto\sqrt{1+\bar f'\hat\Omega^{-1}\bar f}$, so alphas estimated against high-Sharpe factors are *noisier*, not sharper. Hence the same alphas are less significant. The last option confuses population with sample: spanning would set true alphas to zero, but here the estimated alphas are given and nonzero. Degrees of freedom depend on $T,N,K$ only.
> Ref: Ribeiro (2026), Ch. 6, §6.5.2 (p. 206); Ch. 7, §7.3.1 (p. 238)
> Similar: Ribeiro, Problems, Ch. 6 (p. 220); Cochrane, Asset Pricing, Ch. 12

## performance

Q: A manager's true monthly residual returns $\varepsilon_t$ are i.i.d. with volatility $\sigma(\varepsilon)$, and her true information ratio is $IR=\alpha/\sigma(\varepsilon)$. Her assets are appraised rather than traded, so she reports $\tilde\varepsilon_t=\theta\,\varepsilon_t+(1-\theta)\,\varepsilon_{t-1}$ with $0<\theta<1$, which leaves the alpha unchanged. An analyst ignores serial correlation and computes the record length needed for the alpha's $t$-statistic to reach $t_{crit}$ as $\tilde T=(t_{crit}/\widetilde{IR})^2$ from the reported series. Which pair gives $\tilde T$ and the reported first-order autocorrelation $\tilde\rho_1$?
- $\tilde T=\dfrac{(t_{crit}/IR)^2}{\theta^2+(1-\theta)^2}$ and $\tilde\rho_1=\dfrac{\theta(1-\theta)}{\theta^2+(1-\theta)^2}$, so the analyst overstates how long skill takes to show
- $\tilde T=[\theta^2+(1-\theta)^2]\,(t_{crit}/IR)^2$ and $\tilde\rho_1=\theta(1-\theta)\,\sigma^2(\varepsilon)$, so the analyst understates how long skill takes to show
- $\tilde T=\sqrt{\theta^2+(1-\theta)^2}\;(t_{crit}/IR)^2$ and $\tilde\rho_1=\dfrac{\theta(1-\theta)}{\theta^2+(1-\theta)^2}$, so the analyst understates how long skill takes to show
- $\tilde T=[\theta^2+(1-\theta)^2]\,(t_{crit}/IR)^2$ and $\tilde\rho_1=\dfrac{\theta(1-\theta)}{\theta^2+(1-\theta)^2}$, so the analyst understates how long skill takes to show
<!-- YW5zOjM= -->
> The reported variance is $[\theta^2+(1-\theta)^2]\sigma^2(\varepsilon)$, which is below $\sigma^2(\varepsilon)$ for any $0<\theta<1$ and at its minimum of one half when $\theta=\tfrac12$. The mean is untouched, so $\widetilde{IR}=IR/\sqrt{\theta^2+(1-\theta)^2}$. Squaring $t_{crit}/\widetilde{IR}$ then multiplies the true requirement $(t_{crit}/IR)^2$ by the variance factor itself, not by its square root. The autocovariance is $\theta(1-\theta)\sigma^2$, and dividing by the reported variance gives $\tilde\rho_1$. $\theta(1-\theta)\sigma^2(\varepsilon)$ is the autocovariance, not the autocorrelation. Smoothing makes the Sharpe ratio "lie": a flattering ratio combined with positive autocorrelation is the red flag. Survivorship and backfill are different biases. They inflate the *mean* through selection, whereas smoothing deflates the *denominator*. Unsmoothing (Getmansky–Lo–Makarov) restores $\sigma(\varepsilon)$.
> Ref: Ribeiro (2026), Ch. 7, §7.3.1 (p. 238), §7.3.3 (p. 239), §7.3.4–7.3.5 (pp. 240–241)
> Similar: Ribeiro, Problems, Ch. 7 (p. 258); BKM 13e, Ch. 24

## renda-fixa

Q: A two-period zero-coupon bond is priced by $P^{(2)}_t=E_t[m_{t+1}P^{(1)}_{t+1}]$, where $m_{t+1}$ is the stochastic discount factor and $P^{(1)}_{t+1}=1/R_{f,t+1}$ is next period's one-period bond price. In a flight-to-quality regime, recessions (the high-$m_{t+1}$ states) bring falling short rates; in an inflationary regime, bad times bring rising short rates. Up to convexity (Jensen) terms, which statement about the flight-to-quality regime is correct?
- $\mathrm{cov}_t(m_{t+1},P^{(1)}_{t+1})<0$, so $P^{(2)}_t$ sits lower than its expectations-hypothesis value, the forward rate overstates the expected short rate, and the term premium is positive
- $\mathrm{cov}_t(m_{t+1},P^{(1)}_{t+1})>0$, so $P^{(2)}_t$ sits higher than its expectations-hypothesis value, the forward rate understates the expected short rate, and the term premium is negative
- $\mathrm{cov}_t(m_{t+1},P^{(1)}_{t+1})>0$, so $P^{(2)}_t$ sits lower than its expectations-hypothesis value, the forward rate overstates the expected short rate, and the term premium is positive
- $\mathrm{cov}_t(m_{t+1},P^{(1)}_{t+1})=0$, so $P^{(2)}_t$ equals its expectations-hypothesis value, since the bond repays its face value for sure at maturity, and the term premium is zero
<!-- YW5zOjE= -->
> Expand: $P^{(2)}_t=E_t[P^{(1)}_{t+1}]/R_{f,t}+\mathrm{cov}_t(m_{t+1},P^{(1)}_{t+1})$. The first term is the expectations-hypothesis price. In a flight to quality, rates fall when $m$ is high, so the one-period bond's future price is high exactly when $m$ is high. The covariance is positive and the long bond trades *rich*. It is a hedge, so its expected excess return, $-R_f\,\mathrm{cov}(m,R^e)$, is negative, and the forward rate lies below the expected short rate. The inflationary regime flips every sign, which gives the positive, volatile premium of the 1970s–80s. The certain face value (last option) removes cash-flow risk only; the interim price still moves with rates.
> Ref: Ribeiro (2026), Ch. 8, §8.4 (pp. 272–273), §8.4.3 (p. 275), §8.5.1 (p. 276)
> Similar: Ribeiro, Example 8.3 (p. 277); Problems, Ch. 8 (p. 294)

## eventos

Q: A researcher studies $N$ bank dividend cuts, all announced in the same crisis fortnight. For each bank she estimates the market model over $\tau\in[-250,-11]$ trading days, computes $AR_{i\tau}=R_{i\tau}-\hat\alpha_i-\hat\beta_iR_{mkt,\tau}$ over $\tau\in[0,+750]$, sums them into $CAR_i$, and standardizes the average by the estimation-window residual variance. Her $t$-statistic is very large. Which diagnosis is right?
- The design is sound, since the estimation window closes before the event window opens, so $\hat\alpha_i$ and $\hat\beta_i$ are clean and the large $t$ reflects a genuinely slow price response
- Only the horizon is a problem, since summing arithmetic abnormal returns over three years distorts them; switching from $CAR_i$ to buy-and-hold returns would leave a valid, smaller $t$
- Three pitfalls inflate $t$: clustering makes the $CAR_i$ dependent, event-induced variance exceeds the estimation variance, and small errors in $\hat\alpha_i,\hat\beta_i$ accumulate over three years
- Only clustering is a problem, since events in one fortnight share a common shock; standardizing by the cross-sectional dispersion of the $CAR_i$ would fully repair the resulting test
<!-- YW5zOjI= -->
> Clean windows are necessary but not sufficient. (i) All events fall in one fortnight, so the CARs share a common component. The effective sample is far below $N$, and even a cross-sectional standard error does not remove a shock that is common to all of them. (ii) The crisis raises residual volatility, so the estimation-window variance understates the event-window variance and the test over-rejects. (iii) Over 750 days a benchmark error of $\delta_\alpha$ per day and $\delta_\beta$ in beta adds a drift of about $-750(\delta_\alpha+\delta_\beta\bar R_{mkt})$. This is the bad-model problem: the joint hypothesis bites hardest at long horizons. Switching from CAR to BHAR changes how returns are cumulated, not the benchmark error. Short, dispersed windows are where event studies are credible.
> Ref: Ribeiro (2026), Ch. 9, §9.2.1–9.2.4 (pp. 306–308), §9.2.5 (p. 310)
> Similar: Ribeiro, Problems, Ch. 9 (p. 328); BKM 13e, Ch. 11

## primer-c

Q: A corporate coupon bond trades at a premium to par, its yield is expected to stay constant until maturity, and its promised cash flows carry a small default probability concentrated in recessions. Which set of claims about it is correct?
- Its current yield exceeds both its coupon rate and its YTM; its price drifts up toward par; and its promised YTM equals its expected return, since the default risk is small
- Its coupon rate exceeds its current yield, which exceeds its YTM; its price drifts down to par; and the whole spread over Treasuries is expected loss, since small risks carry no premium at all
- Its YTM exceeds its current yield, which exceeds its coupon rate; its price drifts down to par; and its promised YTM overstates its expected yield by the expected-loss piece of the spread
- Its coupon rate exceeds its current yield, which exceeds its YTM; its price drifts down to par; and its spread is expected loss plus a premium for defaulting when marginal utility is high
<!-- YW5zOjM= -->
> A premium bond has coupon rate > yield. Current yield is the coupon over a price exceeding par, so it is below the coupon rate. The YTM also counts the pull-to-par capital *loss*, so it is lower still: coupon > CY > YTM (the discount-bond ordering reversed). At a constant yield the price converges down to par, and that drift is exactly what makes the total return equal the yield. The YTM computed from promised flows is a *promised* yield, which is the maximum achievable. The spread decomposes as (promised − expected) = expected loss, plus (expected − Treasury) = risk premium. The premium is positive because defaults cluster when $m_{t+1}$ is high ($\mathrm{cov}(m,R^e)<0$). How small the probability is does not matter; its timing does. This is why most of the observed spread is premium (the credit-spread puzzle).
> Ref: Ribeiro (2026), App. C, §C.4.2 (p. 377), §C.6 (pp. 378–379), §C.7.3 (pp. 381–382)
> Similar: Ribeiro, Problems, App. C (p. 385); BKM 13e, Ch. 14
