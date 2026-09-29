---
quiz: "Full-Course Review — Round 4 of 5"
tags:
  s01: "S01 · Risk-Neutral Probabilities"
  s02: "S02 · The Hansen–Jagannathan Bound"
  s03: "S03 · Frontier–SDF Duality"
  s04: "S04 · Estimating Betas and the Flat SML"
  s05: "S05 · Multifactor Covariance and Factor Choice"
  s06: "S06 · Fama–MacBeth Two-Pass Regressions"
  s07: "S07 · The Attribution Ladder"
  s08: "S08 · Short-Rate Models and Forwards"
  s09: "S09 · The Present-Value Identity and Discount-Rate News"
  pd: "Primer D · Equity Valuation"
---

## s01

Q: A one-period economy has states $s$ with physical probabilities $\pi(s)>0$ and state prices $q(s)>0$; the discount factor is $m(s)=q(s)/\pi(s)$, the gross riskless rate is $R_f=1/\sum_s q(s)$, and the risk-neutral probabilities are $\tilde\pi(s)=q(s)/\sum_{s'}q(s')$. A stock paying no dividend costs $S_0$ today and is worth $S_T$ next period, and $F_0$ is the forward price for delivery next period, set so that the contract costs nothing to enter. Which expression gives the gap $E[S_T]-F_0$ between the physical expectation and the forward price?
- $R_f\,\mathrm{cov}(m,S_T)$, which is negative for a stock that pays off well when $m$ is low, so the forward price overstates the expected future price
- $-\mathrm{cov}(m,S_T)/R_f$, which is positive for a stock that pays off well when $m$ is low, so the forward price understates the expected future price
- $-R_f\,\mathrm{cov}(m,S_T)$, which is positive for a stock that pays off well when $m$ is low, so the forward price understates the expected future price
- $0$, since no arbitrage forces $F_0=E[S_T]$ and any gap would be a riskless cash-and-carry profit, so the forward price is an unbiased forecast of it
<!-- YW5zOjI= -->
> A zero-cost forward means $0=E[m(S_T-F_0)]$, so $F_0=E[mS_T]/E[m]=R_f S_0=\tilde E[S_T]$: the forward price is the **risk-neutral** expectation, which is also the cost-of-carry price $S_0e^{rT}$ with no dividend yield. Now expand the stock's own price, $S_0=E[m]E[S_T]+\mathrm{cov}(m,S_T)=E[S_T]/R_f+\mathrm{cov}(m,S_T)$, so $E[S_T]=R_fS_0-R_f\,\mathrm{cov}(m,S_T)=F_0-R_f\,\mathrm{cov}(m,S_T)$. A stock that pays in good times has $\mathrm{cov}(m,S_T)<0$, so it is expected to finish above its forward price, and the gap is the risk premium. The first option has the sign flipped; the second divides by $R_f$ where it should multiply; the last confuses $\tilde\pi$ with $\pi$ — no arbitrage makes $\tilde\pi$ a probability distribution, not a forecast.
> Ref: Ribeiro (2026), Ch. 1, §1.7 (pp. 29–31); Ch. 8, §8.6.2 (pp. 280–282)
> Similar: Cochrane (2005), Ch. 1, §1.4; BKM 13e, Ch. 22

## s02

