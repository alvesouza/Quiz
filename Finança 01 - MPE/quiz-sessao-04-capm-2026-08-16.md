---
quiz: "Session 4 — The CAPM as a Special SDF"
tags:
  equil: "1 · Equilibrium: Market = Tangency"
  sml: "2 · The Security Market Line"
  linsdf: "3 · The CAPM as a Linear SDF"
  alpha: "4 · Alpha, Index Model, Beta"
  empir: "5 · Does It Work? The Flat SML"
  uses: "6 · Uses and Abuses"
---

## equil

Q: The equilibrium argument runs: mean-variance optimizers with homogeneous expectations all hold the tangency portfolio, and market clearing then makes the market portfolio efficient. Which assumption performs the aggregation step?
- The existence of a risk-free asset, since without it no investor could split the allocation decision into a cash position and a single risky position.
- The absence of frictions, since transaction costs and taxes would otherwise drive a wedge between the price paid and the price received by any investor.
- Homogeneous expectations, since shared means and covariances put every investor on one tangency portfolio, whose value-weighted sum must be the market.
- Price-taking behaviour, since an investor large enough to move prices would face a budget set that is no longer linear in the quantities being traded.
<!-- YW5zOjI= -->
> Two-fund separation gets each investor onto *some* tangency portfolio; homogeneous expectations make that portfolio the same one for everybody. Summing identical portfolios and clearing forces it to be the market. The other assumptions are needed for the argument to run, but none does the aggregating.
> Ref: Ribeiro (2026), Ch. 4, §4.1 (p. 117); BKM 13e, §9.1 (p. 283)
> Similar: Ribeiro, Problem 4.5 (p. 147); H&L, Ch. 4 §4.1–4.9 (pp. 83–91)

Q: Remove the risk-free asset from that economy and change nothing else. What survives?
- Nothing survives: without a risk-free rate the tangency portfolio is undefined, so no equilibrium relation (in beta form) can be written at all.
- The relation survives for efficient portfolios alone, and for individual assets expected return becomes bounded (an interval, not a point).
- The relation survives unchanged, since the risk-free asset enters only the capital market line (never the security market line) in the derivation.
- The relation survives with the risk-free rate replaced by the expected return on a zero-beta portfolio, uncorrelated with the market (Black, 1972).
<!-- YW5zOjM= -->
> This is Black's zero-beta CAPM: $E[R_i]=E[R_z]+\beta_i(E[R_{mkt}]-E[R_z])$, with $R_z$ the minimum-variance portfolio uncorrelated with the market. The efficient frontier exists without a risk-free asset, so the argument goes through with $E[R_z]$ in the intercept.
> Ref: Ribeiro (2026), Ch. 4, §4.1 (p. 117); H&L, Ch. 4, eqs. (4.11.6)–(4.11.7) (p. 97)
> Similar: Ribeiro, Problem 4.5 (p. 147); H&L, Exercise 4.1 (p. 114)

Q: Roll (1977) argues that the CAPM is not testable as usually attempted. What precisely is the claim?
- That the market portfolio is unobservable, so a test run on a proxy is really a test of whether that proxy is mean-variance efficient, not of the theory.
- That expected returns are unobservable, so any test substitutes realized averages whose sampling error swamps the cross-sectional signal being sought.
- That betas must be estimated rather than observed, so errors in variables bias the slope of the estimated cross-sectional relation towards zero.
- That the model describes a single period, so a test using a multi-period sample imposes stationarity assumptions that the theory itself never makes.
<!-- YW5zOjA= -->
> The true market portfolio includes human capital, real estate and unlisted assets. Because the security market line holds by construction against *any* mean-variance efficient portfolio, substituting a proxy turns the exercise into a test of that proxy's efficiency. The other three are genuine econometric problems, but none is Roll's.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); BKM 13e, §9.3 (p. 304)
> Similar: Ribeiro, True/False 1–30 (pp. 148–149); Cochrane (2005), §9.3 (p. 167)

P: Throughout this quiz the net risk-free rate is 3% and the market portfolio has expected gross return 1,09 with standard deviation 0,20. Asset A has beta 1,5 and total return standard deviation 0,35; asset B has beta 0,5.

