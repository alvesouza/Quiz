---
quiz: "Full-Course Review — Round 2 of 5"
tags:
  s01: "S01 · State Prices, Incompleteness and Options"
  s02: "S02 · Lognormal Consumption and the Risk-Free Rate"
  s03: "S03 · The Lagrangian Frontier and the GMV Portfolio"
  s04: "S04 · The Zero-Beta CAPM and Roll's Critique"
  s05: "S05 · Risk Contributions in a Portfolio"
  s06: "S06 · Characteristic Sorts and the Fama–French Factors"
  s07: "S07 · The Information Ratio and Treynor–Black"
  s08: "S08 · Duration, Convexity and Immunization"
  s09: "S09 · Grossman–Stiglitz and the Limits to Arbitrage"
  pb: "Primer B · Utility and Risk Aversion"
---

## s01

Q: A one-period economy has three states. Two assets trade: a bond paying 1 in every state at price $P_f$, and a stock paying $x_1>x_2>x_3>0$ in states 1, 2, 3 at price $P_s$. A European call on the stock with strike $K$, $x_2\le K<x_1$, is then listed at price $C$. Assuming no arbitrage, what is the state price $q_3$ of the Arrow–Debreu security that pays 1 in state 3 only?
- $q_3=\dfrac{x_2P_f-P_s-(x_1-x_2)\,C/(x_1-K)}{x_2-x_3}$, since the call adds the state-1 claim and the bond and stock then pin down the other two
- $q_3=\dfrac{x_2P_f-P_s+(x_1-x_2)\,C/K}{x_2-x_3}$, since the call adds the state-1 claim and the bond and stock then pin down the other two
- $q_3=\dfrac{x_2P_f-P_s+(x_1-x_2)\,C/(x_1-K)}{x_2-x_3}$, since the call adds the state-1 claim and the bond and stock then pin down the other two
- $q_3=\dfrac{x_2P_f-P_s+(x_1-x_2)\,C/(x_1-K)}{x_1-x_3}$, since the call adds the state-1 claim and the bond and stock then pin down the other two
<!-- YW5zOjI= -->
> With $x_2\le K<x_1$ the call pays $(x_1-K,0,0)$, a scaled Arrow–Debreu security for state 1, so $q_1=C/(x_1-K)$. The market was incomplete with two assets and three states (only bounds on $q_1$); the option completes it. Pricing the bond and stock: $q_2+q_3=P_f-q_1$ and $x_2q_2+x_3q_3=P_s-x_1q_1$. Multiply the first by $x_2$ and subtract: $(x_2-x_3)q_3=x_2P_f-P_s+(x_1-x_2)q_1$. The sign-flipped option drops the fact that $x_1q_1$ is removed from $P_s$ while $x_2q_1$ is removed from $x_2P_f$; the $C/K$ option misreads the call's payoff; the $x_1-x_3$ denominator mixes up which payoffs remain once state 1 is priced. No arbitrage then requires $q_2,q_3>0$, which confines $C$ to exactly the price bounds the incomplete market allowed before the listing.
> Ref: Ribeiro (2026), Ch. 1, §1.4.5 (p. 18), §1.4.6 (pp. 19–20)
> Similar: Ribeiro (2026), Ch. 8, §8.8.1 (pp. 286–287); Cochrane, Asset Pricing, Ch. 4

## s02