Q: Let $R_f$ be the gross riskless rate and $R_{mkt}$ the gross market return, with mean excess return $E[R^e_{mkt}]>0$ and volatility $\sigma(R_{mkt})$. Consider the linear discount factor $m=a+b\,R_{mkt}$ with $b=-\frac{1}{R_f}\frac{E[R^e_{mkt}]}{\sigma^2(R_{mkt})}$ and $a$ chosen so that $E[m]=1/R_f$. What is its coefficient of variation $\sigma(m)/E[m]$, and where does it sit relative to the Hansen–Jagannathan bound built from the market alone?
- $E[R^e_{mkt}]/\sigma(R_{mkt})$: it equals the market Sharpe ratio, so it sits exactly on the single-asset bound, with equality
- $E[R^e_{mkt}]/\big(R_f\,\sigma(R_{mkt})\big)$: it falls short of the market Sharpe ratio, so it violates the bound by a factor of $1/R_f$
- $E[R^e_{mkt}]/\sigma^2(R_{mkt})$: it equals the market's reward per unit of variance, so it clears the bound whenever $\sigma(R_{mkt})<1$
- $R_f\,E[R^e_{mkt}]/\sigma(R_{mkt})$: it exceeds the market Sharpe ratio, so it clears the bound strictly and leaves room to spare
<!-- YW5zOjA= -->
> $\sigma(m)=|b|\,\sigma(R_{mkt})=E[R^e_{mkt}]/\big(R_f\,\sigma(R_{mkt})\big)$, and dividing by $E[m]=1/R_f$ cancels the $R_f$: $\sigma(m)/E[m]=E[R^e_{mkt}]/\sigma(R_{mkt})$. Because this $m$ is perfectly (negatively) correlated with $R_{mkt}$, the correlation inequality behind the bound binds, so the CAPM discount factor lands **on** the ray $\sigma(m)=S\,E[m]$ by construction. That is the contrast the course draws with power utility, whose $\sigma(m)/E[m]\approx\gamma\sigma_c$ is an order of magnitude too small at plausible $\gamma$: the bound does not indict the SDF framework, only smooth consumption-based $m$. The second option forgets to divide by $E[m]$; the fourth multiplies where it should cancel.
> Ref: Ribeiro (2026), Ch. 2, §2.5 (pp. 64–68); Ch. 4, §4.3 (pp. 124–128)
> Similar: Cochrane (2005), Ch. 1, §1.4; Ribeiro, True/False bank, Ch. 2

## s03

Q: A researcher takes $N$ test assets and a broad stock-index proxy $R_p$. Over the sample, the assets' mean excess returns line up exactly as $E[R^e_i]=\beta_{i,p}\,E[R^e_p]$, where $\beta_{i,p}$ is the OLS slope of $R^e_i$ on $R^e_p$, with no intercept left over. Using the equivalence between frontier returns, linear discount factors and beta pricing, what has actually been established?
- The CAPM holds, because exact beta pricing against a broad index is equivalent to a discount factor linear in the true market return, which is the CAPM's claim
- The proxy's Sharpe ratio equals the Hansen–Jagannathan bound over every asset in the economy, traded or not, so no valid discount factor can be any smoother
- The discount factor is the proxy return itself, so $\sigma(m)/E[m]$ equals the proxy's volatility over its mean and the tangency weights are the index weights
- The proxy lies on the mean–variance frontier of those test assets, so a discount factor linear in $R_p$ prices them, a fact about the proxy, not a CAPM test
<!-- YW5zOjM= -->
> The duality runs three ways: $R_p$ is mean–variance efficient (the tangency portfolio, given $R_f$) among the test assets $\iff$ some $m=a+bR_p$ prices them $\iff$ expected returns are linear in betas on $R_p$. Exact beta pricing therefore certifies the **proxy's** efficiency relative to those $N$ assets and nothing more. The CAPM's claim is that the true market portfolio is efficient; Roll's point is that a proxy can be efficient while the market is not, or vice versa, so the result is not a CAPM test. The second option overreaches: the proxy's Sharpe ratio is the tightest bound those $N$ assets impose, and adding assets can only raise it. The third confuses "$m$ linear in $R_p$" with "$m=R_p$".
> Ref: Ribeiro (2026), Ch. 3, §3.4 (pp. 96–100); Ch. 4, §4.1.5 (p. 120), §4.3 (pp. 124–128)
> Similar: Cochrane (2005), Ch. 6; BKM 13e, Ch. 13

## s04

