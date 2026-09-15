---
quiz: "Session 8 — Fixed Income and Derivatives, Part 2: The Term Premium and the SDF"
tags:
  eh: "1 · The Expectations Hypothesis, Stated Two Ways"
  test: "2 · The Regression That Rejects It"
  recursion: "3 · The Recursion and Where the Premium Lives"
  vasicek: "4 · Vasicek: A Mean-Reverting Short Rate"
  affine: "5 · The Affine Family, CIR, and the Ceiling"
---

## eh

Q: The chapter gives the expectations hypothesis in a forward form, $f_{n-1,n}=E_t[r_{t+n-1}]$, and a premium form, $E_t[R^{e,(n)}_{t+1}]=0$ for every $n$. Why does it insist these are one claim rather than two?
- Because the forward form is the one-period case of the premium form, so the premium form adds content only at maturities beyond one period, where forwards are unobservable.
- Because any expected extra return on a long bond would have to show up as a forward that systematically misforecasts, so unbiased forwards and zero expected excess returns imply each other.
- Because both are consequences of the recursion (8.13), which delivers each independently once the covariance of $m_{t+1}$ with bond prices is assumed to be constant over time.
- Because the yield curve is a deterministic function of forwards, so once forwards are unbiased, realized excess returns are identically zero in every state, not merely in expectation.
<!-- YW5zOjE= -->
> The equivalence is the content of (8.11). A predictable excess return on the $n$-period bond is precisely a wedge between the forward rate and the expected future short rate; kill one and you kill the other. Note what the wrong options get wrong: the EH is a statement about *expected* returns, never about realized ones state by state, and the recursion of §8.5 explains the equivalence rather than being needed to state it.
> Ref: Ribeiro (2026), Ch. 8, §8.4 (pp. 272–273), eq. (8.11)
> Similar: Ribeiro, Problem 8.4(a) (p. 295); True/False 23 (p. 297)

Q: Before any data, the chapter argues the expectations hypothesis is "probably wrong". Which chain is the argument, and what does it predict for the test?
- Long bonds are less liquid than short ones, so they earn an illiquidity premium; the slope should therefore forecast returns only in stressed markets, not on average.
- Forwards are computed from noisy par yields, so measurement error biases them upward; the slope should forecast returns with a coefficient $0<b<1$.
- A long bond's price swings with rates, so by the master formula it earns a premium for covarying badly with marginal utility; the slope should forecast returns positively.
- Investors are loss-averse over nominal capital losses, so the curve embeds a behavioural wedge; the slope should forecast returns, but only in samples that contain a rate spike.
<!-- YW5zOjI= -->
> The argument is Chapter 1's, applied to a new asset: duration makes long-bond prices swing with rates; rates rise in states the bondholder dislikes; so $-\mathrm{cov}_t(m_{t+1},R^e_{t+1})$ is positive and long bonds must pay a term premium. And if that premium exists *and moves*, forwards are forecasts plus a premium and the slope of the curve should predict bond excess returns — which is exactly the testable null the next regression puts to the data.
> Ref: Ribeiro (2026), Ch. 8, §8.4.1 (p. 273); §1 master formula (1.13)
> Similar: Ribeiro, Problem 8.4(a) (p. 295); True/False 21 (p. 297)

## test

