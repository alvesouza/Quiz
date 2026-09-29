---
quiz: "Full-Course Review — Round 5 of 5"
tags:
  s01: "S01 · Return Algebra and the Historical Record"
  s02: "S02 · The Puzzles and the SDF Repairs"
  s03: "S03 · Estimation Error in the Frontier"
  s04: "S04 · Beta as a Hedge Ratio; Uses and Abuses of the CAPM"
  s05: "S05 · What a Risk Model Pays and Does Not Claim"
  s06: "S06 · The Factor Zoo and Multiple Testing"
  s07: "S07 · Betting Against Beta and Buffett's Alpha"
  s08: "S08 · Parity, Bounds and Risk-Neutral Valuation"
  s09: "S09 · Disciplined Backtesting and the Map of m"
  q10: "Q10 · One Equation, Five Models"
---

## s01

Q: Annual log returns $r_t=\ln R_t$ on a stock index are i.i.d. $N(\mu,\sigma^2)$, where $R_t$ is the gross simple return. Let $\bar a=E[R_t]-1$ be the population arithmetic mean of simple returns, $g$ the long-run geometric mean (the constant rate that compounds to terminal wealth), and $W_H$ the wealth after $H$ years from one unit invested. Which triple $\big(\ln(1+\bar a),\ \ln(1+g),\ E[W_H]/\mathrm{median}(W_H)\big)$ is correct?
- $\big(\mu,\ \mu-\tfrac12\sigma^2,\ e^{H\sigma^2/2}\big)$, so the arithmetic mean is the log mean itself and compounding loses half a variance
- $\big(\mu+\tfrac12\sigma^2,\ \mu,\ e^{H^2\sigma^2/2}\big)$, so the gap between mean and median wealth grows with the square of the horizon
- $\big(\mu+\tfrac12\sigma^2,\ \mu,\ e^{H\sigma^2/2}\big)$, so the mean-to-median wealth ratio widens exponentially and linearly in $H$
- $\big(\mu+\tfrac12\sigma^2,\ \mu-\tfrac12\sigma^2,\ e^{H\sigma^2}\big)$, so the geometric mean sits a full variance below the arithmetic one
<!-- YW5zOjI= -->
> Lognormality does all the work. $E[R]=E[e^{r}]=e^{\mu+\sigma^2/2}$ (Jensen), so $\ln(1+\bar a)=\mu+\tfrac12\sigma^2$. Log returns add over time, $\ln W_H=\sum r_t\sim N(H\mu,H\sigma^2)$, so the geometric rate is $\ln(1+g)=\mu$ and the median of $W_H$ is $e^{H\mu}$, while $E[W_H]=e^{H\mu+H\sigma^2/2}$. The ratio is $e^{H\sigma^2/2}$: variance, not standard deviation, scales with $H$, which kills the $H^2$ option. The gap $\ln(1+\bar a)-\ln(1+g)=\tfrac12\sigma^2$ is the exact log version of the book's $g\approx\bar r-\tfrac12\sigma^2$ drag; the option placing $g$ at $\mu-\tfrac12\sigma^2$ double-counts it. The operating rule follows: compound at $g$ for terminal wealth, reserve $\bar a$ for one-period expectations. Fat tails (excess kurtosis near 7 in monthly data) are the caveat on the normality of $r_t$.
> Ref: Ribeiro (2026), Ch. 1, §1.2.1 (p. 5), §1.2.4 (pp. 8–9), §1.2.8 (p. 12)
> Similar: BKM 13e, Ch. 5 §5.4–5.5; Ribeiro, Problem 1.1

## s02