Q: In the classic cross-sectional test of the CAPM, the average excess returns of beta-sorted portfolios are regressed on their estimated betas $\hat\beta_i$; US data give a slope well below the market's mean excess return and a positive intercept. A student argues that the flatness is only errors in variables, from using $\hat\beta_i$ in place of the true $\beta_i$. Which reply is right?
- Errors in variables cannot explain it, since a noisy regressor biases the slope away from zero, which would steepen the fitted line rather than flatten it
- The sort makes portfolio betas precise, which keeps attenuation small, and the flat line persists with post-formation betas and out of sample
- Errors in variables cannot arise here, since OLS betas are unbiased, and an unbiased regressor leaves the second-stage slope unbiased in any sample size
- The student is right, since once the Shanken correction is applied the slope returns to the market premium and the intercept falls back to exactly zero
<!-- YW5zOjE= -->
> The student's mechanism is real in principle: a mismeasured regressor **attenuates** the slope toward zero, and the intercept rises to keep the line through the mean, which is the flat-SML shape. That is exactly why the test is run on beta-sorted portfolios: sorting spreads betas widely and diversifies away idiosyncratic noise, so post-formation betas are estimated tightly and attenuation is small. The flatness has persisted for half a century with those betas. The first option has the direction of the bias wrong. The third confuses unbiasedness with precision: an unbiased but noisy $\hat\beta$ still attenuates. The last misreads Shanken, which inflates **standard errors** (by about 1.5% for FF3) and leaves the point estimates unchanged.
> Ref: Ribeiro (2026), Ch. 4, §4.4.6–4.4.7 (pp. 132–135), §4.5 (pp. 136–138); Ch. 6, §6.6.2 (p. 210)
> Similar: BKM 13e, Ch. 13; Ribeiro, True/False bank, Ch. 4

## s05

Q: A two-factor risk model writes $R^e_i=\alpha_i+\beta_{iM}F_M+\beta_{iI}F_I+\varepsilon_i$, where $F_M$ is a market factor with variance $\sigma^2_M$, $F_I$ is an industry factor with variance $\sigma^2_I$ that carries no risk premium, $\mathrm{cov}(F_M,F_I)=\sigma_{MI}$, and the residuals $\varepsilon_i$ (volatility $\sigma_{\varepsilon_i}$) are uncorrelated with the factors and across assets. For two distinct assets $i\neq j$, what is $\mathrm{cov}(R^e_i,R^e_j)$, and what is the industry factor's role in it?
- $\beta_{iM}\beta_{jM}\sigma^2_M+\beta_{iI}\beta_{jI}\sigma^2_I+(\beta_{iM}\beta_{jI}+\beta_{iI}\beta_{jM})\sigma_{MI}$; its terms stay in, since an unpriced factor still moves assets together
- $\beta_{iM}\beta_{jM}\sigma^2_M+\beta_{iI}\beta_{jI}\sigma^2_I+2\,\beta_{iM}\beta_{jI}\,\sigma_{MI}$; its terms stay in, since the cross term is symmetric in the two assets
- $\beta_{iM}\beta_{jM}\sigma^2_M+\beta_{iI}\beta_{jI}\sigma^2_I+(\beta_{iM}\beta_{jI}+\beta_{iI}\beta_{jM})\sigma_{MI}+\sigma_{\varepsilon_i}\sigma_{\varepsilon_j}$; its terms stay in, plus residual comovement
- $\beta_{iM}\beta_{jM}\sigma^2_M+(\beta_{iM}\beta_{jI}+\beta_{iI}\beta_{jM})\sigma_{MI}$; its own variance term drops, since a factor with no premium adds no systematic risk
<!-- YW5zOjA= -->
> The covariance matrix is $\Sigma=B\Sigma_FB'+D$ with $D$ diagonal, so the off-diagonal entry is $\beta_i'\Sigma_F\beta_j$: expand the $2\times2$ quadratic form and both cross products $\beta_{iM}\beta_{jI}$ and $\beta_{iI}\beta_{jM}$ appear, each times $\sigma_{MI}$. The second option is correct only in the special case $\beta_{iM}\beta_{jI}=\beta_{iI}\beta_{jM}$. The third adds a residual term that the diagonal $D$ rules out. The fourth commits the two-jobs error: whether a factor is **priced** decides whether it belongs in an expected-return model; whether it **moves assets together** decides whether it belongs in a risk model. Industry factors carry no robust premium and are still among the most important risk factors.
> Ref: Ribeiro (2026), Ch. 5, §5.4.2 (p. 168), §5.4.4–5.4.5 (pp. 170–172)
> Similar: BKM 13e, Ch. 8; Ribeiro, True/False bank, Ch. 5

