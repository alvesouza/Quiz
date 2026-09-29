---
quiz: "Full-Course Review — Round 1 of 5"
tags:
  s01: "S01 · The Central Equation and the Law of One Price"
  s02: "S02 · From the Euler Equation to the SDF"
  s03: "S03 · The Diversification Limit"
  s04: "S04 · Market = Tangency, and the SML"
  s05: "S05 · The Index Model as a Risk Model"
  s06: "S06 · Linear SDF, Beta Pricing, and the APT"
  s07: "S07 · Performance Measures and Mandates"
  s08: "S08 · Spot Rates, Forwards, Bootstrapping"
  s09: "S09 · Efficiency and the Joint Hypothesis"
  pa: "Primer A · Matrices, Definiteness, Projection"
---

## s01

Q: Two traded portfolios deliver the identical payoff $x_{t+1}$ in every state of nature, yet trade today at different prices. What follows for the CAPM, the APT and every multifactor beta-pricing model?
- No discount factor of any sign can price both portfolios, so no beta-pricing model can fit both prices either, since each such model is a restriction on $m$.
- A discount factor $m$ still exists but is negative in some state, so only the models whose prices of risk are all positive are ruled out by the observation.
- A discount factor $m$ exists only if markets are incomplete, so the beta-pricing models survive provided their factors do not span the full payoff space.
- The gap is an alpha relative to any model of $m$, so beta pricing still holds for the remaining assets and the price difference is purely idiosyncratic.
<!-- YW5zOjA= -->
> The law of one price is exactly what makes the pricing functional linear, and linearity is all that existence of $m$ requires; a violation therefore kills existence itself, not just positivity. Every model in the course (CAPM, consumption CAPM, APT, Fama–French) is a special form of $p = E[m\,x]$ — beta pricing is the linear-SDF statement rewritten — so none of them can price two different numbers for one payoff. Negativity of $m$ is the symptom of an arbitrage under the law of one price, a different failure; incompleteness never rescues a law-of-one-price violation; and an alpha is a pricing error of a *model*, not a contradiction among observed prices.
> Ref: Ribeiro (2026), Ch. 1, §1.4.3 (p. 16), §1.5.2 (pp. 22–23), §1.5.4 (p. 24); Ch. 6, §6.1.2 (pp. 191–192)
> Similar: Cochrane, Asset Pricing, Ch. 4 §4.1–4.2

## s02

Q: An investor with time-separable utility $u(c_t)+\beta E_t[u(c_{t+1})]$, $u'>0$, $u''<0$, may buy any amount $\xi$ of a traded asset at price $p_t$ with payoff $x_{t+1}$, cutting consumption today by $p_t\xi$. Relative to the Chapter 1 existence result for a discount factor, what does her first-order condition add?
- It proves the discount factor unique: every investor equates the same prices to her marginal rate of substitution, so all of them share one $m$ in every state.
- It requires complete markets, since the first-order condition holds for an asset only if she can also trade a separate claim on each state of nature.
- It names $m_{t+1}=\beta u'(c_{t+1})/u'(c_t)$, strictly positive since $u'>0$, so her $m$ rules out arbitrage in every asset she trades, complete markets or not.
- It delivers a discount factor only under power utility, since for a general concave $u$ the condition does not factor into a price times marginal utility.
<!-- YW5zOjI= -->
> The marginal argument (buy $\xi$, set the derivative at $\xi=0$ to zero) gives $p_t u'(c_t)=E_t[\beta u'(c_{t+1})x_{t+1}]$ for *any* concave $u$, and dividing by $u'(c_t)$ identifies the abstract $m$ as the marginal rate of substitution. Because marginal utility is positive, this $m$ is positive in every state — the property Chapter 1 could only obtain by ruling out arbitrage. Nothing requires completeness: the condition holds asset by asset for whatever she trades. Uniqueness does *not* follow: with incomplete markets, different investors' marginal rates of substitution may differ in directions no traded payoff can detect.
> Ref: Ribeiro (2026), Ch. 2, §2.1.1–2.1.2 (pp. 42–44); Ch. 1, §1.5.4 (p. 24)
> Similar: Cochrane, Asset Pricing, Ch. 1 §1.2

## s03