Q: What is the market's Sharpe ratio here, and what does equilibrium say about it?
- 0,45, and it is the highest attainable in this economy, because in equilibrium the market coincides with the tangency portfolio.
- 0,30, and it is the highest attainable in this economy, because in equilibrium the market coincides with the tangency portfolio.
- 0,06, and it bounds the ratio of any individual asset, because no single asset can be more efficient than the whole market.
- 0,30, and it is a lower bound for any efficient portfolio, because leverage raises the Sharpe ratio along the capital market line.
<!-- YW5zOjE= -->
> $(1{,}09-1{,}03)/0{,}20=0{,}30$. In equilibrium the market *is* the tangency portfolio, so no portfolio achieves a higher ratio. Leverage slides you along the capital market line without changing the Sharpe ratio, which is precisely why it is the right yardstick.
> Ref: Ribeiro (2026), Ch. 4, §4.1 (p. 117); Ch. 3, §3.4 (p. 88)
> Similar: Ribeiro, Problem 4.5 (p. 147); BKM, Ch. 9 Problem Sets (p. 309)

Q: Investors disagree about expected returns while agreeing on the covariance matrix. What breaks?
- Nothing breaks, since disagreement about means washes out across investors and the aggregate remains the tangency portfolio of average beliefs.
- Each investor holds a different risky portfolio, so the market is a wealth-weighted blend of them and need not be efficient for anybody at all.
- Two-fund separation breaks, since separation needs agreement about means while the covariance matrix governs only the shape of the frontier.
- Every investor still holds the tangency portfolio, but the risk-free rate is no longer pinned down and the security market line gains a free intercept.
<!-- YW5zOjE= -->
> Two-fund separation still holds investor by investor — each holds cash plus their own tangency portfolio — but those portfolios now differ. The market is their wealth-weighted blend, and a blend of efficient portfolios is not generally efficient. Homogeneous expectations are exactly what collapse them onto one.
> Ref: Ribeiro (2026), Ch. 4, §4.1 (p. 117); D&D 3e, Ch. 8
> Similar: Ribeiro, Problem 4.5 (p. 147); H&L, Ch. 4 §4.10–4.19 (pp. 92–105)

## sml

Q: A colleague plots total risk on the horizontal axis and asserts that every asset must lie on the resulting line. What is wrong?
- That is the security market line, valid for every asset, but its horizontal axis has to be measured in variance rather than in standard deviation.
- Nothing is wrong for individual assets, though the relation fails for portfolios, whose total risk falls below the weighted average of the parts.
- That is the capital market line, valid only for efficient portfolios; the relation holding for every asset uses beta, not total standard deviation.
- That is the capital market line, valid for every asset in equilibrium, but only where the risk-free asset can be shorted without any limit.
<!-- YW5zOjI= -->
> The capital market line covers efficient portfolios and prices total risk $\sigma$; the security market line covers *every* asset and portfolio and prices only $\beta$. An inefficient asset sits strictly below the capital market line while lying exactly on the security market line. Conflating the two is this chapter's classic error.
> Ref: Ribeiro (2026), Ch. 4, §4.2 (p. 120); BKM 13e, §9.1 (p. 283)
> Similar: Ribeiro, Problem 4.1 (p. 146); True/False 1–30 (pp. 148–149)

Q: In the economy above, what expected gross returns does the CAPM assign to assets A and B?
- 1,105 for A and 1,045 for B, applying the premium to each beta after averaging that beta with one.
- 1,150 for A and 1,050 for B, applying the premium of 10 points implied by the market Sharpe ratio.
- 1,120 for A and 1,060 for B, applying the market premium of 6 points to each of the two betas.
- 1,090 for A and 1,030 for B, since beta rescales the market gross return rather than the risk premium.
<!-- YW5zOjI= -->
> $E[R_i]=R_f+\beta_i(E[R_{mkt}]-R_f)$ with premium $0{,}06$: A gives $1{,}03+1{,}5(0{,}06)=1{,}12$, B gives $1{,}03+0{,}5(0{,}06)=1{,}06$. Beta multiplies the *premium* — never the gross return, and never the volatility.
> Ref: Ribeiro (2026), Ch. 4, §4.2 (p. 120); BKM 13e, §9.1 (p. 283)
> Similar: Ribeiro, Problem 4.1 (p. 146); BKM, Ch. 9 Problem Sets (p. 309)