## s06

Q: In a Fama–MacBeth test with $K$ traded factors $f_t$ (mean vector $\lambda$, covariance matrix $\Sigma_F$) and $N$ test assets, the first pass estimates betas $\hat\beta_i$ by time-series OLS, and the second pass runs, in each period $t=1,\dots,T$, a cross-sectional OLS of $R^e_{it}$ on $\hat\beta_i$ with slope vector $\gamma_t$. The Shanken multiplier is $c=1+\lambda'\Sigma_F^{-1}\lambda$. Which statement is right?
- $\hat\lambda=\frac1T\sum_t\gamma_t$ estimates the factor means; $\lambda'\Sigma_F^{-1}\lambda$ is the first-pass regressions' average $R^2$, and the naive standard error is divided by $\sqrt c$
- $\hat\lambda=\frac1T\sum_t\gamma_t$ estimates the prices of risk; $\lambda'\Sigma_F^{-1}\lambda$ is the factors' squared maximum Sharpe ratio, and $\hat\lambda$ itself is scaled up by $c$
- $\hat\lambda=\frac1T\sum_t\gamma_t$ estimates the prices of risk; $\lambda'\Sigma_F^{-1}\lambda$ is the factors' squared maximum Sharpe ratio, and the naive standard error is scaled up by $\sqrt c$
- $\hat\lambda=\frac1T\sum_t\gamma_t$ estimates the prices of risk; $\lambda'\Sigma_F^{-1}\lambda$ is the factors' squared maximum Sharpe ratio, and the naive standard error is scaled up by the full $c$
<!-- YW5zOjI= -->
> The second pass estimates **prices of risk**: the average of the period-by-period cross-sectional slopes, with naive standard error $\mathrm{std}_t(\gamma_t)/\sqrt T$, which absorbs cross-sectional correlation of returns but ignores that $\hat\beta_i$ is estimated. Shanken's correction multiplies the **variance** by $c$, hence the standard error by $\sqrt c$ (not by $c$) and never the point estimate. $\lambda'\Sigma_F^{-1}\lambda$ is the squared maximum Sharpe ratio attainable from the factors, the same object that, by frontier–SDF duality, is the squared Hansen–Jagannathan lower bound on $\sigma(m)/E[m]$ implied by those factors. High-Sharpe factor sets make first-pass errors matter more; for FF3 monthly $c\approx1.03$.
> Ref: Ribeiro (2026), Ch. 6, §6.6.1–6.6.2 (pp. 209–210); Ch. 3, §3.4.1 (p. 97)
> Similar: Cochrane (2005), Ch. 12; Ribeiro, True/False bank, Ch. 6

## s07