Q: The Campbell–Shiller / Fama–Bliss regression (8.12) on 1976–2025 Treasury data ($T=590$) returns $b=2.30$, OLS $t=8.2$, Newey–West $t=3.1$, $R^2\approx0.10$. Which reading of those four numbers is the chapter's?
- The EH null is $b=1$, and $b=2.30$ overshoots it, so the curve forecasts more rate rises than materialize; the low $R^2$ shows most of that forecast is noise.
- The EH null is $b=0$, and a spread one point steeper forecasts about 2.3 points of extra bond return next year; the premium is real and it varies over time.
- The EH null is $b=0$, and the gap between $t=8.2$ and $t=3.1$ shows the point estimate is fragile, so the rejection depends on which standard error the reader prefers.
- The EH null is $b=0$, and $R^2\approx0.10$ means the premium explains a tenth of the curve's slope, the remaining nine tenths being the market's forecast of short rates.
<!-- YW5zOjE= -->
> Under the EH expected excess returns are constant, so the cloud should have no tilt: $b=0$. The estimate is large, positive and more than three Newey–West standard errors away, so the slope forecasts *risk premia*, not merely future short rates. The distractors misplace each number: $b=1$ is the null of the Campbell–Shiller *yield-change* regression, not this one; the rejection survives either $t$; and $R^2$ measures variation in returns explained, not a share of the slope.
> Ref: Ribeiro (2026), Ch. 8, §8.4.2 (pp. 273–274), Figure 8.2, eq. (8.12)
> Similar: Ribeiro, Problem 8.4(b) (p. 295); Key result (p. 275)

Q: Why does the chapter report the Newey–West $t$ of 3.1 rather than the OLS $t$ of 8.2, and what exactly is the defect being corrected?
- Because the term spread is persistent, so the regressor is near-unit-root; Newey–West corrects the bias in $b$ itself, which OLS estimates inconsistently under persistence.
- Because bond returns are heteroskedastic across rate regimes; Newey–West reweights the observations so that the volatile 1980s do not dominate the point estimate.
- Because the twelve-month horizon induces look-ahead bias in the regressor; Newey–West realigns the dating so that only information available at $t$ enters the spread.
- Because monthly observations of a twelve-month return overlap, so residuals are autocorrelated, the effective sample is far below 590, and the OLS standard error is too small.
<!-- YW5zOjM= -->
> Consecutive monthly observations of a next-twelve-month return share eleven months of the same realized return, so the residuals are strongly autocorrelated and the independent information is a fraction of $T=590$. OLS standard errors assume no such overlap and are therefore far too small, inflating $t$ to 8.2. Newey–West corrects the *standard error*, not the coefficient — $b=2.30$ is unchanged — and the rejection survives, which is the point worth making.
> Ref: Ribeiro (2026), Ch. 8, §8.4.2 (p. 273), Figure 8.2
> Similar: Ribeiro, Problem 8.4(c) (p. 295)

## recursion

Q: Starting from $p_t=E_t[m_{t+1}x_{t+1}]$, which observation turns bond pricing into the recursion $P^{(n)}_t=E_t[m_{t+1}P^{(n-1)}_{t+1}]$, and what does its terminal condition buy?
- That coupons are reinvested at the short rate, so the payoff of an $n$-period bond next period is its coupon plus the price of an $(n-1)$-period bond, with $P^{(0)}=1$ by convention.
- That the SDF is lognormal, so an $n$-period price is the product of one-period prices; the terminal condition $P^{(0)}=1$ then fixes the constant of integration in the product.
- That an $n$-period zero held one period becomes an $(n-1)$-period zero, so its payoff is the price of the next-shorter bond; $P^{(0)}=1$ makes the terminal payoff certain.
- That bond payoffs are deterministic, so the SDF passes through the expectation; $P^{(0)}=1$ then makes each maturity's price the product of expected discount factors.
<!-- YW5zOjI= -->
> The recursion (8.13) needs exactly one fact: aging. Next period's payoff of an $n$-period zero is the price *then* of a zero with one fewer period to run. The terminal condition says a zero at maturity is worth its face, normalized to 1, so all cash-flow uncertainty is stripped away and everything left is discounting — which is why the term structure is the cleanest place in the book to isolate $m_{t+1}$. Note that $P^{(1)}_t=E_t[m_{t+1}]=1/R_{f,t}$ falls straight out.
> Ref: Ribeiro (2026), Ch. 8, §8.5.1 (p. 276), eq. (8.13)
> Similar: Ribeiro, Problem 8.5(a) (p. 295); True/False 19 (p. 297)