Q: A universe of $N$ assets obeys the single-index model $R^e_i=\alpha_i+\beta_iR^e_m+\varepsilon_i$, with residuals uncorrelated across assets and with the market, market variance $\sigma_m^2$, and bounded residual variances. Let $\bar\beta=\frac1N\sum_i\beta_i$ and $\overline{\beta^2}=\frac1N\sum_i\beta_i^2$. As $N\to\infty$, the equally weighted portfolio's variance converges to the average-covariance floor. Which expression is the floor?
- $\sigma_m^2\,\overline{\beta^2}$, since each asset's systematic variance is $\beta_i^2\sigma_m^2$ and the floor averages the systematic parts
- $\bar\beta^{\,2}\sigma_m^2$, since each pairwise covariance is $\beta_i\beta_j\sigma_m^2$ and the average over $i\neq j$ tends to it
- $\bar\beta\,\sigma_m^2$, since each asset's covariance with the market is $\beta_i\sigma_m^2$ and the floor averages those terms
- $\bar\beta^{\,2}\sigma_m^2+\overline{\sigma^2_\varepsilon}$, since residual variance persists in the floor next to the common factor part
<!-- YW5zOjE= -->
> The equal-weight variance is $\frac1N\overline{\sigma^2}+(1-\frac1N)\overline{\text{cov}}$, so the floor is the average *off-diagonal* covariance. Under the index model $\text{cov}_{ij}=\beta_i\beta_j\sigma_m^2$, and $\frac{1}{N(N-1)}\sum_{i\ne j}\beta_i\beta_j=\frac{N^2\bar\beta^2-N\overline{\beta^2}}{N(N-1)}\to\bar\beta^{\,2}$. Directly: $\beta_p=\bar\beta$ and the residual term $\frac{1}{N}\overline{\sigma^2_\varepsilon}\to 0$. The trap $\overline{\beta^2}$ is the average *own* systematic variance; it exceeds $\bar\beta^{\,2}$ by the cross-sectional variance of beta, which diversifies because high- and low-beta names partly offset in the portfolio's beta.
> Ref: Ribeiro (2026), Ch. 3, §3.1.6 (pp. 82–83); Ch. 5, §5.3.2–5.3.3 (pp. 162–164)
> Similar: BKM 13e, Ch. 8 §8.2

## s04

Q: An investor holds the market portfolio $M$, with excess return $R^e_m$ and variance $\sigma_m^2$, which is assumed to have the highest attainable Sharpe ratio. She considers adding a small weight $\delta$ in asset $i$ (return $R_i$), financed at the risk-free rate $R_f$, and writes the Sharpe ratio $S(\delta)$ of the result. Imposing $S'(0)=0$ yields which condition?
- $E[R_i]-R_f=(E[R_m]-R_f)\,\sigma_i/\sigma_m$, so each asset is priced by its own volatility relative to the market's
- $E[R_i]-R_f=(E[R_m]-R_f)\,\mathrm{cov}(R_i,R_m)/(2\sigma_m^2)$, since the variance grows by $2\delta\,\mathrm{cov}$ at first order
- $E[R_i]-R_f=(E[R_m]-R_f)\,\mathrm{cov}(R_i,R_m)/\sigma_m$, so the premium is covariance per unit of market volatility
- $E[R_i]-R_f=(E[R_m]-R_f)\,\mathrm{cov}(R_i,R_m)/\sigma_m^2$, so only the marginal covariance with the market is priced
<!-- YW5zOjM= -->
> To first order, $E[R^e_p]=E[R^e_m]+\delta(E[R_i]-R_f)$ and $\text{var}(R_p)=\sigma_m^2+2\delta\,\text{cov}(R_i,R_m)$. Differentiating $S=E[R^e_p]/\sqrt{\text{var}}$ at $\delta=0$: $\frac{E[R_i]-R_f}{\sigma_m}-E[R^e_m]\frac{\tfrac12\cdot 2\,\text{cov}(R_i,R_m)}{\sigma_m^3}=0$. The $2$ from the variance is cancelled by the $\tfrac12$ from the square root (so the "$/2\sigma_m^2$" option forgets the chain rule), and multiplying by $\sigma_m$ leaves $\sigma_m^2$, not $\sigma_m$, in the denominator: beta. The $\sigma_i/\sigma_m$ version is the capital market line, valid only for efficient portfolios — risk is a marginal contribution, not a standalone volatility.
> Ref: Ribeiro (2026), Ch. 4, §4.2.1 (pp. 120–121); Ch. 3, §3.1.8 (p. 84)
> Similar: BKM 13e, Ch. 9 §9.1