Q: Asset A has standard deviation 0,35 with beta 1,5. A second asset has the same 0,35 but beta 0,5. What does the CAPM conclude?
- The comparison is undefined, since two assets with equal total risk and different betas cannot share one factor model.
- The two earn equal expected returns, since identical total risk must command identical compensation in equilibrium.
- The second earns more than A, since equal total risk with lower beta leaves more risk to be compensated.
- The second earns 6% against A's 12%: total risk is irrelevant once systematic risk has been accounted for.
<!-- YW5zOjM= -->
> Only covariance with the market is compensated. Both carry the same total risk, but the second's is overwhelmingly idiosyncratic, hence diversifiable, hence unpriced. This is the central economic content of the security market line, and the direct descendant of $\text{cov}(m,x)$ in Chapter 1.
> Ref: Ribeiro (2026), Ch. 4, §4.2 (p. 120); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 4.3 (p. 147); BKM, §8.2 (p. 254)

Q: In what sense is the security market line an ex ante statement?
- It links expected returns to betas measured ex post, so the line can be recovered exactly once a long enough return sample exists.
- It links expected returns to betas, so a scatter of realized average returns on estimated betas need not lie on it in any finite sample.
- It links realized returns to betas, so a scatter of realized average returns on estimated betas must lie on it up to estimation error.
- It links expected returns to expected betas, so the line shifts whenever the issuers constituting the market portfolio rebalance.
<!-- YW5zOjE= -->
> The line is a statement about $E[R_i]$, which is unobservable. Realized averages estimate it noisily, and betas are estimated too. A flat realized scatter is therefore evidence rather than proof — which is exactly what leaves room for the empirical debate of §4.5.
> Ref: Ribeiro (2026), Ch. 4, §4.2 (p. 120); BKM 13e, §13.1 (p. 410)
> Similar: Ribeiro, Problem 4.6 (p. 148); True/False 1–30 (pp. 148–149)

Q: A manager holds one asset with beta 1,5 and argues she should be paid for its full 0,35 of volatility. What does the theory answer?
- The market pays for full volatility when the holder cannot short it, since otherwise the idiosyncratic part could be hedged away.
- The market pays for full volatility to undiversified holders, which is why concentrated portfolios earn a documented premium.
- The market pays only for the systematic part; the rest is diversifiable, and bearing it is a choice rather than a service.
- The market pays the geometric mean of systematic and total risk, which is the source of the wedge between the two lines.
<!-- YW5zOjI= -->
> Prices are set by investors who *can* diversify, so no premium attaches to risk that diversification removes. Choosing to stay concentrated creates no claim to compensation. It is the same logic that makes $\text{cov}(m,x)$ rather than $\sigma(x)$ the pricing object in Chapter 1.
> Ref: Ribeiro (2026), Ch. 4, §4.2 (p. 120); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 4.3 (p. 147); BKM, §8.2 (p. 254)

## linsdf

Q: Write the CAPM discount factor as $m=a+b\,R_{mkt}$. Using the economy above, what is $b$?
- $b=-0{,}300$, from $b=-\frac{E[R^e_{mkt}]}{\sigma(R_{mkt})}=-\frac{0{,}06}{0{,}20}$, the negative of the Sharpe ratio.
- $b=-1{,}500$, from $b=-\frac{E[R^e_{mkt}]}{\sigma^2(R_{mkt})}=-\frac{0{,}06}{0{,}04}$, with no discounting applied.
- $b=-1{,}456$, from $b=-\frac{1}{R_f}\frac{E[R^e_{mkt}]}{\sigma^2(R_{mkt})}=-\frac{1}{1{,}03}\cdot\frac{0{,}06}{0{,}04}$.
- $b=+1{,}456$, from $b=\frac{1}{R_f}\frac{E[R^e_{mkt}]}{\sigma^2(R_{mkt})}$, positive because the premium itself is positive.
<!-- YW5zOjI= -->
> $b=-(1/1{,}03)(0{,}06/0{,}04)=-1{,}4563$. Two traps: forgetting the $1/R_f$ factor, and dividing by $\sigma$ instead of $\sigma^2$. The sign must be negative — see the next question.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124); Cochrane (2005), §6.1 (p. 100)
> Similar: Ribeiro, Problem 4.2 (p. 147)

