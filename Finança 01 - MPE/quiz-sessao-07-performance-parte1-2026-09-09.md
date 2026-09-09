---
quiz: "Session 7 — Performance, Part 1: The Arithmetic and the Five Measures"
tags:
  illposed: "1 · Why 'Beat the Market' Is Ill-Posed"
  arithmetic: "2 · Sharpe's Arithmetic and the Berk–Green Equilibrium"
  measures: "3 · The Five Measures and What Each Assumes"
  tb: "4 · Treynor–Black: the IR Governs the Attainable Sharpe"
---

## illposed

Q: Chapter 7 closes by claiming that each of its three toolkits answers exactly one of the three questions that make "beat the market" ill-posed. Which pairing is the chapter's?
- The attribution ladder answers luck versus skill; Sharpe's arithmetic answers the benchmark question; the statistics of alpha, with their biases, answer gross versus net.
- The statistics of alpha answer the benchmark question; the attribution ladder answers gross versus net; the Berk–Green equilibrium answers luck versus skill.
- The attribution ladder answers the benchmark question; Sharpe's arithmetic and Berk–Green answer gross versus net; the statistics of alpha answer luck versus skill.
- The Berk–Green equilibrium answers the benchmark question; the statistics of alpha answer gross versus net; the attribution ladder, rung by rung, answers luck versus skill.
<!-- YW5zOjI= -->
> The three questions are "against what, after what, and how sure?" The ladder is a search for the honest benchmark; Sharpe's identity and Berk–Green are about costs and fees, i.e. gross versus net; the standard error, the years-to-detect bar, the survivorship and backfill corrections and the multiple-testing deflation are the luck-versus-skill apparatus.
> Ref: Ribeiro (2026), Ch. 7, §7.1.1 (p. 229), §7.7 (p. 256)
> Similar: Ribeiro, Problem 7.1(d) (p. 258); True/False 1 (p. 259)

Q: In a coin-flipping tournament, ten thousand managers with no skill whatsoever flip a fair coin each year, and roughly ten of them finish a decade unbeaten. What does that establish about winning streaks?
- That a streak cannot by itself separate the skilled from the lucky, because the lucky produce streaks too, in numbers that grow with the size of the contest.
- That long winning streaks are meaningless as evidence, because chance alone manufactures every streak that the industry ever advertises to investors.
- That the correct null is a fair coin, so a manager is skilled precisely when the length of the streak exceeds what a fair coin would deliver at 5% significance.
- That skill and luck are indistinguishable in principle, because a finite record is one draw and no statistic can improve on the flip of a coin as a forecast.
<!-- YW5zOjA= -->
> The chapter is careful: the lesson "is not that long winning streaks are meaningless (a genuinely skilled manager is more likely to produce one)", but that the lucky also generate streaks in numbers rising with the number of players. That is why the serious question is never "did this manager beat the market?" but "did she beat it by more, and for longer, than the luckiest of thousands of unskilled managers would have by chance?" — the same order-statistics logic as the factor zoo and the fund-selection problem.
> Ref: Ribeiro (2026), Ch. 7, §7.1.1 (p. 230), §7.3.5 (p. 241)
> Similar: Ribeiro, True/False 1 (p. 259); Common pitfalls (p. 257)

## arithmetic

Q: An active manager objects to Sharpe's arithmetic: "the market is not a fixed pie — skilled professionals extract returns from retail investors and forced sellers, who are outside the professional pool." Why does the chapter say the objection cannot repeal the identity?
- Because retail investors and index funds trade at the close, so their losses accrue to market makers rather than to the active pool that the identity partitions.
- Because the arithmetic is about gross returns while the objection is about net returns, and the two coincide only when trading costs are identical across all participants.
- Because the objection is an empirical claim about a particular market, and the identity is stated for markets in which the passive share is large enough for the aggregation to bind.
- Because the identity covers all holders of the market, amateur and professional alike, so "dumb money" losses only relabel who loses: the average active dollar still earns the market.
<!-- YW5zOjM= -->
> Sharpe's partition is exhaustive: passive investors hold market weights, so whoever deviates must, in aggregate, hold the complement, which is again the market. If some participants systematically underperform, others systematically outperform by the identical amount, and the average active dollar still earns the market before costs. What the objection correctly identifies is that the pool has winners and losers — dispersion — not that its average can exceed the index.
> Ref: Ribeiro (2026), Ch. 7, §7.1.2 (p. 231)
> Similar: Ribeiro, Problem 7.2(a),(c) (p. 258)