Q: Expanding the recursion as $P^{(n)}_t=E_t[m_{t+1}]E_t[P^{(n-1)}_{t+1}]+\mathrm{cov}_t(m_{t+1},P^{(n-1)}_{t+1})$ is said to "contain both the EH and the reason it fails". How?
- The expectation term is the EH and the covariance term is the premium; the EH holds exactly when that covariance vanishes, and §8.4 shows it does not.
- The covariance term is the EH, since it prices the expected path of short rates; the EH fails because the expectation term is nonzero for maturities beyond one period.
- Both terms are needed for the EH, which fails only because the covariance is time-varying; a constant nonzero covariance would leave the EH intact in the return regression.
- The expectation term is the EH and the covariance is Jensen's inequality, so the EH fails for a purely mechanical reason rather than an economic one.
<!-- YW5zOjA= -->
> With zero covariance the recursion collapses to pure expected discounting and the curve is the expected path of short rates alone: the expectations hypothesis exactly. Long-bond prices do covary with $m_{t+1}$, so expected returns carry a premium and forwards are forecasts plus that premium. Note that a *constant* nonzero premium would still leave returns unforecastable by the slope; what §8.4 rejects is stronger, since the estimated $b=2.30$ says the premium moves.
> Ref: Ribeiro (2026), Ch. 8, §8.5.1 (pp. 276–277), Key result (p. 276)
> Similar: Ribeiro, Problem 8.5(b),(c) (p. 295); True/False 21 (p. 297)

Q: In Example 8.3 the short rate is 4%, moving next year to 6% or 2%. Under equal risk-neutral weights $y_2=3.98\%$; under $	ilde\pi=0.6$ on the high-rate state $y_2=4.18\%$. What generated each number?
- The 3.98% comes from a negative term premium under equal weights, and the 0.20-point rise to 4.18% is the convexity correction $\sigma^2/(2\kappa^2)$ of the Vasicek long yield.
- The 3.98% reflects a downward revision of the expected short rate, and the 0.20-point gap is compensation demanded for the higher variance of the two-state distribution.
- The 3.98% is the pure-expectations yield, exactly equal to the average expected short rate, and the 0.20-point gap is the effect of $	ilde\pi$ on the expected rate path.
- The 3.98% sits below 4% by a convexity effect, though the expected short rate is exactly 4%; and the 0.20-point gap to 4.18% is the term premium the distortion creates.
<!-- YW5zOjM= -->
> Two distinct effects, and the exam prizes keeping them apart. With $	ilde\pi=	frac12$ the expected future short rate is $	frac12(6)+	frac12(2)=4\%$, yet $y_2=3.98\%$: prices are convex in rates, so averaging prices is not averaging rates — a Jensen effect. Then overweighting the *feared* high-rate state to $	ilde\pi=0.6$ pushes $P^{(2)}_0$ from 0.9249 to 0.9213 and the yield to 4.18%: that 0.20-point gap is the term premium, produced entirely by the $m_{t+1}$-distortion, with the physical expectation untouched.
> Ref: Ribeiro (2026), Ch. 8, §8.5.1, Example 8.3 (p. 277)
> Similar: Ribeiro, Problem 8.5(b) (p. 295)

## vasicek

Q: In Vasicek the bond price is $P^{(\tau)}=A(\tau)e^{-B(\tau)r_t}$ with $B(\tau)=(1-e^{-\kappa\tau})/\kappa$, and the parameters entering it are risk-neutral. Which pair of statements is right?
- $B(\tau)$ falls toward zero at long maturities, so distant yields are pinned by the current short rate; and the risk-neutral mean $\theta^*$ exceeds $\theta$ whenever mean reversion is fast.
- $B(\tau)$ rises toward $1/\kappa$, so distant yields respond less than one-for-one to the short rate; and $\theta^*=\theta-\lambda\sigma/\kappa$, the gap $\theta^*-\theta$ being the term premium.
- $B(\tau)$ rises toward $\kappa$, so distant yields respond more than one-for-one to the short rate; and $\theta^*$ equals $\theta$ whenever the price of risk $\lambda$ is nonzero.
- $B(\tau)$ rises toward $1/\kappa$, so the long end is anchored by mean reversion; and the physical and risk-neutral parameters coincide, which is why the curve can be read as a forecast.
<!-- YW5zOjE= -->
> $B(\tau)$ is the bond's sensitivity to the short rate, a kind of duration: zero at $\tau=0$, rising toward $1/\kappa$, so a short-rate move passes through to distant yields less than one-for-one and the long end is anchored by mean reversion. And the price (8.16) is computed under $\tilde\pi$, so its long-run level is the shifted $\theta^*=\theta-\lambda\sigma/\kappa$; the gap between the two means is exactly the term premium, which is why the physical expected path of rates cannot be read straight off the curve.
> Ref: Ribeiro (2026), Ch. 8, §8.5.2 (pp. 277–278), eq. (8.16)
> Similar: Ribeiro, Problem 8.5(d) (p. 295); Common pitfalls (p. 293)