Q: With $b=-1{,}4563$, what is $a$, and what does $E[m]$ have to equal?
- $a=1{,}5874$ and $E[m]=0{,}9709=1/R_f$, since $a$ equals the product of $b$ and the expected market return.
- $a=2{,}5583$ and $E[m]=1{,}0300=R_f$, since the mean discount factor equals the gross risk-free rate by construction.
- $a=0{,}9709$ and $E[m]=0{,}9709=1/R_f$, since $a$ is defined as the reciprocal of the gross risk-free rate.
- $a=2{,}5583$ and $E[m]=0{,}9709=1/R_f$, since a discount factor must price the risk-free asset correctly.
<!-- YW5zOjM= -->
> $a=1/R_f-b\,E[R_{mkt}]=0{,}9709+1{,}4563(1{,}09)=2{,}5583$, and then $E[m]=a+b\,E[R_{mkt}]=0{,}9709=1/R_f$. That identity is not a coincidence: it is $R_f=1/E[m]$ from §1.6 imposed on this particular $m$.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 4.2 (p. 147)

Q: Why must $b$ be negative, and what does that say economically?
- Because $m$ has to be low exactly when the market does well, so that good states are cheap — the market standing in for good times.
- Because $m$ has to be positive in every state, and only a negative slope keeps it positive across the whole support of the market return.
- Because the risk premium is positive, and the sign of $b$ must be the opposite of the sign of the premium for the algebra to close.
- Because a negative slope is what makes the discount factor a decreasing function of consumption in the underlying representative-agent model.
<!-- YW5zOjA= -->
> A dollar delivered in a booming market is a dollar you need least, so it must be cheap: $m$ falls when $R_{mkt}$ rises. This is the same economics as the consumption SDF of Session 2, with the market return standing in for bad times. Note that no linear $m$ can be positive over an unbounded support — that is a known limitation, not the reason for the sign.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124); Ch. 2, §2.3
> Similar: Ribeiro, Problem 4.2 (p. 147); Cochrane (2005), §6.3 (p. 106)

Q: The chapter states a triple equivalence. Which statement of it is correct?
- The market is mean-variance efficient $\iff$ $m$ is positive in every state $\iff$ beta pricing holds against any factor.
- The market is mean-variance efficient $\iff$ $m$ is linear in $R_{mkt}$ $\iff$ beta pricing holds against $R_{mkt}$.
- Markets are complete $\iff$ $m$ is linear in $R_{mkt}$ $\iff$ beta pricing holds against the market return alone.
- Investors have quadratic utility $\iff$ $m$ is linear in $R_{mkt}$ $\iff$ the market portfolio is mean-variance efficient.
<!-- YW5zOjE= -->
> The three are the same fact in three languages: portfolio geometry, discount-factor algebra, and regression form. Completeness is irrelevant here — it governs uniqueness of $m$, not this equivalence. Quadratic utility is one *sufficient* route to efficiency, never a necessary one.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124); Cochrane (2005), §6.2 (p. 103)
> Similar: Ribeiro, Problem 4.2 (p. 147); H&L, Exercise 4.1 (p. 114)

Q: Compute $\sigma(m)$ for this CAPM discount factor and compare it with the Hansen–Jagannathan bound.
- $\sigma(m)=0{,}2913$, so $\sigma(m)/E[m]=0{,}30$, which exceeds the market Sharpe ratio and leaves the bound slack.
- $\sigma(m)=0{,}2913$, so $\sigma(m)/E[m]=0{,}30$, exactly the market Sharpe ratio: the bound holds with equality.
- $\sigma(m)=0{,}0400$, so $\sigma(m)/E[m]=0{,}04$, which violates the bound and shows the CAPM cannot hold here.
- $\sigma(m)=0{,}0874$, so $\sigma(m)/E[m]=0{,}09$, well below the market Sharpe ratio, which the bound permits.
<!-- YW5zOjE= -->
> $\sigma(m)=|b|\sigma(R_{mkt})=1{,}4563(0{,}20)=0{,}2913$, and $0{,}2913/0{,}9709=0{,}30$ — the market Sharpe ratio exactly. Equality is forced: the bound binds against the *highest* Sharpe ratio available, and under the CAPM that is the market's, because the market is the tangency portfolio. The §1.6 bound and the §4.1 equilibrium meet here.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problems 4.2 (p. 147), 1.6(c) (p. 38)