Q: Under power utility with risk aversion $\gamma$ and lognormal consumption growth with mean $g$ and volatility $\sigma_c$, the log risk-free rate is $r_f=\delta+\gamma g-\tfrac12\gamma^2\sigma_c^2$, where $\delta$ is the rate of time preference ($\beta=e^{-\delta}$). Suppose $\gamma$ is raised to the Sharpe-ratio floor $\gamma\approx SR/\sigma_c$ to match the equity premium. Which statement about the $\delta$ needed to match the observed $r_f$, and about a repair, is correct?
- $\delta=r_f-\gamma g+\tfrac12\gamma^2\sigma_c^2$; the $\gamma g$ term dominates at such $\gamma$, so $\delta<0$ and $\beta>1$; recursive utility helps by letting the EIS, not $1/\gamma$, set that term
- $\delta=r_f-\gamma g-\tfrac12\gamma^2\sigma_c^2$; both terms push $\delta$ down as $\gamma$ rises, so $\beta>1$; recursive utility helps by making measured consumption growth far more volatile
- $\delta=r_f-\gamma g+\tfrac12\gamma^2\sigma_c^2$; the precautionary term dominates at such $\gamma$, so $\delta>0$ and the only puzzle left is the premium; habit formation removes that one
- $\delta=r_f+\gamma g-\tfrac12\gamma^2\sigma_c^2$; the rate rises with $\gamma$, so the investor must be extremely impatient; rare disasters help by lowering the required rate of time preference
<!-- YW5zOjA= -->
> Solve the rate equation for $\delta$: $\delta=r_f-\gamma g+\tfrac12\gamma^2\sigma_c^2$. With $\gamma\approx24$, $g\approx2\%$ and $\sigma_c\approx1.9\%$, the intertemporal-substitution term $\gamma g\approx50\%$ swamps the precautionary term $\tfrac12\gamma^2\sigma_c^2\approx10\%$, so $\delta\approx-0.38$ and $\beta\approx1.46$: Weil's risk-free-rate puzzle. The precautionary term only wins for $\gamma>2g/\sigma_c^2$, far above the floor. Under power utility the EIS is forced to equal $1/\gamma$, so a high $\gamma$ means a huge desire to smooth consumption across time and hence a huge rate. Recursive (Epstein–Zin) utility, the engine of long-run risk, separates the two, so risk aversion can be high while the growth term stays small. Habit and disasters raise $\sigma(m)$ by other routes; the repairs are examinable by name and rationale only.
> Ref: Ribeiro (2026), Ch. 2, §2.2.5 (p. 49), §2.4.7 (p. 62), §2.6 (pp. 69–70)
> Similar: Cochrane, Asset Pricing, Ch. 21; Ribeiro, True/False bank, Ch. 2

## s03

Q: A mean–variance optimizer is run on sample moments of $N$ assets estimated from $T$ monthly observations, with $N/T$ not small. Which diagnosis-and-remedy statement is correct?
- Replacing the sample covariance matrix with a single-index factor matrix repairs the tangency portfolio out of sample, because the factor structure also disciplines the vector of expected returns.
- The global minimum-variance portfolio decays out of sample as badly as the tangency portfolio, because it inverts the same noisy covariance matrix and inherits all of its error.
- Sampling daily rather than monthly over the same calendar span cures the problem, because a finer grid shrinks the standard errors of means and covariances in the same proportion.
- Forbidding short sales usually improves out-of-sample results, because clamping the weights the optimizer wanted to short acts like shrinking the spuriously low covariances behind them.
<!-- YW5zOjM= -->
> Jagannathan and Ma's result: a no-short constraint lowers the in-sample Sharpe ratio but typically raises the out-of-sample one, because it binds exactly where a spuriously low estimated covariance invited an extreme short, and clamping that weight is equivalent to shrinking the offending covariance: regularization in disguise. Finer sampling sharpens variances and covariances but not means, whose standard error depends on the calendar span only. The minimum-variance portfolio is the survivor, since it uses only $\Sigma$, the well-estimated object. A factor matrix fixes $\Sigma$ and is silent on $\mu$, which is why Chapter 5 finds that it rescues the minimum-variance portfolio and barely helps the tangency portfolio: the handoff from Chapter 3 fixes half the problem.
> Ref: Ribeiro (2026), Ch. 3, §3.5.6 (pp. 104–105), §3.5.9 (pp. 106–107); Ch. 1, §1.2.5 (p. 9); Ch. 5, §5.5.4 (p. 177)
> Similar: Ribeiro, True/False bank, Ch. 3

## s04

