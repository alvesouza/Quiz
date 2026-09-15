---
quiz: "Session 8 — Fixed Income and Derivatives, Part 3: Replication, the Tree, and the Risk-Neutral Measure"
tags:
  carry: "1 · Forwards, Futures, and Cost of Carry"
  parity: "2 · Payoffs, Strategies, and Put–Call Parity"
  american: "3 · Bounds, Early Exercise, and Dividends"
  tree: "4 · The Binomial Tree as State Pricing"
  rn: "5 · The Risk-Neutral Measure and Black–Scholes"
---

## carry

Q: Cost-of-carry gives $F_0=S_0e^{(r-q)T}$, and in Example 8.4 an index at 4,000 with $r=5\%$, $q=2\%$ and $T=0.5$ yields $F_0=4{,}060.45$. What is the chapter's point about what is absent from that number?
- The expected terminal price is absent because it is unobservable, so the carry formula is a practical approximation that a forecast of $S_T$ would in principle improve upon.
- The dividend yield is absent from the replication itself and enters only as a quoting adjustment, which is why a non-dividend index would carry at the same 3% net rate.
- No expectation of $S_T$ enters at all: two ways of owning the asset at $T$ must cost the same today, so the forward is the spot grown at the net carry, pinned by arbitrage.
- The equity premium is absent because it cancels between the long and short legs of the cash-and-carry trade, leaving only the part of the expected return not priced by the CAPM.
<!-- YW5zOjI= -->
> Route one buys the forward and sets aside $F_0e^{-rT}$; route two buys the asset for $S_0$ and collects the yield $q$. Both deliver one unit at $T$, so the law of one price fixes $F_0$ — with no expectation, no volatility and no equity premium anywhere. Hence the figure: the 5% financing cost outweighs the 2% dividend, so deferring purchase costs the net 3% per year, or 1.5% over six months. Without the dividend the forward would be higher still, $4{,}000e^{0.025}=4{,}101.26$.
> Ref: Ribeiro (2026), Ch. 8, §8.6.2 (pp. 280–282), Example 8.4, eq. (8.18)
> Similar: Ribeiro, Problem 8.6(a),(c),(d) (p. 295); True/False 8 (p. 296)

Q: Which statement about futures, forwards, and marking-to-market is exactly right as the chapter puts it?
- A future settles daily, removing counterparty risk; its price differs from the forward's only when the underlying is correlated with rates, and that wedge is second-order.
- A future settles daily, which removes counterparty risk; its price therefore exceeds the forward's by the accumulated interest on the margin account at any positive rate.
- A future settles once, at maturity, like a forward, but through a clearing house; the daily margin call is a credit device that has no effect on the contract's value at all.
- A future settles daily, so its value drifts as $V_t=(F_t-F_0)e^{-r(T-t)}$ between settlements; the forward, settling once, is the contract whose value stays at zero throughout.
<!-- YW5zOjA= -->
> Marking-to-market collects gains and losses as they accrue, which is why futures trade to anonymous exchange-cleared counterparties while forwards are bilateral OTC deals. Because interim cash is reinvested, a positive correlation between the underlying and rates pushes the futures price marginally above the forward's; with deterministic or uncorrelated rates the two coincide. And (8.19) describes the drifting value of the *forward* — the future pays that value out daily, resetting to zero.
> Ref: Ribeiro (2026), Ch. 8, §8.6.2 (p. 282), §8.6.3 (p. 282)
> Similar: Ribeiro, True/False 16 (p. 296); BKM 13e, Ch. 22 §22.4 (p. 777)

## parity