Q: Chapter 1 writes $E[R^i]=R_f+\beta_{i,m}\lambda_m$ against the discount factor, while Chapter 4 writes $E[R^i]=R_f+\beta_i(E[R_{mkt}]-R_f)$ against the market. How do the two relate?
- They are different models; the first requires no arbitrage while the second requires complete markets to pin the market portfolio down.
- They are different models; the first holds always while the second additionally requires investors to hold mean-variance efficient portfolios.
- They are the same identity in identical units, so $\lambda_m$ is numerically equal to the market risk premium whenever the CAPM holds.
- They are the same identity in different units; $\lambda_m<0$ while the market premium is positive, because $m$ moves opposite to $R_{mkt}$.
<!-- YW5zOjM= -->
> The Chapter 1 form is an algebraic rewriting of $p=E[mx]$ and holds for any valid $m$. Chapter 4 substitutes the specific $m=a+bR_{mkt}$. Since $b<0$, loading positively on $m$ means loading negatively on the market: $\lambda_m=-\sigma^2(m)/E[m]=-0{,}0874$ here, while the market premium is $+0{,}06$. Same content, opposite sign convention.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 4.2 (p. 147); Cochrane (2005), §6.1 (p. 100)

## alpha

Q: How is alpha defined in this chapter, before any regression is run?
- As the pricing error $\alpha_i=E[R_i]-[R_f+\beta_i(E[R_{mkt}]-R_f)]$, the gap between the expected return and what the model assigns.
- As the intercept $\hat\alpha_i$ of the time-series regression of an asset's excess return on the market's, which is what makes it estimable.
- As the difference between an asset's realized average $\bar R_i$ and the realized average return of the market over the same sample.
- As the component of $E[R_i]$ attributable to the risk that the single-index model leaves inside its residual variance term.
<!-- YW5zOjA= -->
> Alpha is a *pricing error* first and a regression intercept second. The definition is model-based and involves unobservable expectations; the regression is how we estimate it. Keeping this order straight is what makes the next question answerable.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129); BKM 13e, §8.2 (p. 254)
> Similar: Ribeiro, Problem 4.1 (p. 146)

Q: A researcher runs $R^e_{i,t}=\alpha_i+\beta_iR^e_{mkt,t}+\varepsilon_{i,t}$, obtains a good fit, and reports it as evidence for the CAPM. What is wrong?
- The regression estimates $\beta_i$ consistently but not $\alpha_i$, so no restriction on the intercept can be tested from a fit of this form.
- The regression must use gross rather than excess returns, so the reported intercept is not comparable with the $\alpha_i$ the CAPM restricts.
- The regression is valid only if the residuals $\varepsilon_i$ are uncorrelated across assets, which a single time-series fit cannot establish.
- The index model is an estimation vehicle valid with or without the CAPM; the CAPM adds the restriction $\alpha_i=0$, which fit alone cannot test.
<!-- YW5zOjM= -->
> This is the key distinction of §4.4. The index model is a *statistical decomposition* into systematic and idiosyncratic parts; it fits well under the CAPM and equally well without it. The CAPM's content is the testable restriction $\alpha_i=0$ for all $i$. A high $R^2$ speaks to the decomposition, not to the restriction.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129); BKM 13e, §8.3 (p. 261)
> Similar: Ribeiro, Problem 4.4 (p. 147)