Q: A fund's excess return is regressed by OLS first on a set of traded factors $f_t$ (the short model, intercept $\alpha_S$) and then on $f_t$ plus one more traded factor $g_t$ (the long model, intercept $\alpha_L$, loading $\gamma_g$ on $g_t$). Let $a_g$ be the intercept from regressing $g_t$ itself on $f_t$ in the same sample. What is $\alpha_S-\alpha_L$, and what does a collapse of alpha from the short to the long model identify?
- $\gamma_g\,E[g_t]$ in every case, so the collapse is the loading times the premium of $g_t$ whatever its correlation with $f_t$, and it identifies a tilt that was never skill
- $a_g$ alone, independent of the fund, so the collapse is a property of the factor set rather than of the manager, and it identifies nothing about skill in either direction
- $\gamma_g\,a_g$, so the collapse is how much the fund's realized return fell once $g_t$ was added, and it identifies negative skill that the short model had been hiding
- $\gamma_g\,a_g$, which equals $\gamma_g E[g_t]$ only when $g_t$ is uncorrelated with $f_t$, and it identifies a mechanical premium the short model mistook for skill
<!-- YW5zOjM= -->
> Omitted-variable algebra: write $g_t=a_g+\delta'f_t+v_t$. The short-model loadings are $\beta_S=\beta_L+\gamma_g\delta$, so $\alpha_S=\bar R^e-\beta_S'\bar f=\alpha_L+\gamma_g(\bar g-\delta'\bar f)=\alpha_L+\gamma_g\,a_g$. The alpha falls by the fund's loading times the **alpha of $g$ against the smaller model**; the chapter's $\gamma_g E[g_t]$ is the special case where $g_t$ is orthogonal to $f_t$ (then $a_g=E[g_t]$). A collapsing alpha moves return from "skill" to "exposure to a premium any investor could buy by rule". The fund's return did not change, so the third option's "negative skill" is a misreading; the second drops the fund's own loading.
> Ref: Ribeiro (2026), Ch. 7, §7.4.1 (pp. 242–244); Ch. 4, §4.4.6 (p. 132)
> Similar: BKM 13e, Ch. 24; Ribeiro, True/False bank, Ch. 7

## s08

Q: In the Vasicek model the short rate follows $dr=\kappa(\theta-r)\,dt+\sigma\,dW$, with physical long-run mean $\theta$, mean-reversion speed $\kappa>0$ and volatility $\sigma$, and zero-coupon bond prices are exponential-affine in $r$. A version fitted to today's yield curve shows yields rising clearly with maturity, although today's short rate equals the physical $\theta$. Which reading is consistent with the model?
- The convexity term $\sigma^2/(2\kappa^2)$ lifts long yields above $\theta$, so a rising curve is exactly what the model predicts at $r=\theta$ with no risk premium at all
- The curve is priced under the risk-neutral measure, whose long-run level exceeds the physical $\theta$ when rate risk is priced, so the slope is a term premium, not a forecast
- At $r=\theta$ the drift $\kappa(\theta-r)$ keeps pushing expected short rates upward over time, so the rising curve is a pure expectations forecast with no premium in it
- Vasicek admits negative rates, so to keep every bond price below one the fitted curve must slope upward, which makes the upward slope an artefact of the Gaussian shock
<!-- YW5zOjE= -->
> At $r=\theta$ the physical drift is zero, so the expected short-rate path is flat, and the convexity adjustment works **downward**: the long-run yield is $\theta-\sigma^2/(2\kappa^2)<\theta$. With no premium the curve would be flat with a slight downward hook. A clearly rising curve therefore needs the risk-neutral long-run level $\theta^*$ above $\theta$: the pricing measure overweights the high-rate states bondholders dislike — the same distortion as $\tilde\pi(s)=m(s)\pi(s)/E[m]$ in Session 1 — and the gap is the term premium that makes the expectations hypothesis fail. Negative rates are Vasicek's flaw, fixed by CIR's $\sqrt r$ scaling, and have nothing to do with the slope.
> Ref: Ribeiro (2026), Ch. 8, §8.5.2 (pp. 277–279), §8.5.3 (p. 279); Ch. 1, §1.7 (pp. 29–31)
> Similar: Cochrane (2005), Ch. 19; Ribeiro, True/False bank, Ch. 8

## s09

Q: Let $\delta_t=d_t-p_t$ be the log dividend–price ratio, which the Campbell–Shiller identity writes as $\delta_t\approx\text{const}+E_t\sum_{j\ge1}\rho^{j-1}(r_{t+j}-\Delta d_{t+j})$ with $\rho$ slightly below one, $r$ the log return and $\Delta d$ log dividend growth. Define $b_r$ and $b_d$ as the OLS slopes of $\sum_{j\ge1}\rho^{j-1}r_{t+j}$ and of $\sum_{j\ge1}\rho^{j-1}\Delta d_{t+j}$ on $\delta_t$. In some market a researcher estimates $b_r\approx0.2$. What must $b_d$ be, and what does that say?
- $b_d\approx0.8$: a high ratio forecasts high dividend growth, so most of the ratio's movement is cash-flow news
- $b_d\approx1.2$: a high ratio forecasts high dividend growth, so the ratio overshoots the news it carries
- $b_d\approx-0.8$: a high ratio forecasts low dividend growth, so most of the ratio's movement is cash-flow news
- $b_d\approx0$: the remaining $0.8$ is regression error, since the identity holds only up to its linearization
<!-- YW5zOjI= -->
> Regress both sides of the identity on $\delta_t$: the left side gives exactly one, so $b_r-b_d\approx1$ and $b_d\approx0.2-1=-0.8$. A high dividend–price ratio (a low price) would then forecast **low** future dividend growth, and 80% of the ratio's variance would be cash-flow news — the opposite of Cochrane's US finding, $b_r\approx1$, $b_d\approx0$, where the whole budget goes to discount rates. The first option uses $b_r+b_d=1$ and gets the sign wrong; the second uses $b_d-b_r=1$; the fourth forgets that the identity is an adding-up constraint with no error term. In the Gordon special case both expected returns and growth are constant, so $\delta_t$ could not move at all.
> Ref: Ribeiro (2026), Ch. 9, §9.3.1–9.3.2 (pp. 311–313), §9.3.4–9.3.5 (pp. 316–317)
> Similar: Cochrane (2011), "Discount Rates"; Ribeiro, True/False bank, Ch. 9

## pd

Q: A firm has next-year earnings $E_1$, plowback ratio $b$, return on reinvested equity $\mathrm{ROE}$, and required return $k=R_f+\beta\,(E[R_{mkt}]-R_f)$ from the CAPM with $E[R_{mkt}]>R_f$ and $b\,\mathrm{ROE}<k$, so its forward multiple is $P_0/E_1=(1-b)/(k-b\,\mathrm{ROE})$. What is $\partial(P_0/E_1)/\partial b$, and how does the multiple respond to a higher $\beta$?
- $(\mathrm{ROE}-k)/(k-b\,\mathrm{ROE})$; more plowback raises the multiple only if $\mathrm{ROE}>k$, and a higher $\beta$ lowers it
- $(k-\mathrm{ROE})/(k-b\,\mathrm{ROE})^2$; more plowback raises the multiple only if $\mathrm{ROE}<k$, and a higher $\beta$ lowers it
- $\mathrm{ROE}(1-b)/(k-b\,\mathrm{ROE})^2$; more plowback always raises the multiple, and a higher $\beta$ raises it as well
- $(\mathrm{ROE}-k)/(k-b\,\mathrm{ROE})^2$; more plowback raises the multiple only if $\mathrm{ROE}>k$, and a higher $\beta$ lowers it
<!-- YW5zOjM= -->
> Quotient rule: the numerator is $-(k-b\,\mathrm{ROE})+\mathrm{ROE}(1-b)=\mathrm{ROE}-k$, over $(k-b\,\mathrm{ROE})^2$. The sign is the sign of $\mathrm{ROE}-k$, the same condition that signs PVGO $=E_1b(\mathrm{ROE}-k)/[k(k-b\,\mathrm{ROE})]$: growth adds value only when reinvested capital earns more than its cost, and at $\mathrm{ROE}=k$ the multiple is $1/k$ whatever $b$ is. A higher $\beta$ raises $k$ through the CAPM, and $\partial(P_0/E_1)/\partial k=-(1-b)/(k-b\,\mathrm{ROE})^2<0$, so riskier firms trade at lower multiples. The first option drops the square; the second flips the sign; the third forgets that plowback also cuts the payout $1-b$.
> Ref: Ribeiro (2026), App. D, §D.1 (p. 388), §D.5 (pp. 394–395), §D.6 (pp. 395–396)
> Similar: BKM 13e, Ch. 18; Ribeiro, Appendix D checklist