Q: With $\kappa=0.25$, $\theta=5\%$, $\sigma=1.5\%$ and $r_0=3\%$, Vasicek implies yields of 3.23, 3.42, 3.82, 4.18 and 4.59% at 1, 2, 5, 10 and 30 years, with a long-run yield of 4.82%. Which two features does the chapter ask you to explain?
- The curve rises because $r_0$ sits below $\theta$; and 4.82% lies below $\theta=5\%$ by the convexity term $\sigma^2/(2\kappa^2)$, since volatility makes long bonds more valuable.
- The curve rises because the price of risk is positive; and 4.82% lies below $\theta$ because the model is fitted under the physical measure, which omits the term premium.
- The curve rises because $\kappa$ is small enough for the current rate to persist; and 4.82% lies below $\theta$ because mean reversion truncates the far end of the maturity axis.
- The curve rises because the short rate is expected to climb toward $\theta$; and 4.82% lies below $\theta$ because the long end converges to the average of simulated paths, which is skewed.
<!-- YW5zOjA= -->
> Shape first: with $r_0=3\%$ below $\theta=5\%$ the short rate is expected to drift up, so the curve slopes upward — and above $\theta$ it would invert, with no recession forecast anywhere in the model. Level second: the infinite-maturity yield is $\theta-\sigma^2/(2\kappa^2)=4.82\%$, strictly below $\theta$, because convexity is worth money (§8.3.2): more volatile short rates make long bonds more valuable, which lowers their yields. Even the long yield is not the expected short rate.
> Ref: Ribeiro (2026), Ch. 8, §8.5.2 (pp. 278–279), Figure 8.3
> Similar: Ribeiro, Problem 8.5(d) (p. 295); True/False 25 (p. 297)

## affine

Q: Which statement about CIR, the affine family, and this course's ceiling is exactly right?
- CIR imposes $\kappa>0$ and a reflecting barrier at zero, keeping rates positive; the affine label then applies to yields rather than to log prices, as in Vasicek.
- CIR adds a second factor so that level and slope move separately, which is what keeps rates positive; its bond price is affine and derived in the body by matching coefficients.
- CIR replaces the Gaussian shock with a jump process and therefore leaves the affine class, which is the price paid for positive rates and the reason Vasicek is taught instead.
- CIR scales the shock by $\sqrt{r}$ so the rate stays positive, and it remains affine; the Riccati derivation of the affine form is a PhD Hint, named here and never examined.
<!-- YW5zOjM= -->
> Vasicek's level-independent shock lets $r$ wander negative; CIR (1985) scales the diffusion by $\sqrt{r}$, so near zero the shock vanishes and the positive drift dominates. Crucially it stays *affine* — log prices linear in the state — so the exponential bond price and the tractability survive, with $A$ and $B$ solving slightly different equations. The forcing of that form through a Riccati ODE, and the general Duffie–Kan class, are held at the ceiling with the stochastic calculus: named, not operated, and never examinable.
> Ref: Ribeiro (2026), Ch. 8, §8.5.3 (p. 279), PhD Hint (pp. 279–280); CLAUDE.md §1 (methods ceiling)
> Similar: Ribeiro, True/False 25 (p. 297)
