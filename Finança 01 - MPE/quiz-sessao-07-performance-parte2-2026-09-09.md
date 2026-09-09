---
quiz: "Session 7 — Performance, Part 2: The Statistics of Alpha and the Attribution Ladder"
tags:
  sealpha: "1 · The Standard Error of an Alpha and Its t-Statistic"
  detect: "2 · Years to Detect Skill"
  lies: "3 · When the Sharpe Ratio Lies"
  bias: "4 · Survivorship, Backfill, and Selection"
  ladder: "5 · The Attribution Ladder"
  style: "6 · Style Analysis and Holdings-Based Attribution"
---

## sealpha

Q: A fund's excess return is regressed on $K$ traded factors over $T$ periods, giving intercept $\hat\alpha$ and residual volatility $\sigma(\varepsilon)$. Which expression is the chapter's $t$-statistic for the null of no skill, and what does it say drives detectability?
- $t_{\hat\alpha}\approx \hat\alpha\sqrt{T}/\sigma_P$, where $\sigma_P$ is the fund's total volatility, so a fund with low total risk is easier to certify as skilled.
- $t_{\hat\alpha}\approx \left(\hat\alpha/\sigma(\varepsilon)\right)\sqrt{T}=\mathrm{IR}\sqrt{T}$, so detectability is driven by alpha per unit of residual risk and by the record's length.
- $t_{\hat\alpha}\approx \hat\alpha\,T/\sigma(\varepsilon)$, so detectability rises linearly in the sample length and a long enough record certifies even a very small information ratio.
- $t_{\hat\alpha}\approx \left(\hat\alpha/\sigma(\varepsilon)\right)\sqrt{K}$, so detectability is governed by how rich the benchmark is rather than by the length of the record.
<!-- YW5zOjE= -->
> With $\mathrm{se}(\hat\alpha)\approx\sigma(\varepsilon)/\sqrt{T}$ (dropping the small factor-Sharpe correction $\bar\mu_f'\hat\Sigma^{-1}\bar\mu_f$), the $t$-statistic is the information ratio times $\sqrt{T}$. The consequence the chapter stresses: significance depends on the IR, not the raw alpha, so a 5% alpha bought with 20% tracking error ($\mathrm{IR}=0{,}25$) is harder to distinguish from luck than a 1% alpha bought with 2% ($\mathrm{IR}=0{,}5$). And precision buys at a punishing rate — quadruple the data to halve the standard error.
> Ref: Ribeiro (2026), Ch. 7, §7.3.1 (p. 238), eqs. (7.8)–(7.9)
> Similar: Ribeiro, Problem 7.4(a) (p. 259)

Q: A manager quotes a monthly alpha $\hat\alpha_m$ with standard error $\mathrm{se}(\hat\alpha_m)$ and wants to report annual figures. Which scaling is correct, and what happens to the $t$-statistic?
- Scale both the alpha and its standard error by $\sqrt{12}$; the $t$-statistic is unchanged, and the information ratio is likewise invariant to the reporting frequency.
- Scale the alpha by 12 and its standard error by $\sqrt{12}$; the $t$-statistic rises by $\sqrt{12}$, which is the correct annual figure because a year contains twelve independent draws.
- Scale the alpha by $\sqrt{12}$ and its standard error by 12; the $t$-statistic falls by $\sqrt{12}$, which is the conservative convention the chapter recommends for short records.
- Scale both the alpha and its standard error by 12; the $t$-statistic is unchanged, while the information ratio (a drift over a volatility) is the object that scales by $\sqrt{12}$.
<!-- YW5zOjM= -->
> Alpha is a drift, so expected returns add: $\hat\alpha_a=12\hat\alpha_m$ and $\mathrm{se}(\hat\alpha_a)=12\,\mathrm{se}(\hat\alpha_m)$. The twelves cancel and $t$ is identical either way (7.10). The classic error is annualizing alpha by 12 and its standard error by $\sqrt{12}$, inflating $t$ by $\sqrt{12}\approx3{,}46$ and manufacturing significance. The IR, being a drift over a volatility, is what scales by $\sqrt{12}$ — and $t=\mathrm{IR}\sqrt{T}$ then comes out the same whether $T$ is counted in months or years.
> Ref: Ribeiro (2026), Ch. 7, §7.3.2 (pp. 238–239), eq. (7.10); Common pitfalls (p. 257)
> Similar: Ribeiro, Problem 7.4(b),(c) (p. 259)

## detect

Q: A manager earns a true annual alpha $\alpha$ with residual volatility $\sigma(\varepsilon)$, and we ask how long a record must run for the alpha's $t$-statistic to reach a critical value $t_{crit}$. Which expression is right, and how does the requirement respond to halving the information ratio?
- $T\approx (t_{crit}/\mathrm{IR})^2$, and halving the IR quadruples the required record, because the requirement grows with the square of the inverse information ratio.
- $T\approx (t_{crit}/\mathrm{IR})^2$, and halving the IR doubles the required record, because the standard error falls as $\sqrt{T}$ and the two square roots cancel.
- $T\approx t_{crit}/\mathrm{IR}^2$, and halving the IR quadruples the required record, because only the residual variance enters the standard error of the intercept.
- $T\approx (t_{crit}\,\sigma(\varepsilon)/\alpha)$, and halving the IR doubles the required record, because the $t$-statistic is linear in the length of the sample.
<!-- YW5zOjA= -->
> Inverting $t\approx\mathrm{IR}\sqrt{T}$ gives $T\approx(t_{crit}/\mathrm{IR})^2$ (7.11). The square is what makes the requirement brutal: at $t_{crit}=1{,}96$, an IR of 0,5 needs about fifteen years and an IR of 0,25 about sixty. The chapter's table runs 96, 43, 15, 6,8 and 3,8 years for IRs of 0,20, 0,30, 0,50, 0,75 and 1,00 — only a manager at 0,75 or better can prove skill inside a decade.
> Ref: Ribeiro (2026), Ch. 7, §7.3.3 (p. 239), eq. (7.11), Example 7.2 (p. 239)
> Similar: Ribeiro, Problem 7.4(a),(d) (p. 259)

Q: A manager's five-year alpha is not statistically significant. The chapter insists on a specific asymmetry in how such a result should be read. Which statement is that asymmetry?
- Insignificance is evidence of no skill only at horizons past the years-to-detect bar, so a five-year record rejects skill for any manager whose information ratio exceeds 0,5.
- Insignificance is uninformative but significance is informative, because a short record has low power against a true alpha and therefore cannot generate a spurious one by chance.
- Insignificance means "not enough data to tell," never "no skill"; and symmetrically, an alpha that *is* significant on a short record is as likely to be a lucky draw as a skilled one.
- Insignificance and significance are equally uninformative at every horizon, because the joint-hypothesis problem means the benchmark is always in doubt regardless of sample length.
<!-- YW5zOjI= -->
> Failing to reject the null of no skill only confesses ignorance: a manager with a true IR of 0,3 needs forty-plus years, so five years of insignificance says nothing about her. The mirror image is the sharper point — the same short record that could not have proved a modest true skill can easily manufacture an apparent large one. Over practical horizons the test simultaneously has low power against the truth and high vulnerability to luck.
> Ref: Ribeiro (2026), Ch. 7, §7.3.3 (p. 240), Key result (p. 240)
> Similar: Ribeiro, Problem 7.4(d) (p. 259); Common pitfalls (p. 257)

## lies

Q: A private-credit fund reports a high Sharpe ratio and monthly returns with strong positive autocorrelation. What is the chapter's diagnosis, and what is the technical fix it names?
- The autocorrelation reveals a momentum tilt in the underlying book, so the alpha should be re-measured against the four-factor benchmark before the Sharpe ratio is trusted at all.
- The autocorrelation is the signature of appraisal smoothing, which understates volatility and inflates the Sharpe ratio; the fix is to unsmooth by inverting the moving-average filter.
- The autocorrelation reflects stale risk-free rates in the excess-return calculation, which biases the mean upward; the fix is to recompute excess returns against a matched-maturity bill.
- The autocorrelation indicates a survivorship-tainted return series, since dead funds stop reporting mid-quarter; the fix is a survivorship-free database that retains every fund that existed.
<!-- YW5zOjE= -->
> Illiquid assets are marked to model, and appraisals are sticky, so reported returns are a moving average of true returns. Smoothing leaves the mean alone but cuts the reported volatility, inflating the Sharpe ratio; positive serial correlation is the tell. Getmansky, Lo and Makarov (2004) unsmooth by inverting the filter. The general lesson: a Sharpe ratio is only as honest as the prices behind it — and it can also be *bought*, by selling out-of-the-money options, since volatility is blind to the shape of the tail.
> Ref: Ribeiro (2026), Ch. 7, §7.3.4 (pp. 240–241)
> Similar: Ribeiro, True/False (p. 259)

## bias

Q: Survivorship bias and backfill bias both inflate observed fund performance. What distinguishes them from ordinary sampling noise, and what follows for a researcher with a very large database?
- They are selection effects, not noise, so they do not shrink with more data (not even at the usual $\sqrt{T}$ rate); a larger tainted sample is a more precise wrong number.
- They are noise with a non-zero mean, so they shrink at the usual $\sqrt{T}$ rate but only after the dead funds have been reinstated into the estimation sample.
- They are heteroskedasticity in the residuals, so they leave the alpha unbiased while inflating its $t$-statistic, which is why large databases produce spurious significance.
- They are multiple-testing artefacts, so they shrink once the critical value is raised to the Harvey–Liu–Zhu bar of $t>3$ that the factor zoo of Chapter 6 requires.
<!-- YW5zOjA= -->
> Noise averages out; selection does not. A database of the funds alive today is a database of winners, worth roughly one to two-and-a-half percent per year of overstated return, and backfilled incubation histories add more. Both push the same way, and both survive any amount of extra data. The only defence is a survivorship-free database that retains every fund that ever existed and counts the failures.
> Ref: Ribeiro (2026), Ch. 7, §7.3.5 (pp. 241–242)
> Similar: Ribeiro, True/False (p. 259); Common pitfalls (p. 257)

Q: Among ten thousand funds with no skill, the best five-year record will look spectacular. The chapter says this cross-sectional selection problem and one other problem from Chapter 6 are literally the same problem. Which, and what is the correct test it implies?
- The errors-in-variables problem in Fama–MacBeth betas; the correct test forms portfolios rather than using individual funds, so that estimation error in the ranking variable averages out.
- The GRS joint test of time-series intercepts; the correct test asks whether the alphas of all funds are jointly zero rather than whether the top fund's alpha is individually large.
- The multiple-testing arithmetic of the factor zoo; the correct test asks whether the top fund's alpha exceeds what the best of ten thousand lucky funds would produce by chance.
- The bias–variance bargain behind shrinkage estimators; the correct test shrinks each fund's alpha toward the cross-sectional mean before ranking, which removes the selection effect.
<!-- YW5zOjI= -->
> "A fund with $t=2{,}5$ selected from ten thousand funds is no more impressive than a factor with $t=2{,}5$ selected from the zoo." The maximum of many noisy draws is large by construction, and next period's residual is a fresh draw, so ranking on past return selects high past alpha and, on average, no future one. Modelling the whole cross-section of luck is what the Kosowski–Timmermann–White–Wermers bootstrap and the false-discovery-rate machinery of the PhD hint do.
> Ref: Ribeiro (2026), Ch. 7, §7.3.5 (p. 242), PhD Hint (p. 242); §6.7
> Similar: Ribeiro, True/False (p. 259)

## ladder

Q: A traded factor $g$ with premium $E[g]>0$ is added to a fund's benchmark, and the fund's loading on it in the enlarged regression is $\beta_g$. How does the alpha move, and what fixes the size of the move?
- $\alpha_{\text{with }g}=\alpha_{\text{without }g}\,(1-\beta_g)$, so the alpha shrinks proportionally to the new loading and vanishes only when the fund is a pure bet on $g$.
- $\alpha_{\text{with }g}=\alpha_{\text{without }g}+\beta_g E[g]$, so adding a positively priced factor a fund loads on raises the alpha by the premium the earlier benchmark failed to credit.
- $\alpha_{\text{with }g}=\alpha_{\text{without }g}-E[g]$, so the alpha falls by the full premium of the added factor regardless of how much of the exposure the fund actually carries.
- $\alpha_{\text{with }g}=\alpha_{\text{without }g}-\beta_g E[g]$, so the alpha falls by the loading times the premium: how much exposure the fund carries, times how large the premium is.
<!-- YW5zOjM= -->
> Equation (7.15) is the omitted-variable formula of regression, and it is the arithmetic of the entire ladder: each rung subtracts a loading times a premium. A fund with $\beta_{UMD}=0{,}4$ in a market where momentum earned 7% loses $0{,}4\times7\%=2{,}8\%$ of alpha when momentum enters — which is why a momentum-heavy fund looks brilliant against the CAPM and ordinary against Carhart. What survives to the top rung is the return orthogonal to every premium anyone could have bought.
> Ref: Ribeiro (2026), Ch. 7, §7.4.1 (p. 243), eq. (7.15); Example 7.3 (p. 244)
> Similar: Ribeiro, Problem 7.6(b) (p. 259); BKM 13e, Ch. 24 §24.5 (p. 850)

Q: The ladder runs CAPM $\to$ FF3 $\to$ four-factor, each model nested in the next. Why does the chapter say an alpha can only be *reinterpreted*, never *rehabilitated*, as one climbs — and where does it say to stop?
- Because nesting guarantees the alpha falls monotonically as a matter of algebra; stop when the alpha first loses significance, which is the honest reading of the manager's residual skill.
- Because a return a richer benchmark explains was explainable all along; stop at a pre-specified, public benchmark chosen for the asset class before the fund's returns are seen.
- Because the intercept absorbs whatever the factors leave, so its interpretation is fixed by the last factor added; stop at the four-factor model, which the profession has agreed is the true model.
- Because each rung raises the $R^2$ and lowers the residual volatility, mechanically raising the information ratio; stop when adding a factor no longer changes the fund's $R^2$ materially.
<!-- YW5zOjE= -->
> The poorer benchmark simply failed to see a return that was available all along, so climbing can move a slice from "skill" to "known exposure" but never back. Nesting does *not* force monotonicity as algebra — an alpha can rise if the fund loads negatively on a positively priced factor (7.15) — and the stopping rule is a discipline, not a statistic: too few factors miscount beta as alpha, too many, especially ones chosen after seeing they kill the alpha, is the attribution face of p-hacking. "A benchmark tuned to a fund is not a measurement but an excuse."
> Ref: Ribeiro (2026), Ch. 7, §7.4.1 (pp. 243–244); §6.7
> Similar: Ribeiro, Common pitfalls (p. 257); BKM 13e, Ch. 24 §24.5 (p. 850)

## style

Q: Sharpe's (1992) returns-based style analysis regresses a fund's returns on passive style indices with coefficients constrained to be non-negative and to sum to one. What do the constraints buy, and what does the chapter compare them to?
- They restore identification when the style indices are collinear, so the coefficients become consistent estimates of the fund's true holdings, as in the errors-in-variables correction of Chapter 6.
- They make the coefficients readable as portfolio weights, trading a little in-sample fit for economic meaning — the same bias-for-variance bargain shrinkage struck in Chapter 3.
- They force the intercept to be zero, so the entire return is attributed to style, which is what makes style analysis a description of the fund rather than a test of its manager's skill.
- They guarantee the regression's $R^2$ exceeds that of the unconstrained fit, which is what allows the residual to be read as an alpha rather than as unexplained tracking error.
<!-- YW5zOjE= -->
> Unconstrained coefficients like $(0{,}7,-0{,}3,0{,}5,0{,}4,-0{,}1,-0{,}2)$ are nonsense as weights for a long-only fund; they are the regression fitting noise with offsetting bets in correlated indices — the same multicollinearity pathology that wrecked the unconstrained mean–variance weights of Chapter 3. Constraining yields something like $(0{,}45,0,0{,}35,0{,}20,0,0)$, interpretable and stable. A constrained style regression is a shrinkage estimator in disguise, and the methods ceiling holds: constrained least squares is still least squares.
> Ref: Ribeiro (2026), Ch. 7, §7.4.2 (p. 245); §3.5
> Similar: Ribeiro, True/False (p. 259); BKM 13e, Ch. 24 §24.2 (p. 839)