Q: Which statement about Sharpe's arithmetic of active management is exactly right as the chapter states it?
- It is an empirical regularity documented across markets and decades, so a market with unusually many unskilled participants can generate a positive average active alpha before costs.
- It is an accounting identity constraining the average of the active pool, not its dispersion, so it is compatible with genuine skill redistributing returns within the pool.
- It is an equilibrium result requiring that investors be rational and that fund flows compete away any positive net alpha, which is what makes the pool's average equal the index.
- It is a corollary of the CAPM, since only if the market portfolio is mean–variance efficient does the value-weighted average of all deviations from it earn the market return.
<!-- YW5zOjE= -->
> The chapter insists on the modality: "This is not an empirical regularity that might fail in some market or some decade; it is an identity, true by the definition of a market portfolio." It needs neither rationality nor the CAPM — that is Berk–Green's job and Chapter 4's respectively. And it constrains only the average: skill is a zero-sum competition inside the pool, so winners and losers coexist with a pool average of exactly the market before costs, and below it after.
> Ref: Ribeiro (2026), Ch. 7, §7.1.2 (pp. 230–231), Key result (p. 231)
> Similar: Ribeiro, Problem 7.2(b),(d) (p. 258); BKM 13e, Ch. 24 §24.1 (p. 827)

Q: The Berk–Green (2004) equilibrium takes managerial skill seriously and still predicts zero net alpha. Which chain of reasoning is theirs, and what does it predict about flows?
- Skill is scarce and non-scalable, so fees rise until gross alpha is exhausted; flows should therefore be unrelated to past performance, and net alpha should persist in the tails.
- Skill has decreasing returns to scale and investors compete for access, so the fund grows until gross alpha just covers fees; flows chase past performance though it does not predict future net returns.
- Skill is competed away by other managers imitating the strategy, so gross alpha itself decays to zero; flows chase past performance and past performance predicts future gross but not net returns.
- Skill is unobservable, so investors cannot tell it from luck and price all funds identically; flows are unrelated to performance, and net alpha is zero because fees are set by competition among investors.
<!-- YW5zOjE= -->
> Berk–Green reconciles two facts that look contradictory: managers demonstrably have skill (positive gross alphas) and investors demonstrably do not benefit (net alphas near zero, no persistence). Both hold because fund size and fees adjust until they do. A zero net alpha is therefore not evidence of no skill — it is the equilibrium price of a scarce, imperfectly scalable resource, and it is why cost, the one thing a manager cannot inflate, is the most reliable predictor of a fund's future net return.
> Ref: Ribeiro (2026), Ch. 7, §7.1.3 (pp. 231–232)
> Similar: Ribeiro, True/False (p. 259); BKM 13e, Ch. 24 §24.1 (p. 827)

## measures