Q: Log consumption growth is $\Delta\ln c_{t+1}\sim N(g,\sigma_c^2)$, and the representative investor has power utility with time-discount factor $\beta$ and relative risk aversion $\gamma$, so $m_{t+1}=\beta(c_{t+1}/c_t)^{-\gamma}$. Let $r_f$ be the continuously compounded risk-free rate. Holding $\beta$, $g$ and $\sigma_c$ fixed, what is $\partial r_f/\partial\gamma$, and what decides its sign?
- $g-\gamma\sigma_c^2$: positive when $g>\gamma\sigma_c^2$, the substitution force outweighing the precautionary force that $u'''>0$ creates
- $g+\gamma\sigma_c^2$: positive for every $\gamma$, the substitution force and the precautionary force pushing the rate upward together
- $g-\tfrac12\gamma\sigma_c^2$: positive when $g>\tfrac12\gamma\sigma_c^2$, the substitution force outweighing the precautionary force $u'''>0$ creates
- $\gamma\sigma_c^2-g$: positive when $\gamma\sigma_c^2>g$, the precautionary force outweighing the substitution force that $1/\gamma$ creates
<!-- YW5zOjA= -->
> $\ln m=\ln\beta-\gamma\Delta\ln c$ is normal with mean $\ln\beta-\gamma g$ and variance $\gamma^2\sigma_c^2$, so $E[m]=\beta e^{-\gamma g+\frac12\gamma^2\sigma_c^2}$ and $r_f=-\ln E[m]=-\ln\beta+\gamma g-\tfrac12\gamma^2\sigma_c^2$: impatience, growth divided by the EIS $1/\gamma$, and a precautionary term. Differentiating, $\partial r_f/\partial\gamma=g-\gamma\sigma_c^2$ (the $\tfrac12$ disappears because $\gamma^2$ is differentiated). A higher $\gamma$ both makes the investor less willing to substitute over time (raising the rate when growth is expected) and strengthens the precautionary motive (lowering it). Power utility is prudent ($u'''>0$), which is why the precautionary term exists at all. With realistic $g\approx2\%$ and $\sigma_c\approx2\%$, the derivative stays positive for any plausible $\gamma$, which is the risk-free-rate puzzle.
> Ref: Ribeiro (2026), Ch. 2, §2.2.4–§2.2.5 (p. 49); App. B, §B.4.2 (p. 360)
> Similar: Cochrane, Asset Pricing, Ch. 1 (the risk-free rate); Ribeiro (2026), Ch. 2, §2.4 (p. 55)

## s03

Q: There are $N$ risky assets with mean vector $\mu$ and nonsingular covariance matrix $\Sigma$, and no risk-free asset. Let $A=\mathbf1'\Sigma^{-1}\mathbf1$, $B=\mathbf1'\Sigma^{-1}\mu$, $C=\mu'\Sigma^{-1}\mu$, $D=AC-B^2$, and let $g$ be the global minimum-variance portfolio, the solution of $\min_w w'\Sigma w$ subject to $w'\mathbf1=1$. For an arbitrary fully invested portfolio $p$ ($w_p'\mathbf1=1$, on or off the frontier), what is $\operatorname{cov}(R_p,R_g)$, and what follows for a zero-beta partner of $g$?
- $B/A$ for every fully invested $p$, so the covariance with $g$ equals $g$'s mean and $g$'s zero-beta partner sits at mean zero
- $1/A$ only for frontier portfolios $p$, so off-frontier portfolios can have zero covariance with $g$ and act as its zero-beta partner
- $(A\mu_p-B)/D$ for every fully invested $p$, so it vanishes at $\mu_p=B/A$ and $g$ serves as its own zero-beta partner
- $1/A$ for every fully invested $p$, so no fully invested portfolio has zero covariance with $g$ and $g$ has no zero-beta partner
<!-- YW5zOjM= -->
> The Lagrangian $w'\Sigma w-2\lambda(w'\mathbf1-1)$ gives $\Sigma w=\lambda\mathbf1$, so $w_g=\Sigma^{-1}\mathbf1/A$ with variance $1/A$. Then $\operatorname{cov}(R_p,R_g)=w_p'\Sigma w_g=w_p'\mathbf1/A=1/A$ for **every** fully invested $p$, frontier or not: $\Sigma w_g$ is proportional to $\mathbf1$, so the first-order condition makes every portfolio's covariance with $g$ equal to $g$'s own variance. That covariance is strictly positive, so $g$ is the one frontier portfolio with no zero-beta partner; this is why the zero-beta construction runs from any frontier portfolio *other than* $g$. The expression $(A\mu_p-B)/D$ is a slope term from the frontier algebra, not a covariance with $g$.
> Ref: Ribeiro (2026), Ch. 3, §3.2.2 (p. 85), §3.2.6 (p. 87), §3.2.10 (p. 89); App. A, §A.6 (p. 340)
> Similar: Ribeiro (2026), Ch. 4, §4.1.4 (p. 119)

## s04

Q: A researcher picks a stock index $I$ as the market proxy, estimates every asset's beta $\beta_{iI}$ against it in one sample, and finds that the sample mean returns satisfy $\bar R_i=\gamma_0+\gamma_1\beta_{iI}$ exactly for all assets, with $\gamma_1>0$ and $\gamma_0$ exceeding the risk-free rate. What does this establish?
- That the Sharpe–Lintner CAPM holds, with $\gamma_0$ exceeding the risk-free rate because measurement error in the estimated betas flattens the slope and raises the intercept
- That $I$ is on the sample mean–variance frontier on its upper branch, and $\gamma_0$ is the mean of $I$'s zero-beta portfolio; the true market's efficiency is untested
- That the Black zero-beta CAPM holds as an equilibrium, since an intercept exceeding the risk-free rate is what borrowing restrictions predict for the true market portfolio
- That $I$ is the tangency portfolio of the sample, since only the tangency portfolio yields an exact linear beta relation, and $\gamma_0$ equals the risk-free rate in population
<!-- YW5zOjE= -->
> Frontier algebra alone implies that expected returns are exactly linear in betas against **any** frontier portfolio $p\neq g$, with intercept $E[R_{z(p)}]$, the mean of its zero-beta portfolio. The reverse also holds, so an exact sample SML against $I$ says precisely that $I$ is sample-efficient, and $\gamma_1>0$ puts it on the upper branch. That is Roll's point: the test is a joint test of the model and of the proxy's efficiency, and it says nothing about the true (unobservable) market portfolio. Sharpe–Lintner would need $\gamma_0=r_f$; the Black zero-beta CAPM is an equilibrium claim about the true market, which the proxy cannot reach; the tangency portfolio needs a risk-free asset, and with it $\gamma_0=r_f$.
> Ref: Ribeiro (2026), Ch. 4, §4.1.4 (p. 119), §4.1.5 (p. 120); Ch. 3, §3.2.10 (p. 89)
> Similar: Roll (1977), JFE 4(2); BKM 13e, Ch. 13

## s05

Q: Under the single-index model $R^e_i=\alpha_i+\beta_iR^e_m+\varepsilon_i$, residuals are uncorrelated with each other and with the index, $\operatorname{var}(R^e_m)=\sigma_m^2$ and $\operatorname{var}(\varepsilon_i)=\sigma^2(\varepsilon_i)$. A portfolio has weights $w_i$ and beta $\beta_p=\sum_iw_i\beta_i$. The additive (Euler) allocation assigns asset $i$ the share $w_i(\Sigma w)_i$ of portfolio variance, where $\Sigma$ is the covariance matrix of excess returns. Which expression is that share, and what does it imply?
- $w_i\beta_i\beta_p\sigma_m^2+w_i^2\sigma^2(\varepsilon_i)$, so a big position in a low-beta stock may add less systematic risk than a small one in a high-beta stock
- $w_i^2\beta_i^2\sigma_m^2+w_i^2\sigma^2(\varepsilon_i)$, so each stock's systematic contribution depends only on its own weight and beta, not on the portfolio beta
- $w_i\beta_i\beta_p\sigma_m^2+w_i\sigma^2(\varepsilon_i)$, so idiosyncratic contributions shrink only as fast as the weights, and diversification never removes them
- $\beta_i\beta_p\sigma_m^2+w_i\sigma^2(\varepsilon_i)$, so a stock's contribution does not scale with its weight, and position size is irrelevant to the risk budget
<!-- YW5zOjA= -->
> The model implies $\Sigma=\sigma_m^2\beta\beta'+\operatorname{diag}(\sigma^2(\varepsilon_i))$, so $(\Sigma w)_i=\beta_i\sigma_m^2\sum_jw_j\beta_j+w_i\sigma^2(\varepsilon_i)=\beta_i\beta_p\sigma_m^2+w_i\sigma^2(\varepsilon_i)$. Multiplying by $w_i$ and summing gives $\beta_p^2\sigma_m^2+\sum_iw_i^2\sigma^2(\varepsilon_i)=\sigma_p^2$, the systematic floor plus a residual term that vanishes as weights shrink. The systematic piece $w_i\beta_i\beta_p\sigma_m^2$ is governed by beta-weighted size, so raw position size is the wrong guide to where risk comes from. The $w_i^2\beta_i^2$ version drops the cross-covariances and does not sum to $\sigma_p^2$; the other two forget a factor $w_i$ in one term or both.
> Ref: Ribeiro (2026), Ch. 5, §5.3.1 (p. 161), §5.3.7 (p. 166)
> Similar: BKM 13e, Ch. 8 (the single-index model); Ribeiro (2026), Ch. 3, §3.1 (p. 78)

## s06

Q: A researcher sorts stocks into deciles on a characteristic $X$ and finds a monotone, high-$t$ spread in average returns. She then builds a factor $F_X$ that is long the top and short the bottom of the same sort, adds it to the market, and shows that the two-factor model prices the ten $X$ deciles with small alphas. What does the last step add to the evidence?
- That $X$ is a priced risk, since the $F_X$ loadings rise across the deciles in step with average returns, which is the covariance evidence Daniel and Titman found missing
- That $X$ is a mispricing, since a characteristic whose own long–short portfolio explains its deciles shows that the characteristic, not any covariance, drives returns
- Little beyond the sort, since a factor built from a sort prices its own sort portfolios almost mechanically; a risk reading needs other test assets and a story for $F_X$
- That the model is correctly specified, since pricing the $X$ deciles with small alphas means a GRS test cannot reject it for any other set of test portfolios either
<!-- YW5zOjI= -->
> A monotone sort establishes an association between $X$ and average returns, without a model; it cannot tell covariance from mispricing, and it says nothing about costs, snooping or persistence. Building $F_X$ from the same sort and then pricing the same deciles is close to circular: the deciles' average returns line up with their loadings on a factor constructed as the difference of the extreme deciles. This is why Fama–French factors are judged on test assets beyond their own construction, and why a factor needs a reason to be priced beyond "it prices the sort". The GRS result on one set of test assets does not transfer to others, and loadings rising with returns is what any characteristic-mimicking factor produces.
> Ref: Ribeiro (2026), Ch. 6, §6.3.5 (p. 202), §6.4.1 (p. 202), §6.5 (p. 205)
> Similar: Ribeiro (2026), Ch. 6, §6.3.4 (pp. 199–201); Ch. 6, §6.2.4 (pp. 197–198)

## s07

Q: In the Treynor–Black model an investor combines the index $M$ with an active portfolio of $J$ securities weighted in proportion to $\alpha_j/\sigma^2(\varepsilon_j)$, where $\alpha_j$ is security $j$'s alpha and $\sigma(\varepsilon_j)$ its residual volatility against $M$; the attainable squared Sharpe ratio is reported as $S_M^2+\sum_j\mathrm{IR}_j^2$, with $\mathrm{IR}_j=\alpha_j/\sigma(\varepsilon_j)$. Two of the securities are value stocks whose residuals are positively correlated because both load on an omitted value factor. What is the consequence?
- Nothing changes, since the Treynor–Black weights depend only on each security's own alpha and residual variance, so the formula stays exact whatever the residual correlations
- The attainable Sharpe ratio exceeds the formula, since positively correlated residuals let the two alphas reinforce each other and so raise the active portfolio's information ratio
- The formula still holds, but the two securities must be dropped from the active portfolio, since a correlated residual is systematic risk that the index has already priced
- The formula overstates the attainable Sharpe ratio, since adding squared ratios needs uncorrelated residuals, and the two positions are partly one bet that counts once in breadth
<!-- YW5zOjM= -->
> The additivity $\mathrm{IR}_A^2=\sum_j\mathrm{IR}_j^2$ comes from applying the tangency rule $\Sigma^{-1}\mu$ to residuals with a **diagonal** covariance matrix, the single-index assumption. When two residuals are positively correlated the residual covariance matrix is no longer diagonal: the optimal weights change and the true $\mathrm{IR}_A^2=\alpha'\Sigma_\varepsilon^{-1}\alpha$ falls below the sum, because two correlated bets with the same-sign alpha diversify each other less than independent ones. In the fundamental law $\mathrm{IR}\approx\mathrm{IC}\sqrt{\text{breadth}}$, breadth counts independent bets, not positions. The correlation is a missing factor, which is exactly where the diagonal assumption of the risk model breaks.
> Ref: Ribeiro (2026), Ch. 7, §7.2.3 (p. 235); Ch. 5, §5.2.3 (p. 159)
> Similar: BKM 13e, Ch. 27 (Treynor–Black); Ribeiro (2026), Ch. 5, §5.3.5 (p. 165)

## s08

Q: A liability pays $L$ at horizon $H$; at a flat annually compounded yield $y$ its present value is $PV_L$. It is immunized with a barbell of two zero-coupon bonds maturing at $H_1<H<H_2$, with present-value weights $w_1,w_2\ge0$, $w_1+w_2=1$, chosen so that $w_1H_1+w_2H_2=H$ and total value equals $PV_L$. A zero maturing at $T$ has convexity $T(T+1)/(1+y)^2$. To second order, what is the change in surplus (assets minus liability) after an instantaneous parallel shift $\Delta y$?
- $-\tfrac12\,PV_L\,w_1w_2(H_2-H_1)^2(\Delta y)^2/(1+y)^2$: a loss whatever the direction of the parallel shift
- $+\tfrac12\,PV_L\,w_1w_2(H_2-H_1)^2(\Delta y)^2/(1+y)^2$: a gain whatever the direction of the parallel shift
- $+\tfrac12\,PV_L\,(w_1H_1^2+w_2H_2^2)(\Delta y)^2/(1+y)^2$: a gain whatever the direction of the parallel shift
- $+\tfrac12\,PV_L\,w_1w_2(H_2-H_1)^2\,\Delta y/(1+y)$: a gain only when the parallel shift is upward
<!-- YW5zOjE= -->
> Matched value and duration cancel the level and first-order terms, leaving $\Delta S\approx\tfrac12PV_L(C_A-C_L)(\Delta y)^2$. With $C_A=\sum_kw_kH_k(H_k+1)/(1+y)^2$ and $C_L=H(H+1)/(1+y)^2$, the linear terms cancel because $w_1H_1+w_2H_2=H$, leaving $C_A-C_L=(w_1H_1^2+w_2H_2^2-H^2)/(1+y)^2=w_1w_2(H_2-H_1)^2/(1+y)^2$: the cross-sectional variance of the asset maturities. The barbell is more convex than the bullet liability, so a parallel shift in either direction raises the surplus. The catch is that a flat curve moving in parallel is itself an assumption: this gain is the price of exposure to non-parallel moves (a twist that lowers short rates and raises long rates hurts the barbell), which is why immunization must be rebalanced and why a matching zero is the only exact hedge.
> Ref: Ribeiro (2026), Ch. 8, §8.3.2 (p. 270), §8.3.3 (p. 271)
> Similar: BKM 13e, Ch. 16 §16.3 (convexity); Ribeiro (2026), Ch. 8, §8.3.4 (p. 272)

## s09

Q: Two mispricings carry the same information and are equally costly to discover. One sits in large, liquid, cheap-to-short stocks; the other in small, illiquid, hard-to-short stocks with high idiosyncratic volatility, traded mainly by arbitrageurs who manage outside capital. Combining Grossman–Stiglitz with the limits to arbitrage, which prediction follows?
- More mispricing survives in the small stocks, since what sets the equilibrium degree of efficiency is the full cost of acting on information, not the cost of learning it alone
- The same mispricing survives in both, since Grossman–Stiglitz ties the equilibrium degree of efficiency to the cost of acquiring the information, and that cost is identical here
- More mispricing survives in the large stocks, since deep liquidity attracts the noise traders whose demand keeps prices away from value in a Grossman–Stiglitz equilibrium
- No mispricing survives in either, since any arbitrageur who finds either gap will trade until it closes, and a gap that stays open was compensation for risk all along
<!-- YW5zOjA= -->
> Grossman–Stiglitz says prices can never be fully revealing while information is costly: the gap must stay just large enough to pay the informed for their effort. The limits to arbitrage extend "effort" to everything needed to act: trading costs, short-sale constraints, idiosyncratic risk that cannot be hedged, noise-trader risk at finite horizons (De Long et al.), and the risk that clients withdraw capital after losses (Shleifer–Vishny). All are higher in small, illiquid, hard-to-short stocks, so the equilibrium gap is wider there, which is where anomalies are in fact strongest. The "identical cost" answer stops at discovery cost; the "no gap" answer is the frictionless arbitrage argument, which both frameworks deny.
> Ref: Ribeiro (2026), Ch. 9, §9.1.4 (p. 304), §9.1.5 (pp. 305–306)
> Similar: Shleifer and Vishny (1997), JF 52(1); BKM 13e, Ch. 12

## pb

Q: Investor 1 has CARA utility $u(W)=-e^{-aW}$ and investor 2 has CRRA utility $u(W)=W^{1-\gamma}/(1-\gamma)$, and at initial wealth $W_0$ their Arrow–Pratt absolute risk aversions coincide, $a=\gamma/W_0$. Each chooses a risky holding when the excess return is normal with mean $E[r]-r_f$ and variance $\sigma^2$ (treat the CRRA choice with the usual mean–variance approximation), and each prices a fixed additive gamble $\tilde\varepsilon$ with $E[\tilde\varepsilon]=0$ and small variance by the Pratt approximation. Wealth doubles to $2W_0$. What happens?
- Investor 1 keeps the same risky share and the same premium for the gamble; investor 2 keeps the same risky dollars and roughly halves the premium
- Investor 1 keeps the same risky dollars and halves the premium for the gamble; investor 2 doubles the risky dollars and keeps the same premium
- Investor 1 keeps the same risky dollars and the same premium for the gamble; investor 2 doubles the risky dollars and roughly halves the premium
- Both double their risky dollars, since they share the same absolute aversion at $W_0$, and both roughly halve their premium for the gamble
<!-- YW5zOjI= -->
> CARA: $A(W)=a$ at every wealth, so the dollar holding $D^*=(E[r]-r_f)/(a\sigma^2)$ and the Pratt premium $\pi\approx\tfrac12a\operatorname{var}(\tilde\varepsilon)$ are both independent of wealth; the risky **share** halves. CRRA: $A(W)=\gamma/W$ falls with wealth (DARA) while relative aversion is constant, so the share $y^*=(E[r]-r_f)/(\gamma\sigma^2)$ is fixed and dollars double, and the premium for a fixed-size gamble becomes $\tfrac12(\gamma/2W_0)\operatorname{var}(\tilde\varepsilon)$, about half. Equal absolute aversion at one wealth level says nothing about how it moves with wealth, which is what the two families differ on: constant absolute aversion fixes the dollars; constant relative aversion fixes the share.
> Ref: Ribeiro (2026), App. B, §B.3 (pp. 356–357), §B.4 (p. 357), §B.6.2 (p. 364)
> Similar: Ribeiro (2026), App. B, §B.6.1 (p. 362); BKM 13e, Ch. 6