Q: Put–call parity, $C+Ke^{-rT}=P+S_0$, is derived by comparing two portfolios. Which description of the derivation and its scope is right?
- A call plus a bond and a put plus the stock both pay $\max(S_T,K)$, so replication alone fixes the identity; it needs no model at all, and it holds exactly for European options.
- A call plus the stock and a put plus a bond both pay $\max(S_T,K)$, so the identity is fixed by replication, and it extends to American options because early exercise is never optimal.
- A long call and a short put replicate the stock, so parity follows from the CAPM applied to the replicating portfolio; it therefore holds only when the market is mean-variance efficient.
- A call plus a bond and a put plus the stock both pay $\max(S_T,K)$, so parity holds under any pricing model provided the underlying's volatility is constant over the option's life.
<!-- YW5zOjA= -->
> Portfolio A (call plus a zero paying $K$) is worth $\max(S_T-K,0)+K=\max(S_T,K)$; portfolio B (put plus the share) is worth $\max(K-S_T,0)+S_T=\max(S_T,K)$. Identical payoffs, identical prices — no probabilities, no volatility, no model. The scope matters: parity is exact for European options; American options satisfy only inequalities, since the early-exercise right can only add value (and for an American put it does).
> Ref: Ribeiro (2026), Ch. 8, §8.7.3 (pp. 284–285), eq. (8.22)
> Similar: Ribeiro, Problem 8.7(c), Problem 8.8(a) (p. 295); True/False 12, 20 (pp. 296–297)

Q: In Example 8.5, $S_0=K=100$, $r=5\%$, $T=1$, and the Black–Scholes call is $C=10.4506$, so parity gives $P=10.4506-100+95.1229=5.5735$, which matches the Black–Scholes put exactly. What does the agreement demonstrate?
- That Black–Scholes is internally consistent at 20% volatility, which is evidence for the lognormal assumption, since a model with fatter tails would break the identity.
- That the put and the call carry the same implied volatility here, which is the at-the-money case in which the volatility smile is flat by construction.
- That parity is an identity no model can violate, so once the call is priced the put is not a separate problem, and any quoted put breaking it is an arbitrage.
- That the call and the put are equally valuable at the money, the 4.88 difference being exactly the interest on the strike over one year at the risk-free rate.
<!-- YW5zOjI= -->
> Parity is a replication identity, so *any* arbitrage-free model must reproduce it — the agreement tests the arithmetic, never the lognormal assumption. Its practical content is that the put comes free once the call is priced, and that a quoted put violating (8.22) beyond transaction costs is a riskless arbitrage against the call, the stock and the bond. (The $C-P$ gap here is $S_0-Ke^{-rT}=4.8771$, the value of a forward struck at $K$.)
> Ref: Ribeiro (2026), Ch. 8, §8.7.3, Example 8.5 (p. 285)
> Similar: Ribeiro, Problem 8.8(a) (p. 296)

## american

Q: The lower arbitrage bound on a European call is $C\ge\max(S_0-Ke^{-rT},0)$. What does the chapter draw from it, and where does the bound come from?
- It comes from the upper bound $C\le S_0$ read in reverse, and it implies a call is always worth more than the stock net of the strike, so deep-in-the-money calls trade at parity.
- It comes from put–call parity with $P\ge0$ dropped, and it says a call is worth at least a forward, so it carries time value above intrinsic and should not be exercised early.
- It comes from the binomial model with one step, and it implies that a call's time value is largest at the money, since the bound binds exactly where the payoff kinks.
- It comes from the assumption that the stock cannot be short-sold, and it implies the call is bounded below by its intrinsic value, which is what rules out early exercise.
<!-- YW5zOjE= -->
> Parity gives $C=S_0-Ke^{-rT}+P$, and a put is never a liability, so $C\ge S_0-Ke^{-rT}$ — which exceeds the intrinsic value $\max(S_0-K,0)$ whenever rates are positive. That gap *is* time value, and it is why exercising an American call on a non-dividend stock, which collects only intrinsic value, throws money away. The upper bound $C\le S_0$ is separate and immediate: a right to buy the stock cannot be worth more than the stock.
> Ref: Ribeiro (2026), Ch. 8, §8.7.4 (p. 285), eq. (8.23)
> Similar: Ribeiro, True/False 10 (p. 296); BKM 13e, Ch. 21 §21.4 (p. 730)