Q: A stock's excess return obeys $R^e_i=\alpha_i+\beta_iR^e_m+\varepsilon_i$ with $\varepsilon_i$ uncorrelated with $R^e_m$, where $\sigma_i^2$ and $\sigma_m^2$ are the stock and market variances and $\rho$ their correlation. An investor holds one unit of the stock and shorts $h$ units of a market futures position paying $hR^e_m$. Which triple (variance-minimizing $h$, residual variance, expected excess return of the hedged position) is correct?
- $h=\beta_i$; residual variance $\sigma_i^2-\beta_i\sigma_m^2$; expected excess return $\alpha_i$
- $h=\beta_i$; residual variance $\sigma_i^2-\beta_i^2\sigma_m^2$; expected excess return $\alpha_i$
- $h=\rho\,\sigma_m/\sigma_i$; residual variance $\sigma_i^2(1-\rho^2)$; expected excess return $\alpha_i$
- $h=\beta_i$; residual variance $\sigma_i^2(1-\rho^2)$; expected excess return $E[R^e_i]$
<!-- YW5zOjE= -->
> $\mathrm{Var}(R^e_i-hR^e_m)=\sigma_i^2-2h\beta_i\sigma_m^2+h^2\sigma_m^2$ is minimized at $h=\beta_i=\mathrm{cov}(R_i,R_m)/\sigma_m^2$: the OLS slope is the minimum-variance hedge ratio. The minimum is $\sigma_i^2-\beta_i^2\sigma_m^2=\sigma_i^2(1-\rho^2)=\sigma_\varepsilon^2$, the idiosyncratic variance. $\rho\sigma_m/\sigma_i$ is the slope of the reverse regression (market on stock), a classic slip. Shorting $\beta_i$ units of the market strips out $\beta_iE[R^e_m]$, leaving $\alpha_i$: the hedged position is pure alpha plus idiosyncratic noise, and its reward-to-risk $\alpha_i/\sigma_\varepsilon$ is the appraisal ratio of Chapter 7. The abuse follows too: a mis-estimated $\beta$ leaves residual market exposure that shows up as fake alpha.
> Ref: Ribeiro (2026), Ch. 4, §4.2.4 (pp. 122–123), §4.4.6 (p. 132), §4.6.5 (p. 145); Ch. 7, §7.2.1 (p. 232)
> Similar: BKM 13e, Ch. 8 §8.2

## s05

Q: A manager replaces the sample covariance matrix of 48 industries with an industry-factor risk model, and the out-of-sample volatility of her minimum-variance portfolio falls sharply. A colleague concludes that, since these factors explain comovement so well, tilting toward high-loading industries must raise expected return. Which reply is correct?
- The colleague is right under the APT, because any factor that explains comovement must carry a premium $\lambda$, and arbitrage ties $\lambda$ to the factor's own variance $\sigma_f^2$.
- The colleague is right only for the minimum-variance portfolio, since its lower realized $w'\Sigma w$ at an unchanged mean reveals the premium that the industry factors carry.
- A risk model restricts only $\Sigma$; pricing is a claim that $b\neq0$ in $m=a-b'f$, tested through alphas or cross-sectional slopes, on which comovement is silent.
- The colleague is wrong only because industry factors are non-traded, and a non-traded $f$ cannot carry a premium until a factor-mimicking portfolio has been built.
<!-- YW5zOjI= -->
> A covariance factor and a priced factor are different claims. The risk model restricts second moments and leaves the intercepts $\alpha_i$ free: two assets with identical loadings can have wildly different expected returns. Whether a factor is priced is a statement about the discount factor, $m=a-b'f$ with $b\neq0$, equivalently a nonzero $\lambda$ in beta pricing, and it is tested by GRS alphas or Fama–MacBeth slopes, not by how much variance the factor explains. Industry factors are the textbook case of factors that repair the diagonal of $\Sigma$ without earning a premium. The minimum-variance portfolio uses no means at all, so its improvement says nothing about $\mu$. Non-traded factors can be priced; mimicking portfolios only make the premium tradable.
> Ref: Ribeiro (2026), Ch. 5, §5.5.4 (p. 177), §5.6.1 (pp. 178–179); Ch. 6, §6.1.1 (p. 191), §6.1.4 (p. 193)
> Similar: Ribeiro, True/False bank, Ch. 5

## s06

Q: A researcher, writing after several hundred factors have been published, reports a new long–short sort with a $t$-statistic of 2.6 in its discovery sample. Which verdict agrees with the multiple-testing logic and the replication evidence?
- It clears the single-test 5% bar but not the hurdle of about $t>3$, and published premia typically shrink by about a quarter out of sample and by more than half after publication.
- It clears the $t>3$ hurdle once its $t$-statistic is annualized, and published premia typically keep their size after publication, since the capital available to arbitrage them is limited.
- It fails both bars, because the $t>3$ hurdle applies to every test including a pre-specified single one, and published premia typically shrink by about a quarter after publication.
- It clears the hurdle, because $t>3$ applies only to factors lacking a risk story, and published premia shrink by more than half out of sample but only a quarter after publication.
<!-- YW5zOjA= -->
> $t=2.6$ passes a single pre-specified test at 5% but not the Harvey–Liu–Zhu bar of roughly 3, which corrects for the number of tests the field has run, not for any one test (a genuinely pre-specified single test at $t>2$ stays valid). McLean and Pontiff find premia decay by about 26% out of sample and about 58% post-publication; the last option swaps the two. A $t$-statistic does not change with annualization when mean and standard error are scaled consistently. The same logic transfers to backtesting: the best of many specifications carries a snooping-inflated $t$, which is why the survivor list (market, value weakened, momentum, profitability and investment, size weakest) is short.
> Ref: Ribeiro (2026), Ch. 6, §6.7.1 (pp. 213–214), §6.7.2 (pp. 214–216), §6.8.1 (pp. 217–218)
> Similar: Harvey, Liu and Zhu (2016); Ribeiro, True/False bank, Ch. 6