## s05

Q: The single-index covariance matrix is $\Sigma=\sigma_m^2\beta\beta'+D$, with $D=\mathrm{diag}(\sigma^2_{\varepsilon_1},\dots,\sigma^2_{\varepsilon_N})$, $\beta$ the vector of market betas and $\sigma_m^2$ the market variance. Let $A=\sum_j\beta_j/\sigma^2_{\varepsilon_j}$ and $B=\sum_j\beta_j^2/\sigma^2_{\varepsilon_j}$. Applying Sherman–Morrison to the global minimum-variance weights $w_{mv}\propto\Sigma^{-1}\mathbf 1$ gives which weight for asset $i$?
- $w_i\propto\frac{1}{\sigma^2_{\varepsilon_i}}\Big(1-\frac{\sigma_m^2A}{1+\sigma_m^2B}\,\beta_i\Big)$
- $w_i\propto\frac{1}{\sigma^2_{\varepsilon_i}}\Big(1+\frac{\sigma_m^2A}{1+\sigma_m^2B}\,\beta_i\Big)$
- $w_i\propto\frac{1}{\sigma^2_{\varepsilon_i}}\Big(1-\frac{\sigma_m^2A}{\sigma_m^2B}\,\beta_i\Big)$
- $w_i\propto\frac{1}{\sigma^2_{\varepsilon_i}}\Big(1-\frac{\sigma_m^2B}{1+\sigma_m^2A}\,\beta_i\Big)$
<!-- YW5zOjA= -->
> Sherman–Morrison gives $\Sigma^{-1}=D^{-1}-\sigma_m^2\frac{D^{-1}\beta\beta'D^{-1}}{1+\sigma_m^2\beta'D^{-1}\beta}$. Multiply by $\mathbf 1$: $\beta'D^{-1}\mathbf 1=A$ and $\beta'D^{-1}\beta=B$, so $\Sigma^{-1}\mathbf 1=D^{-1}\mathbf 1-\frac{\sigma_m^2A}{1+\sigma_m^2B}D^{-1}\beta$, whose $i$-th entry is the first option. It reads as two forces: overweight quiet names ($1/\sigma^2_{\varepsilon_i}$) and underweight high betas (the minus sign), since beta is the only channel of common risk. The plus sign reverses the second force; dropping the $1$ in the denominator is the limit $\sigma_m^2B\to\infty$, not the exact inverse; swapping $A$ and $B$ breaks the dimension of the scalar. The inverse always exists because the denominator exceeds one — the cure for the near-singular sample $\Sigma$ of Chapter 3.
> Ref: Ribeiro (2026), Ch. 5, §5.2.4 (p. 160); App. A, §A.6 (pp. 340–342)
> Similar: Ribeiro, Problems, Ch. 5

## s06