Q: Which pair of early-exercise statements is exactly right, and why does the tree matter for one of them?
- An American call on a non-dividend stock may be exercised early once it is deep in the money, and an American put never should be; the tree confirms both node by node.
- An American call should never be exercised early even when dividends are paid, since the dividend is already in the price; an American put may be, so the tree prices it.
- An American call on a non-dividend stock should never be exercised early, and dividends cannot change that; an American put is worth the same as a European put.
- An American call on a non-dividend stock is never exercised early, though a dividend can make it optimal; an American put may be, which is why the tree prices it.
<!-- YW5zOjM= -->
> Two facts, both from comparing "exercise now" with "hold". Exercising a call collects intrinsic value, discarding time value and the interest on $K$, so without dividends it never pays — and the American call equals the European, priced by Black–Scholes. A dividend flips it: the holder does not receive it and may exercise just before the ex-date. An American put can be optimal to exercise, since the strike collected in cash earns interest, so it is worth strictly more than a European put and has no closed form; the tree decides node by node.
> Ref: Ribeiro (2026), Ch. 8, §8.7.5 (pp. 285–286), §8.8.4 (p. 289)
> Similar: Ribeiro, True/False 10, 28 (pp. 296–297); BKM 13e, Ch. 21 §21.3 (p. 722)

## tree

Q: In the one-period tree of Example 8.6 ($S_0=100$, $u=1.2$, $d=0.8$, $R=1.05$, $K=100$) the call is worth 11.90, with $\Delta=0.5$ and $B=-38.10$. Where does the physical probability of an up move enter?
- It enters through $q=(R-d)/(u-d)$, which is the physical probability corrected for risk aversion, so a physical probability of 0.7 would raise $q$ above 0.625.
- It enters only through $S_0$, which already reflects it, and nowhere else: replication matches the payoff state by state, so 0.7 or 0.3 both give 11.90.
- It enters through the expected payoff $0.7(20)+0.3(0)=14$, which must then be discounted at the option's own risk-adjusted rate rather than at the risk-free rate.
- It enters nowhere, and this is why the binomial price is only an approximation to the true price, which would require the physical distribution and a utility function.
<!-- YW5zOjE= -->
> The replication is state by state — $\Delta S_0u+RB=C_u$ and $\Delta S_0d+RB=C_d$ — so probabilities never appear, and the option must cost what the portfolio costs: $0.5(100)-38.10=11.90$. The weights $q=0.625$ and $1-q$ that emerge from rearranging that cost are a probability distribution but *not* the real one. What does carry the market's expectation is the stock price itself, and the option pricer inherits it through the hedge rather than forecasting it.
> Ref: Ribeiro (2026), Ch. 8, §8.8.1 (pp. 286–287), Example 8.6, eqs. (8.24)–(8.25)
> Similar: Ribeiro, Problem 8.7(b),(d) (p. 295); True/False 6, 14 (p. 296)

Q: The chapter recovers the two Arrow–Debreu state prices from the stock and the bond, then shows the binomial option price is the same object. Which statement of that link is right?
- The bond gives $q_u+q_d=1/R$ and the stock gives $S_0uq_u+S_0dq_d=S_0$; solving both and summing payoffs against the state prices reproduces (8.25), with $\tilde\pi(u)=Rq_u$.
- The bond gives $q_u+q_d=1$ and the stock gives $uq_u+dq_d=R$; the state prices are therefore the risk-neutral probabilities themselves, which is why no discounting appears in (8.25).
- The state prices are recovered from two options of different strikes, since the stock and the bond span only the mean of the payoff, not the two states separately.
- The state prices equal the physical probabilities weighted by the SDF and divided by $R$, so recovering them requires an estimate of $m$ that the tree obtains from the stock's drift.
<!-- YW5zOjA= -->
> Two traded assets, two states, two equations: the bond prices the sum of the states ($1/R$) and the stock prices the payoff-weighted sum ($S_0$). Solving gives $q_u=(R-d)/[R(u-d)]$ and $q_d=(u-R)/[R(u-d)]$, and $C_0=q_uC_u+q_dC_d$ is exactly (8.25). Scaling by the gross rate turns a state price into a risk-neutral probability, $\tilde\pi=R_{f,t}q$ (1.16). So the binomial model contains nothing new: it is Chapter 1's state pricing in a two-state economy.
> Ref: Ribeiro (2026), Ch. 8, §8.8.2 (p. 287); §1.4, §1.7
> Similar: Ribeiro, True/False 18, 22 (pp. 296–297)