## s07

Q: The empirical security market line is $E[R^e_i]=a+s\,\beta_i$ with intercept $a>0$, and it passes through the market, so $a+s=\lambda$, where $\lambda$ is the market premium. An investor levers a low-beta portfolio (beta $\beta_L<1$) to beta one by holding $1/\beta_L$ units of it, financing the extra $1/\beta_L-1$ at a cost $c>0$ below the risk-free rate, as insurance float allows. What is the CAPM alpha of the levered position?
- $a\,(1-\beta_L)/\beta_L+c$
- $(a+c)\,(1-\beta_L)$
- $a/\beta_L+c\,(1-\beta_L)/\beta_L$
- $(a+c)\,(1-\beta_L)/\beta_L$
<!-- YW5zOjM= -->
> The levered excess return is $\tfrac{1}{\beta_L}R^e_L+\big(\tfrac{1}{\beta_L}-1\big)c$, with beta one. Its mean is $\tfrac{a}{\beta_L}+s+\big(\tfrac{1}{\beta_L}-1\big)c$, and subtracting $\lambda=a+s$ gives $a\big(\tfrac{1}{\beta_L}-1\big)+c\big(\tfrac{1}{\beta_L}-1\big)=(a+c)(1-\beta_L)/\beta_L$. The option $a/\beta_L+\dots$ forgets to subtract the slope's share of the premium; $(a+c)(1-\beta_L)$ forgets the leverage scaling. Two lessons at once: the flat line (positive $a$) is what the BAB leg harvests, and it is larger the lower $\beta_L$; cheap, permanent financing ($c>0$) adds to it. That is the Frazzini–Kabiller–Pedersen reading of Berkshire: leverage of about 1.6 financed by float below the bill rate, applied to cheap, safe, quality (value, BAB, QMJ) stocks, with a modest residual alpha.
> Ref: Ribeiro (2026), Ch. 7, §7.5.1–7.5.2 (pp. 246–247), eq. (7.16), §7.6.2 (pp. 252–253); Ch. 4, §4.5.2 (p. 137)
> Similar: Ribeiro, Example 7.6; Frazzini and Pedersen (2014)

## s08

Q: A European call and put on a non-dividend-paying stock share strike $K$ and maturity $T$; the stock price is $S$, the gross risk-free return to $T$ is $R_f$, and every price obeys $p=E[m\,x]$ for a strictly positive discount factor $m$. Using $\max(S_T-K,0)-\max(K-S_T,0)=S_T-K$, which statement is correct?
- $C-P=S-K/R_f$, so $C\ge S-K/R_f>S-K$, and early exercise of an American put on this stock is never optimal.
- $C-P=S-K/R_f$, so $C\ge S-K/R_f>S-K$, and early exercise of an American call on this stock is never optimal.
- $C-P=(E[S_T]-K)/R_f$, so the parity gap rises with the expected return, and an American call is worth more than a European one.
- $C-P=S-K\,R_f$, so $C\ge S-K\,R_f$, and the call bound is looser than intrinsic value, which makes early exercise of a call optimal.
<!-- YW5zOjE= -->
> Linearity of $p=E[mx]$ prices the payoff identity: $C-P=E[mS_T]-K\,E[m]=S-K/R_f$, with no probabilities or expected returns entering; physical $E[S_T]$ never appears. Since $P\ge0$ (positive $m$, nonnegative payoff), $C\ge S-K/R_f$, and $K/R_f<K$ when $R_f>1$, so the European call is worth strictly more than the exercise value $S-K$. An American call on a non-dividend stock is therefore never exercised early and is worth the same as the European one. The put has no such bound: deep in the money, collecting $K$ now can beat waiting, so early exercise of an American put can be optimal.
> Ref: Ribeiro (2026), Ch. 1, §1.3.2 (p. 14); Ch. 8, §8.7.3 (p. 284), §8.7.4–8.7.5 (p. 285)
> Similar: BKM 13e, Ch. 20 §20.4; Ribeiro, True/False bank, Ch. 8

## s09