Q: Excess returns $R^e_i$ are priced by $0=E[m\,R^e_i]$ with a linear discount factor $m=a-b'f$, where $f$ is a $K$-vector of factors with nonsingular covariance matrix $\Sigma_F$, $E[m]=1/R_f$, and $R_f$ is the gross risk-free rate. Suppose every factor is itself a traded excess return. Which expression for $b$ follows, and how is it read?
- $b=R_f\,\Sigma_F^{-1}E[f]$, proportional to the tangency weights on the factors, so $m$ is affine in the maximum-Sharpe factor portfolio
- $b=\frac{1}{R_f}\Sigma_F\,E[f]$, proportional to each factor's covariance-weighted mean, so $m$ loads most on the most volatile factor
- $b=\frac{1}{R_f}\Sigma_F^{-1}E[f]$, proportional to the tangency weights on the factors, so $m$ is affine in the maximum-Sharpe factor portfolio
- $b=\frac{1}{R_f}\Sigma_F^{-1}\mathbf 1$, proportional to the minimum-variance weights on the factors, so $m$ is affine in the least-risky factor portfolio
<!-- YW5zOjI= -->
> From $0=E[m]E[R^e_i]+\text{cov}(m,R^e_i)$: $E[R^e_i]=-R_f\,\text{cov}(m,R^e_i)=R_f\,\text{cov}(R^e_i,f)\,b=\beta_i'(R_f\Sigma_Fb)$, so $\lambda=R_f\Sigma_Fb$ — linear SDF and beta pricing are one statement. A traded factor prices itself, so $\lambda=E[f]$, and inverting gives $b=\Sigma_F^{-1}E[f]/R_f$: exactly the tangency direction $\Sigma^{-1}\mu^e$ of Chapter 3 applied to the factors. The discount factor is therefore affine in the factors' maximum-Sharpe portfolio, the multifactor version of the CAPM's $m$ affine in the market. Multiplying by $R_f$ instead of dividing inverts $\lambda=R_f\Sigma_Fb$; $\Sigma_F$ without the inverse and $\Sigma_F^{-1}\mathbf 1$ confuse the tangency with other frontier objects. The APT reaches the same beta pricing only approximately, from no-arbitrage plus a factor structure.
> Ref: Ribeiro (2026), Ch. 6, §6.1.2–6.1.3 (pp. 191–192), §6.1.5 (p. 193), §6.2.1 (p. 195); Ch. 3, §3.3.3 (p. 92)
> Similar: Cochrane, Asset Pricing, Ch. 6 §6.3

## s07

Q: A concentrated fund has a higher Treynor ratio but a lower Sharpe ratio than a diversified fund. Which statement reconciles the two rankings using the diversification limit and the security market line?
- Jensen's alpha settles it, since alpha is the vertical distance to the security market line and is therefore already adjusted for the idiosyncratic risk both measures disagree about.
- Held alone, the concentrated fund's idiosyncratic variance is borne, so Sharpe (and $M^2$) rank; as one sleeve of many, that variance diversifies at rate $1/N$, so Treynor ranks.
- $M^2$ settles it, since rescaling each fund to the market's volatility removes the idiosyncratic component and so reproduces the Treynor ranking for either use of the fund.
- Sharpe is correct for both uses, since idiosyncratic risk carries a premium in any finite book, and Treynor overstates a sleeve by ignoring the residual it adds.
<!-- YW5zOjE= -->
> Each measure's denominator is an assumption about how the fund is held. As the whole risky holding, total volatility is what the investor bears, so Sharpe ranks, and $M^2=(S_p-S_m)\sigma_m$ is a relabelling that ranks identically. As one of many uncorrelated sleeves, the residual variance enters the book with weight $w_i^2$ and dies as $1/N$ — the diversification floor — leaving beta as the only consumed risk, so Treynor ranks. Jensen's alpha is a numerator with no risk denominator at all; idiosyncratic risk is not priced in the SML, which is exactly why the sleeve use can ignore it.
> Ref: Ribeiro (2026), Ch. 7, §7.2.2 (pp. 234–235); Ch. 5, §5.3.2 (p. 162); Ch. 4, §4.6.3 (p. 144)
> Similar: BKM 13e, Ch. 24 §24.1

## s08

Q: A one-year zero-coupon bond fixes the discount factor $d_1=1/(1+s_1)$. A two-year bond with face value $1$ and annual coupon rate $c$ trades at price $P_2$. Let $d_2=1/(1+s_2)^2$ and let $f_{1,2}$ be the one-year rate one year forward. Which pair of expressions is correct?
- $d_2=\frac{P_2-c}{(1+c)\,d_1}$ and $1+f_{1,2}=d_1/d_2$, so the forward is the ratio of adjacent discount factors
- $d_2=\frac{P_2-c\,d_1}{1+c}$ and $1+f_{1,2}=d_2/d_1$, so the forward is the ratio of adjacent discount factors
- $d_2=\frac{P_2}{1+c}-c\,d_1$ and $1+f_{1,2}=d_1/d_2$, so the forward is the ratio of adjacent discount factors
- $d_2=\frac{P_2-c\,d_1}{1+c}$ and $1+f_{1,2}=d_1/d_2$, so the forward is the ratio of adjacent discount factors
<!-- YW5zOjM= -->
> The coupon bond is a portfolio of zeros, so by the law of one price $P_2=c\,d_1+(1+c)\,d_2$; strip the year-one coupon at its known price and divide: $d_2=(P_2-c\,d_1)/(1+c)$. The forward follows from equating two riskless routes to year two, $(1+s_2)^2=(1+s_1)(1+f_{1,2})$, i.e. $1+f_{1,2}=d_1/d_2>1$ whenever $d_2<d_1$. The inverted ratio $d_2/d_1$ gives a gross rate below one; dividing $P_2-c$ by $d_1$ treats the coupon as undiscounted; and $P_2/(1+c)-c\,d_1$ forgets to scale the stripped coupon by $1/(1+c)$.
> Ref: Ribeiro (2026), Ch. 8, §8.2.1–8.2.3 (pp. 266–268); Ch. 1, §1.4.3 (p. 16)
> Similar: BKM 13e, Ch. 15 §15.2–15.3