Q: Asset A has beta 1,5 and total standard deviation 0,35, with the market at 0,20. Decompose its variance.
- Systematic 0,3000 and idiosyncratic 0,0500, with $R^2=0{,}857$, since $\beta\,\sigma_{mkt}=1{,}5(0{,}20)$ in units of standard deviation.
- Systematic 0,0600 and idiosyncratic 0,0625, with $R^2=0{,}490$, since $\beta\,\sigma_{mkt}\sigma_i=1{,}5(0{,}20)(0{,}35)$.
- Systematic 0,0900 and idiosyncratic 0,0325, with $R^2=0{,}735$, since $\beta^2\sigma^2_{mkt}=2{,}25(0{,}04)$.
- Systematic 0,1225 and idiosyncratic 0,0000, with $R^2=1{,}000$, since a single-factor model leaves no residual variance by construction.
<!-- YW5zOjI= -->
> $\text{var}(R_i)=\beta_i^2\sigma^2_{mkt}+\text{var}(\varepsilon_i)$. Systematic $=2{,}25(0{,}04)=0{,}09$; total $=0{,}35^2=0{,}1225$; residual $=0{,}0325$; $R^2=0{,}09/0{,}1225=0{,}735$. Everything is in *variance* units — mixing in standard deviations is the standard slip.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129); BKM 13e, §8.2 (p. 254)
> Similar: Ribeiro, Problem 4.3 (p. 147)

Q: Twenty-five assets each have asset A's idiosyncratic variance 0,0325, uncorrelated across assets, and beta 1,5. What is the equally weighted portfolio's residual risk?
- Residual variance 0,0325 and residual volatility 0,180, since the portfolio inherits the common residual variance of its constituents.
- Residual variance 0,0000 and residual volatility 0,000, since idiosyncratic risk vanishes completely in any portfolio of many assets.
- Residual variance 0,0065 and residual volatility 0,081, since the residual variance falls with the square root of the number of holdings.
- Residual variance 0,0013 and residual volatility 0,036, since independent residuals average down by the number of holdings.
<!-- YW5zOjM= -->
> Independent residuals give $\text{var}(\bar\varepsilon)=0{,}0325/25=0{,}0013$, i.e. volatility $0{,}036$. It is the *variance* that falls with $N$; volatility falls with $\sqrt{N}$. It shrinks fast but never reaches zero at finite $N$ — while the systematic part, $\beta^2\sigma^2_{mkt}=0{,}09$, does not shrink at all.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129); BKM 13e, §8.2 (p. 254)
> Similar: Ribeiro, Problem 4.3 (p. 147)

Q: Why does the estimation regression use excess returns on both sides?
- Because the CAPM restricts the excess return relation, so the intercept of the excess-return regression is precisely the alpha the theory sets to zero.
- Because excess returns are stationary while gross returns are not, so only the excess-return regression satisfies the assumptions behind OLS inference.
- Because subtracting the risk-free rate removes the market's own drift, leaving a beta estimate that is unbiased in samples of any finite length.
- Because gross returns are bounded below by zero, so a regression in gross returns would violate the normality that the standard errors require.
<!-- YW5zOjA= -->
> The theory says $E[R_i]-R_f=\beta_i(E[R_{mkt}]-R_f)$. Regressing excess on excess makes the fitted intercept the empirical counterpart of exactly that pricing error. Running it in gross returns yields an intercept that mixes alpha with $R_f(1-\beta_i)$ and is not the object the CAPM restricts.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129); BKM 13e, §8.3 (p. 261)
> Similar: Ribeiro, Problem 4.4 (p. 147)

Q: A single time-series regression returns $\hat\alpha=2{,}0\%$ per year with a standard error of 2,5 points. What follows?
- The CAPM is confirmed for this asset, since failing to reject the null of zero alpha is evidence in favour of the restriction.
- The CAPM is rejected for this asset, since a positive point estimate of alpha is by itself a pricing error the model forbids.
- Nothing is established: the estimate is statistically indistinguishable from zero, so it is no evidence against the CAPM at all.
- The result is uninterpretable, since alpha requires a cross-sectional rather than a time-series regression to be estimated at all.
<!-- YW5zOjI= -->
> With $t=0{,}8$ the estimate is noise. Note the asymmetry: failing to reject is not confirmation either — the standard error is wide enough to be consistent with economically large alphas. Alphas are notoriously imprecise, which is why Session 7 treats their statistics carefully.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129); Ch. 7, §7.3
> Similar: Ribeiro, Problem 4.4 (p. 147); BKM, §13.1 (p. 410)

## empir