Q: A concentrated fund holds few names; a diversified fund holds many. They can be ranked oppositely by the Sharpe ratio and the Treynor ratio. What creates the flip, and which ranking is right?
- The flip comes from a difference in market beta, and Treynor is right whenever the fund will be the investor's entire risky position, since beta is the only priced risk.
- The flip comes from a difference in alpha, and Sharpe is right whenever the fund is one sleeve of many, since alpha is what a sleeve contributes to the book.
- The flip comes from a difference in the sample mean excess return, and neither ranking is right until the two funds are rescaled to a common volatility using $M^2$.
- The flip comes from a difference in idiosyncratic risk, and the right ranking is settled by how the fund will be held: alone (Sharpe) or as one sleeve of many (Treynor).
<!-- YW5zOjM= -->
> Sharpe divides by total volatility $\sigma_P$ and Treynor by $\beta_P$; the two denominators differ by exactly the idiosyncratic component, so two funds differing in residual risk can be ranked oppositely. Held alone, that idiosyncratic risk is risk the investor actually bears and Sharpe is the correct measure; held as one of twenty sleeves, it washes out at the book level and only beta consumes risk budget, so Treynor is correct. The disagreement is two measures answering two different questions.
> Ref: Ribeiro (2026), Ch. 7, §7.2.2 (pp. 234–235)
> Similar: Ribeiro, Problem 7.3(a),(d) (p. 258); BKM 13e, Ch. 24 §24.1 (p. 827)

Q: The chapter calls Jensen's alpha "a numerator in search of a denominator" and calls $M^2$ a relabelling. Which reading of the decision table is correct?
- Jensen's alpha ranks funds correctly whenever the benchmark is right, and $M^2$ adds information the Sharpe ratio lacks by pricing the fund at the market's volatility.
- Jensen's alpha cannot rank funds alone: a large alpha bought with large tracking error may be worse than a small cheap one, and $M^2$ is the Sharpe ratio restated in return units.
- Jensen's alpha and the information ratio rank identically because they share a numerator, and $M^2$ ranks identically to the Treynor ratio because both hold systematic risk fixed.
- Jensen's alpha is the only measure valid under a multi-factor benchmark, and $M^2$ is the only one valid when the fund is levered, since it delevers the fund to the market's volatility.
<!-- YW5zOjE= -->
> Alpha is a return, not a ratio: it measures value added against a stated benchmark but says nothing about the risk taken to earn it. The information ratio $\alpha_P/\sigma(\varepsilon_P)$ supplies the missing denominator. $M^2=(S_P-S_M)\sigma_M$ is the Sharpe ratio restated as "P beat the market by x% at equal risk" — a monotone transform, so identical rankings, more legible to a client.
> Ref: Ribeiro (2026), Ch. 7, §7.2.1 (p. 233), §7.2.2 (p. 234)
> Similar: Ribeiro, Problem 7.1(c) (p. 258); BKM 13e, Ch. 24 §24.1 (p. 827)

Q: The chapter names the Sortino and Calmar ratios beyond the classical five. What defect of the Sharpe ratio are they built to see, and what is their place in the chapter?
- They repair the Sharpe ratio's dependence on the benchmark, since neither requires a market index, and the chapter adopts them for evaluating overlays where no benchmark is agreed.
- They repair the Sharpe ratio's dependence on the sample mean, since drawdowns and downside deviations are estimated more precisely, and the chapter adopts them for short records.
- They see the shape of the tail, which volatility is blind to, and the chapter names them as the practical downside-risk measures while keeping the classical five as its working set.
- They see the smoothing induced by illiquid marks, which volatility understates, and the chapter adopts them whenever reported returns show positive autocorrelation.
<!-- YW5zOjI= -->
> Sortino replaces total volatility with downside deviation; Calmar divides by the worst peak-to-trough drawdown. Both answer the Sharpe ratio's blindness to tail shape — a strategy selling disaster insurance has low volatility, a hideous drawdown, and a gorgeous Sharpe ratio until it is flattened. The chapter names them and keeps the classical five, whose assumptions are cleanest, adding that no single ratio captures a return distribution.
> Ref: Ribeiro (2026), Ch. 7, §7.2.1 (p. 234), §7.3.4 (pp. 240–241)
> Similar: Ribeiro, True/False (p. 259)

## tb