## s09

Q: An event study finds that buying stocks after public earnings announcements earns a positive and significant CAPM alpha (intercept of the excess return on the market excess return), but a zero Fama–French three-factor alpha (market, size SMB, value HML). What may be concluded about market efficiency?
- Neither verdict isolates efficiency: each is a joint test with its benchmark, and a zero FF3 alpha cannot say whether SMB and HML are risk or mispricing.
- The semi-strong form holds, since FF3 prices the strategy and it is the better-fitting model, so the CAPM alpha is only compensation for size and value risk.
- The weak form is rejected, since the profit comes from trading on past returns around the announcement, which is information contained in the price history.
- The semi-strong form is rejected, since the CAPM is the equilibrium model and a zero FF3 alpha merely reflects factors mined from the same anomalies.
<!-- YW5zOjA= -->
> An abnormal return is realised minus *normal* return, and normal comes from a model, so every efficiency test is a joint test. The CAPM result rejects "efficiency and CAPM"; the FF3 result fails to reject "efficiency and FF3". Whether that means efficiency holds depends on whether SMB and HML are covariances with a priced risk or characteristics proxying for mispricing — the characteristics-versus-covariances question the data alone cannot settle. The announcement is public information, so the test is semi-strong, not weak; and declaring either model "the" equilibrium model assumes away the joint-hypothesis problem.
> Ref: Ribeiro (2026), Ch. 9, §9.1.1 (p. 301), §9.1.3 (p. 303); Ch. 6, §6.2.4 (p. 197)
> Similar: BKM 13e, Ch. 11 §11.3–11.4

## pa

Q: A regression of an asset's excess return on factors $f_1,f_2$ (plus a constant) is re-run after adding $f_3=f_1-f_2$. Let $\Sigma_F$ be the factor covariance matrix and $X$ the $T\times K$ regressor matrix. What happens?
- $\Sigma_F$ stays positive definite, because each factor has positive variance, so the loadings remain unique and $R^2$ rises because a regressor was added.
- $\Sigma_F$ is singular, so the projection itself is undefined, and the fitted values, the residuals and $R^2$ can no longer be computed at all.
- $\Sigma_F$ is singular and the loadings are not unique, but the fitted values and $R^2$ are unchanged, since the column space of $X$ is unchanged.
- $\Sigma_F$ is singular but the loadings are unique, and the residual variance falls to zero, since $f_3$ is an exact portfolio of the other factors.
<!-- YW5zOjI= -->
> With $w=(1,-1,-1)'$, $w'\Sigma_Fw=\text{var}(f_1-f_2-f_3)=0$ for $w\neq0$, so $\Sigma_F$ is only semidefinite and singular, and so is $X'X$: the regression twin of a redundant asset. $(X'X)^{-1}$ does not exist, so the loadings are not unique (any multiple of $w$ can be added). But OLS is a projection onto the column space of $X$, and adding a column already in that span changes neither the subspace, nor the fitted values $\hat y$, nor the residual, nor $R^2$. Positive variance of each factor is necessary for definiteness, not sufficient; and a redundant regressor adds no explanatory power, so the residual does not vanish.
> Ref: Ribeiro (2026), App. A, §A.4 (pp. 338–339), §A.8.3 (p. 346); Ch. 6, §6.6.4 (p. 211)
> Similar: Ribeiro, Problems, App. A