Q: Empirically the cross-sectional relation between beta and average return looks flatter than the theoretical line. Which pattern of alphas does that produce?
- Low-beta assets show positive alphas and high-beta assets negative ones, since a flatter fitted line sits above theory at low beta and below it at high beta.
- Low-beta assets show negative alphas and high-beta assets positive ones, since a flatter fitted line sits below theory at low beta and above it at high beta.
- All assets show positive alphas, since the fitted intercept exceeds the risk-free rate and the fitted slope stays positive throughout.
- Alphas are zero on average by construction, since the cross-sectional regression forces the residuals to sum to zero across the test assets.
<!-- YW5zOjA= -->
> A flatter line with a higher intercept crosses the theoretical one near beta one. Below that crossing, realized returns exceed the CAPM prediction (positive alpha); above it, they fall short (negative alpha). This is precisely the pattern that Betting Against Beta later exploits.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); BKM 13e, §13.1 (p. 410)
> Similar: Ribeiro, Problem 4.6 (p. 148)

Q: Suppose the fitted cross-sectional relation has intercept 5,5% and passes through the market at 9%. What alphas does that imply at betas 0,5 and 1,5?
- About $+1{,}25$ points at beta 0,5 and $-1{,}25$ points at beta 1,5, since the fitted slope is 3,5 points against the theoretical 6.
- About $-1{,}25$ points at beta 0,5 and $+1{,}25$ points at beta 1,5, since the fitted line is steeper than the theoretical one.
- About $+2{,}50$ points at beta 0,5 and $-2{,}50$ points at beta 1,5, since the fitted intercept exceeds the risk-free rate by 2,5.
- About zero at both, since a line passing through the market portfolio reproduces the CAPM prediction at every value of beta.
<!-- YW5zOjA= -->
> Fitted slope $=0{,}09-0{,}055=0{,}035$. At $\beta=0{,}5$: fitted $7{,}25\%$ against CAPM $6\%$, so $\alpha=+1{,}25$. At $\beta=1{,}5$: fitted $10{,}75\%$ against CAPM $12\%$, so $\alpha=-1{,}25$. The two lines cross at $\beta=1$, where both give $9\%$.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); BKM 13e, §13.1 (p. 410)
> Similar: Ribeiro, Problem 4.6 (p. 148)

Q: A fitted intercept of 5,5% against a risk-free rate of 3% has a specific theoretical reading. Which?
- It is what the zero-beta CAPM predicts when borrowing is restricted, so $E[R_z]$ exceeds $R_f$ and the line flattens accordingly.
- It is a symptom of errors in variables, since noisy betas raise the fitted intercept while leaving the fitted slope unaffected.
- It is evidence of a second priced factor, since only an omitted factor can raise the intercept above the observed risk-free rate.
- It is a sign that the sample period contained an equity bear market, since a low realized market return lifts the fitted intercept.
<!-- YW5zOjI= -->
> Black's zero-beta model replaces $R_f$ with $E[R_z]$, and investors who cannot borrow freely bid up low-beta assets instead, pushing $E[R_z]$ above $R_f$ and flattening the line. Errors in variables *also* flattens the slope, so both stories are live — but only the zero-beta reading is a theoretical prediction rather than an econometric artefact.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); H&L, Ch. 4 (p. 97)
> Similar: Ribeiro, Problem 4.6 (p. 148); Ch. 7 (Frazzini–Pedersen)

Q: Fama and French (1992) report that beta has little cross-sectional explanatory power once size and book-to-market are included. What does that establish?
- That beta is irrelevant to risk, so the systematic and idiosyncratic decomposition of the index model has no economic content whatsoever.
- That beta is not a sufficient description of expected returns in the data, which motivates multifactor models rather than settling the CAPM's truth.
- That the CAPM is false as a matter of logic, since a single counterexample in the cross-section refutes a theory stated in terms of expectations.
- That size and book-to-market are themselves the true state variables, since any characteristic surviving a horse race must proxy for a risk factor.
<!-- YW5zOjE= -->
> The finding is about *sufficiency*: one factor does not span the cross-section. It neither refutes the theory logically (Roll's critique still bites) nor certifies size and value as risk factors — that argument is Session 6's, and remains contested.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); Ch. 6, §6.2
> Similar: Ribeiro, Problem 4.6 (p. 148); BKM, §13.1 (p. 410)