## rn

Q: Under CRR calibration, $u=e^{\sigma\sqrt{\Delta t}}$, $d=1/u$, and the Black–Scholes price of the Example 8.5 call is 10.4506, while the binomial prices are 10.52 at $N=25$, 10.41 at 50, 10.43 at 100 and 10.44 at 200. What do the calibration and the sequence show?
- The factors are chosen to match the stock's expected return, and the oscillation reflects the sampling error of the tree, which vanishes at the rate $1/\sqrt{N}$ as steps are added.
- The factors are chosen to match $\sigma$, so the drift never enters; the sequence oscillates because even and odd $N$ straddle the strike, with the envelope narrowing as $1/N$.
- The factors are chosen to match $\sigma$ and the drift jointly, which is why the binomial price approaches the limit from above whenever the option is at the money.
- The factors are chosen to match the risk-neutral mean of the terminal price, so the tree converges monotonically once $N$ exceeds the number of periods to expiry.
<!-- YW5zOjE= -->
> CRR sets the factors from $\sigma$ alone, so only volatility and $r$ (through $q$) enter the price: two economies with the same volatility and wildly different expected stock returns price the option identically, because the underlying's price already embeds its expected return. The convergence is honest rather than monotone: whether a node lands near the strike depends on the parity of $N$, so even and odd counts straddle the limit while the envelope narrows roughly as $1/N$.
> Ref: Ribeiro (2026), Ch. 8, §8.8.3 (p. 288), §8.9.2 (pp. 290–291), Figure 8.7
> Similar: Ribeiro, Problem 8.8(c),(d) (p. 296); True/False 26 (p. 297)

Q: The risk-neutral measure is $\tilde\pi(s)=m(s)\pi(s)/E_t[m_{t+1}]$, and pricing becomes $p_t=\tilde E_t[x_{t+1}]/R_{f,t}$. Which pair of claims about it is the chapter's?
- It absorbs the risk adjustment into the probabilities and is the market's best forecast of outcomes, which is why $\Phi(d_2)$ in Black–Scholes is the probability of exercise.
- It absorbs the risk adjustment into the probabilities, and it assigns positive weight to states the physical measure rules out, which is what makes disaster insurance expensive.
- It moves the risk adjustment out of $\mathrm{cov}(m,x)$ and into the probabilities, and it is deliberately pessimistic about the feared states, so it is never a forecast.
- It moves the risk adjustment into the discount rate, which is why the risk-free rate appears; the distortion of the probabilities is a normalization with no economic content.
<!-- YW5zOjI= -->
> Reweighting by $m$ overweights high-marginal-utility states, so everything the covariance term carried is now inside the probabilities and discounting happens at $R_{f,t}$. Two warnings follow. It is not a forecast: using $\tilde\pi$ to predict outcomes systematically overweights disasters, which is exactly what makes it right for pricing and wrong for forecasting — so $\Phi(d_2)$ is the risk-neutral, not the physical, probability of exercise. And the measures agree on which states are possible, differing only in weights, with ratio $m/E_t[m]$.
> Ref: Ribeiro (2026), Ch. 8, §8.9.1 (pp. 289–290), eqs. (8.26)–(8.27)
> Similar: Ribeiro, Problem 8.8(b) (p. 296); True/False 30 (p. 297)