Q: A long–short strategy is backtested on point-in-time data (historical index membership, unrestated accounting figures), net of stated costs and turnover, and its alpha against a four-factor benchmark has $t>3$ in development and stays positive on data untouched during development. Which conclusion, stated as a claim about the discount factor $m$, is warranted?
- Either the four-factor $m$ omits a priced source of risk or prices deviate from it; the backtest by itself cannot tell those two apart.
- The market is inefficient, since point-in-time data and an untouched test sample together rule out any missing-factor explanation.
- The four-factor $m$ is confirmed, since an alpha that survives out of sample must be compensation for covariance with the four factors.
- Nothing about $m$ follows, since Sharpe's arithmetic implies that half of all strategies beat any benchmark gross purely by chance.
<!-- YW5zOjA= -->
> The disciplines listed (point-in-time data against look-ahead and survivorship, net-of-cost reporting, the $t>3$ bar, an untouched test sample against data snooping) make the alpha credible; they cannot make it interpretable. A nonzero alpha means $E[m\,R^e]\neq0$ for the four-factor $m$: either $m$ is missing a priced factor or prices are off relative to it. That is the joint-hypothesis problem, and the capstone map reads every model as a claim about $m$ precisely so that a surviving alpha becomes a candidate row for the fourth column of open problems. An alpha is by definition the part not explained by the factors, so it cannot confirm them. Sharpe's arithmetic concerns gross dollar-weighted averages, not an out-of-sample, net, $t>3$ alpha.
> Ref: Ribeiro (2026), Ch. 9, §9.1.3 (p. 303), §9.4.4 (p. 321), §9.4.5 (p. 322), §9.5 (pp. 323–325)
> Similar: Ribeiro, Example 9.3; Ribeiro, True/False bank, Ch. 9

## q10

Q: Every model in the course specializes $p_t=E_t[m_{t+1}x_{t+1}]$. Let $c_t$ be consumption, $\beta$ and $\gamma$ time preference and risk aversion, $R_m$ the market return, $P^{(n)}_t$ the price of a zero-coupon bond paying one in $n$ periods, $q(s)$ and $\pi(s)$ the state price and probability of state $s$, and $R_f$ the gross risk-free return. Which set of specializations is entirely correct?
- $m=\beta(c_{t+1}/c_t)^{-\gamma}$; CAPM $m=a+bR_m$ with $b>0$; $P^{(n)}_t=E_t[m_{t+1}P^{(n-1)}_{t+1}]$; a call is $E^*[\max(S_T-K,0)]/R_f$ with $\pi^*(s)=R_f\,q(s)$
- $m=\beta(c_{t+1}/c_t)^{-\gamma}$; CAPM $m=a-bR_m$ with $b>0$; $P^{(n)}_t=E_t[m_{t+1}P^{(n)}_{t+1}]$; a call is $E^*[\max(S_T-K,0)]/R_f$ with $\pi^*(s)=R_f\,q(s)$
- $m=\beta(c_{t+1}/c_t)^{-\gamma}$; CAPM $m=a-bR_m$ with $b>0$; $P^{(n)}_t=E_t[m_{t+1}P^{(n-1)}_{t+1}]$; a call is $E^*[\max(S_T-K,0)]/R_f$ with $\pi^*(s)=q(s)/R_f$
- $m=\beta(c_{t+1}/c_t)^{-\gamma}$; CAPM $m=a-bR_m$ with $b>0$; $P^{(n)}_t=E_t[m_{t+1}P^{(n-1)}_{t+1}]$; a call is $E^*[\max(S_T-K,0)]/R_f$ with $\pi^*(s)=R_f\,q(s)$
<!-- YW5zOjM= -->
> Each wrong set breaks exactly one link. The CAPM discount factor must fall when the market rises, $m=a-bR_m$ with $b>0$, so that high-beta assets, which pay in the states where $m$ is low, earn a premium; $+b$ would make them hedges. The bond recursion rolls maturity down: next period the $n$-period bond is an $(n-1)$-period bond, so $P^{(n)}_t=E_t[m_{t+1}P^{(n-1)}_{t+1}]$ with $P^{(0)}=1$. Risk-neutral probabilities are state prices scaled up by $R_f$, $\pi^*(s)=R_fq(s)=R_f\pi(s)m(s)$, which is what makes them sum to one since $\sum_s q(s)=1/R_f$. The consumption row is common to all four: marginal rate of substitution under power utility. One pricing equation, four choices of $m$; the multifactor row, $m=a-b'f$, is the CAPM row with more factors.
> Ref: Ribeiro (2026), Ch. 9, §9.5, Table 9.1 (pp. 323–325); Ch. 2, §2.2.1 (p. 47); Ch. 4, §4.3.1 (p. 126); Ch. 8, §8.5.1 (p. 276), §8.9.1 (p. 289)
> Similar: Cochrane, Asset Pricing, Ch. 1; Ribeiro, True/False bank, Ch. 9