Q: An investor holds the market index, whose Sharpe ratio is $S_M$, and adds an active portfolio with alpha $\alpha_A$ and residual volatility $\sigma(\varepsilon_A)$ at the weight that maximizes the combined Sharpe ratio. What is the attainable combined Sharpe ratio?
- $\sqrt{S_M^2+\left(\alpha_A/\sigma(\varepsilon_A)\right)^2}$, because the residual bet is orthogonal to the market, so the squared Sharpe ratios add.
- $S_M+\alpha_A/\sigma(\varepsilon_A)$, because the active overlay adds its own reward-to-risk slope directly on top of the slope the index already offers.
- $\sqrt{S_M^2+\left(\alpha_A/\sigma_A\right)^2}$, because the improvement is alpha per unit of the active portfolio's total volatility $\sigma_A$.
- $S_M\sqrt{1+\alpha_A/\sigma(\varepsilon_A)}$, because the overlay scales the index's slope by its own reward-to-risk ratio rather than adding a further term to it.
<!-- YW5zOjA= -->
> Writing $R^e_A=\alpha_A+\beta_A R^e_{mkt}+\varepsilon_A$, the combined position is a two-asset tangency problem in the market and the pure alpha bet $\varepsilon_A$, which is uncorrelated with the market by construction. For uncorrelated assets the squared Sharpe ratios add: $S^2_{\text{combined}}=S_M^2+\mathrm{IR}_A^2$ (7.6). The denominator is residual volatility, not total volatility — charging the overlay for the market risk the investor already owns is exactly the error the identity corrects.
> Ref: Ribeiro (2026), Ch. 7, §7.2.3 (p. 235), eq. (7.6); Example 7.1 (p. 236)
> Similar: Ribeiro, Problem 7.3(c) (p. 258); BKM 13e, Ch. 24 §24.1 (p. 827)

Q: An investor holds the index and adds an active portfolio with alpha $\alpha$ and residual volatility $\sigma(\varepsilon)$; separately, a manager can spread her edge over $J$ mutually uncorrelated bets each with information ratio $\mathrm{IR}_j$. Which pair of statements is right?
- The optimal active weight is $w^\star\propto\alpha/\sigma(\varepsilon)$, and $J$ uncorrelated bets give $\mathrm{IR}^2=\sum_j \mathrm{IR}_j$, so depth in a single bet beats breadth across many.
- The optimal active weight is $w^\star\propto\alpha\,\sigma(\varepsilon)$, and $J$ uncorrelated bets give $\mathrm{IR}=\sum_j \mathrm{IR}_j$, so breadth adds linearly and a concentrated book is always dominated.
- The optimal active weight is $w^\star\propto\alpha/\sigma_A$, and $J$ uncorrelated bets give $\mathrm{IR}=\max_j \mathrm{IR}_j$, so only the manager's single best idea governs the improvement.
- The optimal active weight is $w^\star\propto\alpha/\sigma^2(\varepsilon)$, and $J$ uncorrelated bets give $\mathrm{IR}^2=\sum_j \mathrm{IR}_j^2$, so independent alphas add in quadrature.
<!-- YW5zOjM= -->
> Treynor–Black gives $w^\star\propto\alpha/\sigma^2(\varepsilon)$ — more alpha and less residual *variance* both argue for a larger tilt. Uncorrelated residuals make squared Sharpe ratios additive (7.7), so twenty independent bets at $\mathrm{IR}_j=0{,}2$ give $\sqrt{20}\times0{,}2\approx0{,}89$. This is Grinold's fundamental law, $\mathrm{IR}\approx \mathrm{IC}\times\sqrt{\text{breadth}}$: a weak edge on very many independent positions builds a provable record; one strong view cannot, because a single bet carries irreducible residual risk.
> Ref: Ribeiro (2026), Ch. 7, §7.2.3 (pp. 235–236), eqs. (7.6)–(7.7)
> Similar: Ribeiro, Problem 7.3(c) (p. 258); BKM 13e, Ch. 24 §24.1 (p. 827)