Q: Why is any empirical rejection of the CAPM described as a joint-hypothesis problem?
- Because a test bundles the pricing model with the assumption of a constant beta, so rejection may reflect time variation rather than a mistaken model.
- Because a test bundles the pricing model with the assumption of normally distributed returns, so rejection may reflect fat tails rather than mispricing.
- Because a test bundles the pricing model with the estimator's asymptotics, so rejection may reflect small-sample bias rather than a failure of the theory.
- Because a test bundles the pricing model with an assumption about the market proxy and about expectations, so rejection cannot name the culprit.
<!-- YW5zOjM= -->
> Roll supplies half of it (which proxy?) and Fama the other half (are expectations rational?). A rejection tells you the *bundle* fails without saying which component did. The other three are genuine complications, but each is a specific auxiliary assumption rather than the joint-hypothesis problem itself.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); Ch. 9, §9.1
> Similar: Ribeiro, True/False 1–30 (pp. 148–149); Cochrane (2005), §9.3 (p. 167)

## uses

P:

Q: A firm evaluates a project whose cash flows have beta 1,5 while the firm's own equity beta is 0,5. Which discount rate is right, and why?
- 12%, the project's own beta, since the discount rate must reflect the risk of the cash flows, not of the firm doing the discounting.
- 6%, the firm's equity beta, since the project is financed from the firm's balance sheet and inherits the firm's cost of capital in equilibrium.
- 9%, the market return, since a project with beta above the firm's should be evaluated at the average of the two relevant discount rates.
- 3%, the risk-free rate, since project-specific risk is diversifiable across the firm's portfolio of projects and therefore not priced.
<!-- YW5zOjA= -->
> Discount rates attach to *cash flows*, not to firms: $1{,}03+1{,}5(0{,}06)=1{,}12$. Using the company-wide rate makes risky projects look artificially attractive and safe ones artificially poor — the single most consequential abuse in §4.6.
> Ref: Ribeiro (2026), Ch. 4, §4.6 (p. 141); BKM 13e, §9.4 (p. 305)
> Similar: Ribeiro, Problem 4.7 (p. 148)

Q: A fund reports Jensen's alpha of 1,5 points per year against the market. What does this legitimately establish, and what does it not?
- It measures the manager's skill directly, though it cannot distinguish luck from skill without a longer sample than is normally available.
- It measures average return beyond CAPM-implied compensation, but it neither establishes skill nor rules out exposure to factors outside the model.
- It measures exposure to omitted factors, since under the CAPM a nonzero alpha can only arise from a risk source the model has left out.
- It measures nothing at all, since Jensen's alpha is defined for individual assets and has no interpretation when applied to managed portfolios.
<!-- YW5zOjE= -->
> Alpha is a pricing error relative to *one* benchmark. Positive alpha against the CAPM may be skill, or it may be loading on size, value or momentum that this benchmark cannot see — which is exactly why Session 7 escalates to multifactor attribution before drawing conclusions about managers.
> Ref: Ribeiro (2026), Ch. 4, §4.6 (p. 141); Ch. 7, §7.2
> Similar: Ribeiro, Problem 4.7 (p. 148); BKM, §9.4 (p. 305)

Q: Which use of the CAPM does the chapter treat as legitimate despite the empirical failures of §4.5?
- As a disciplined benchmark that forces an explicit statement of what compensated risk is, against which any claimed abnormal return must be argued.
- As a precise forecasting tool for expected returns, provided betas are estimated over a sufficiently long window to control estimation error.
- As a complete description of the cross-section, provided the market proxy is broadened to include human capital and unlisted assets.
- As a valuation method that requires no judgement, since every input is observable and the resulting discount rate is model-free.
<!-- YW5zOjA= -->
> The chapter's position is that the CAPM's enduring value is conceptual discipline: it separates compensated from uncompensated risk and makes any claim of outperformance state its benchmark. It does not deliver precise expected-return forecasts, and §4.5 is candid that the cross-section does not obey it.
> Ref: Ribeiro (2026), Ch. 4, §4.6 (p. 141); Common pitfalls (p. 145)
> Similar: Ribeiro, Problem 4.7 (p. 148); True/False 1–30 (pp. 148–149)
