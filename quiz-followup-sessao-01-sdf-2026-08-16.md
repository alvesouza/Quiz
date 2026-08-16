---
quiz: "Follow-up — Session 1: the four confusions (after 12/30)"
tags:
  ladder: "A · The Ladder of Assumptions"
  covsign: "B · The Sign of cov(m,x)"
  measures: "C · Physical vs. Risk-Neutral"
  record: "D · Statistics of the Historical Record"
---

## ladder

Q: A payoff space is closed under portfolio formation and the law of one price holds. Nothing further is assumed. What follows about the pricing functional?
- It is well defined only on replicable payoffs, and $p(\cdot)$ stays undefined for any $x$ outside the span.
- It is linear and strictly positive, since a linear $p(\cdot)$ cannot price a nonnegative $x\ge 0$ below zero.
- It is concave, because the curvature of $p(\cdot)$ encodes the risk aversion of the agents in equilibrium.
- It is linear, hence representable as $E[m\,x]$ for some $m$; nothing yet forces $m$ to be positive.
<!-- YW5zOjM= -->
> Law of one price $\Rightarrow$ linearity $\Rightarrow$ representation as an inner product, i.e. as some $m$. Positivity is an extra purchase, bought by no-arbitrage. Concavity belongs to utility, not to the pricing functional — importing it here is importing Session 2 into a purely algebraic result.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Cochrane (2005), §4.1 (p. 62)
> Similar: Ribeiro, Problem 1.3 (p. 37); H&L, Exercise 8.4 (p. 255)

Q: Match each assumption to exactly what it buys.
- Law of one price buys existence of some $m$; no-arbitrage buys the ability to choose $m>0$; completeness buys uniqueness of $m$.
- No-arbitrage buys existence of some $m$; the law of one price buys positivity; completeness buys uniqueness of $m$.
- Completeness buys existence of some $m$; the law of one price buys uniqueness; no-arbitrage buys positivity of $m$.
- The law of one price buys both existence and uniqueness; no-arbitrage buys positivity; completeness adds nothing not already implied.
<!-- YW5zOjA= -->
> The three purchases are distinct and cumulative, and the ladder runs from weakest to strongest assumption. Swapping the first two is the single most common error in this chapter: the law of one price is the *weaker* hypothesis and it already suffices for existence.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Cochrane (2005), §4.1–4.2 (pp. 62–71)
> Similar: Ribeiro, True/False 1–21 (p. 39)

Q: A price system satisfies the law of one price, but a careful search uncovers an arbitrage opportunity. What can be said about $m$?
- No $m$ prices the traded assets, since an arbitrage opportunity destroys the linearity that the representation requires.
- Some $m$ prices every traded asset, but every such $m$ must be negative in at least one state of nature.
- Some strictly positive $m$ exists but is not unique, and the arbitrage shows up precisely as that multiplicity of solutions.
- Some $m$ prices the traded assets and it is necessarily positive, since $m=q/\pi$ and probabilities are always positive.
<!-- YW5zOjE= -->
> Linearity survives — the law of one price is all it needs — so a representation still exists. What fails is positivity: the representation requires some $q(s)<0$, and $m=q/\pi$ inherits that sign. The last option forgets that a *state price* can go negative, which is exactly the signature of arbitrage.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Cochrane (2005), §4.2 (p. 67)
> Similar: Ribeiro, Problem 1.2(d) (p. 37)

Q: In an incomplete market a continuum of valid discount factors exists. Which objects are nonetheless pinned down?
- Nothing is pinned down: incompleteness makes even the prices of traded assets admit a range of admissible values.
- Only the value of $m$ in states of strictly positive physical probability; the multiplicity is confined to null-probability states.
- The prices of all traded assets, and the projection $x^*$ of $m$ onto the payoff space; the discount factors differ by an orthogonal term.
- The discount factor of smallest variance among the strictly positive ones, from which all others follow by rotation inside the payoff space.
<!-- YW5zOjI= -->
> Every valid $m$ can be written $m=x^*+\varepsilon$ with $E[\varepsilon x]=0$ for every traded payoff. The projection is unique and the traded prices never move; the indeterminacy touches only payoffs outside the span. Believing that incompleteness unsettles traded prices is the gravest version of this error.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Cochrane (2005), §4.1 (p. 62)
> Similar: Ribeiro, Problems 1.2(e), 1.8 (pp. 37–38)

Q: The course calls $p=E[m\,x]$ "almost empty." Which statement captures precisely what the equation does and does not impose?
- It imposes that agents maximize expected utility with concave preferences, since only then does the pricing operator come out linear.
- It imposes that some linear functional prices the whole payoff space, and nothing more; without tying $m$ to data there is no content.
- It imposes that markets be complete, since otherwise the payoff space fails to be closed under portfolio formation.
- It imposes that $m$ be measurable with respect to aggregate consumption, which is the restriction that gives it testable content.
<!-- YW5zOjE= -->
> Any arbitrage-free set of prices admits an $m$. Empirical content appears only when a candidate is proposed: consumption in Session 2, the market return in Session 4. Completeness is never what the equation requires — it only decides whether $m$ is unique.
> Ref: Ribeiro (2026), Ch. 1, §1.3 (p. 13); Cochrane (2005), §1.1 (p. 4)
> Similar: Ribeiro, True/False 22–30 (p. 40)

Q: An analyst prices with $y$ while the true discount factor is $m$, and $y$ happens to price the riskless bond correctly. What is the pricing error on a payoff $x$, and when does it vanish?
- $E[y-m]\,E[x]$; it vanishes whenever the means agree, which was already imposed, so no error could ever arise.
- $\sigma(y-m)\,\sigma(x)$; it vanishes only if $y=m$ state by state, so no false candidate can price any payoff at all.
- $[\text{cov}(y,x)-\text{cov}(m,x)]/E[m]$; it vanishes when $y$ is an affine transformation of $m$ with unit coefficient.
- $\text{cov}(y-m,\,x)$; it vanishes throughout the payoff space when $y-m$ is orthogonal to it, i.e. when the projections agree.
<!-- YW5zOjM= -->
> $p_y(x)-p(x)=E[(y-m)x]=\text{cov}(y-m,x)+E[y-m]E[x]$, and matching the riskless asset kills the second term. A candidate that is wrong state by state still prices everything correctly if its projection onto the payoff space coincides.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Campbell (2018), Ch. 4
> Similar: Ribeiro, Problem 1.3(c) (p. 37)

Q: Working only with excess returns, a researcher imposes $0=E[m\,R^e]$ for all of them. What does that condition identify?
- It identifies $m$ completely, provided there are as many linearly independent excess returns as there are states of nature.
- It identifies $m$ only up to a positive multiplicative constant, since the condition is homogeneous of degree one.
- It identifies $E[m]$ but not its dispersion across states, which would require an asset whose observed price is nonzero.
- It identifies nothing whatsoever, since the condition holds trivially for any random variable whose mean is equal to zero.
<!-- YW5zOjE= -->
> If $m$ satisfies the condition then so does $cm$ for every $c>0$. Without an asset of nonzero price — typically the riskless one — neither $E[m]$ nor $R_f$ is identified. That is exactly why tests built on excess returns estimate premia rather than the level of the SDF.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Cochrane (2005), §1.4 (p. 10)
> Similar: Ribeiro, Problem 1.4 (p. 37)

Q: In an incomplete market a non-spanned payoff admits only price bounds. How is each bound constructed?
- The upper bound is the cost of the dearest super-replicating portfolio and the lower bound that of the cheapest sub-replicating one.
- The upper bound is $E[x]/R_f$ and the lower bound is zero; any price in that interval is consistent with the absence of arbitrage.
- The upper bound is the cost of the cheapest super-replicating portfolio and the lower bound that of the dearest sub-replicating one.
- The upper bound is the cost of the dearest sub-replicating portfolio and the lower bound that of the cheapest super-replicating one.
<!-- YW5zOjI= -->
> To super-replicate is to dominate the payoff in every state: the cheapest such portfolio is the ceiling. To sub-replicate is to be dominated: the dearest is the floor. Both come out of a linear program. Swapping "cheapest" and "dearest" is the classic trap.
> Ref: Ribeiro (2026), Ch. 1, §1.4 (p. 16)
> Similar: Ribeiro, Problem 1.8 (p. 38)

Q: A colleague objects that writing $E[R^i]=R_f+\beta_{i,m}\lambda_m$ already presupposes the CAPM. Which reply is correct?
- The colleague is right: the beta representation is the security market line, and the security market line is the CAPM's statement.
- The colleague is partly right: the representation needs $m$ to be strictly positive, and only the CAPM secures that positivity.
- The representation needs complete markets, and it is that hypothesis — not the CAPM — that sustains it in any economy considered.
- The representation rewrites $p=E[mx]$ and holds for every valid $m$; the CAPM enters only by making $m$ linear in the market.
<!-- YW5zOjM= -->
> The beta form is an identity, not a model: $\beta_{i,m}$ varies by asset and $\lambda_m$ is common to all. The CAPM's content lies in asserting $m=a+bR^{mkt}$, which is Session 4. Neither positivity nor completeness is required to write it down.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Cochrane (2005), Ch. 6
> Similar: Ribeiro, True/False 22–30 (p. 40)

P: Three states — boom, normal, recession — with physical probabilities $\pi=(0{,}30;\ 0{,}45;\ 0{,}25)$. A bond paying 1 in every state trades at 0,96; a stock with payoffs $(1{,}50;\ 1{,}00;\ 0{,}60)$ trades at 0,972; a call on the stock struck at 1,00 with payoffs $(0{,}50;\ 0;\ 0)$ trades at 0,12.

Q: Are these three assets enough to complete the market, and why?
- Yes, because three assets are traded in a three-state economy, and matching the count of assets to the count of states is what completeness means.
- Yes, because the payoff matrix formed by the bond, the stock and the call has rank three, so every Arrow–Debreu security is replicable.
- No, because the call is a derivative of the stock and therefore adds no payoff direction that the stock and the bond did not already span.
- No, because completeness additionally requires that a distinct asset pay off in each state and be worthless in the others.
<!-- YW5zOjE= -->
> Completeness is a rank condition, never a headcount. Here the three payoff vectors are linearly independent, so the rank is three and the market is complete. A derivative is redundant only when its payoff already lies in the span — a call struck above the lowest payoff does not.
> Ref: Ribeiro (2026), Ch. 1, §1.4 (p. 16); H&L, Ch. 5 §5.1–5.10 (pp. 119–129)
> Similar: Ribeiro, Problem 1.2(a) (p. 37); D&D 3e, Ch. 9 (p. 247)

Q: Recover the state prices implied by these three assets.
- $q=(0{,}24;\ 0{,}45;\ 0{,}27)$ — solving the linear system whose rows are the payoffs and whose right-hand side is the vector of prices.
- $q=(0{,}30;\ 0{,}45;\ 0{,}25)$ — the state prices coincide with the physical probabilities whenever the market is complete.
- $q=(0{,}25;\ 0{,}469;\ 0{,}281)$ — solving the system and then normalizing the vector so that its three components sum to one.
- $q=(0{,}80;\ 1{,}00;\ 1{,}08)$ — solving the system and then reweighting each component by the physical probability of its state.
<!-- YW5zOjA= -->
> The call gives $0{,}50\,q_1=0{,}12$, so $q_1=0{,}24$; the bond gives $q_1+q_2+q_3=0{,}96$; the stock closes the system at $q_2=0{,}45$, $q_3=0{,}27$. Option C is the risk-neutral measure and option D is the SDF — neither is the state-price vector.
> Ref: Ribeiro (2026), Ch. 1, §1.4 (p. 16)
> Similar: Ribeiro, Problem 1.2(b) (p. 37)

## covsign

Q: From the state prices $q=(0{,}24;\ 0{,}45;\ 0{,}27)$ and $\pi=(0{,}30;\ 0{,}45;\ 0{,}25)$, what are the SDF and the net risk-free rate?
- $m=(0{,}072;\ 0{,}2025;\ 0{,}0675)$ and $R_f-1=4{,}17\%$, multiplying each state price by the probability of its state.
- $m=(0{,}80;\ 1{,}00;\ 1{,}08)$ and $R_f-1=4{,}00\%$, reading the rate as the shortfall of $E[m]$ below one.
- $m=(0{,}24;\ 0{,}45;\ 0{,}27)$ and $R_f-1=4{,}17\%$, since the discount factor is the state-price vector itself.
- $m=(0{,}80;\ 1{,}00;\ 1{,}08)$ and $R_f-1=4{,}17\%$, with $E[m]=0{,}96$ equal to the sum of the state prices.
<!-- YW5zOjM= -->
> $m(s)=q(s)/\pi(s)$ gives $(0{,}80;\,1{,}00;\,1{,}08)$ — low in the boom, high in the recession. $E[m]=\sum_s q(s)=0{,}96$, and $R_f=1/0{,}96=1{,}0417$. The rate is the *reciprocal* of $E[m]$, not its complement: $1-E[m]$ is a different number that happens to look plausible.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Cochrane (2005), §1.1 (p. 4)
> Similar: Ribeiro, Problem 1.4(b) (p. 37)

Q: In the same economy, a contract pays 1 in the recession state and nothing otherwise. What are its price and expected gross return?
- Price 0,27 and expected return $+4{,}17\%$, equal to $R_f$, because the state prices already embed the whole risk correction.
- Price 0,25 and expected return $0\%$, because the competitive premium on an insurance contract equals its expected payout.
- Price 0,27 and expected return $-7{,}41\%$, below $R_f$, because $\text{cov}(m,x)>0$ raises the price above $E[x]/R_f$.
- Price 0,225 and expected return $+11{,}1\%$, above $R_f$, because a claim concentrated in one state is a leveraged position.
<!-- YW5zOjI= -->
> Price $=q_3=0{,}27$; expected payoff $=\pi_3=0{,}25$; hence $E[R]=0{,}25/0{,}27=0{,}926$, i.e. $-7{,}41\%$. Check it the long way: $\text{cov}(m,x)=0{,}27-0{,}96\times0{,}25=+0{,}03$, and $p=E[x]/R_f+\text{cov}(m,x)=0{,}24+0{,}03$. Insurance earning less than $R_f$ is the price of protection, not an anomaly.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 1.5(a) (p. 37)

Q: Two assets have the same expected payoff. Asset A has $\text{cov}(m,x_A)>0$ and asset B has $\text{cov}(m,x_B)<0$. Which comparison holds?
- A is dearer and its expected return exceeds $R_f$, since a high price and a high risk premium always move together.
- A is dearer and its expected return falls below $R_f$; B is cheaper and its expected return exceeds $R_f$.
- A is cheaper, because positive covariance with $m$ signals risk, and risk always requires a discount in the price.
- The two command the same price, since expected payoffs are equal and covariance affects only the variance of realized returns.
<!-- YW5zOjE= -->
> In $p=E[x]/R_f+\text{cov}(m,x)$ the covariance is *added* to the price. With the same expected payoff, a higher price means a lower expected return, since $E[R]=E[x]/p$. A is the insurance-type asset; B is the stock-type asset.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Cochrane (2005), §1.4 (p. 10)
> Similar: Ribeiro, Problem 1.5 (p. 37)

Q: Insurance policies and lottery tickets both carry negative expected returns. In the language of $p=E[mx]$, what separates them?
- Both have $\text{cov}(m,x)>0$ and differ only in magnitude, insurance being the extreme member of one and the same family.
- Insurance has $\text{cov}(m,x)<0$ and the lottery has $\text{cov}(m,x)>0$; the skewness of the payoffs flips the sign of the covariance.
- Insurance pays in high-$m$ states, so $\text{cov}(m,x)>0$ accounts for its high price; the lottery pays where $m$ is low and escapes the model.
- Neither is priced by $p=E[mx]$, since a payoff with negative expected return would violate the absence of arbitrage.
<!-- YW5zOjI= -->
> Insurance is dear because it delivers exactly where scarcity bites — a return below $R_f$ is what protection costs, and the model explains it fully. The lottery delivers where $m$ is low, so the model says it should be cheap, and it is not. That residual is preference for skewness, which lives outside $p=E[mx]$.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Cochrane (2005), §1.4 (p. 10)
> Similar: Ribeiro, Problem 1.5(b) (p. 37)

Q: In the representation $E[R^i]=R_f+\beta_{i,m}\lambda_m$, what is $\lambda_m$ and what is its sign?
- $\lambda_m=\sigma^2(m)/E[m]$, hence positive; assets with positive beta on $m$ earn expected returns above $R_f$.
- $\lambda_m=\sigma(m)/E[m]$, hence positive; it is exactly the right-hand side of the Hansen–Jagannathan bound.
- $\lambda_m=-\sigma^2(m)/E[m]$, hence negative; assets with positive beta on $m$ earn expected returns below $R_f$.
- $\lambda_m=E[m]/\sigma^2(m)$, hence positive; it is the reciprocal of the price of risk and grows when $m$ is barely volatile.
<!-- YW5zOjI= -->
> The price of risk attached to the SDF itself is *negative*: whatever pays more when $m$ is high delivers when you need it most, and pays for that privilege with a lower expected return. Option B substitutes the right-hand side of the HJ bound — a different object, and not even the same power of $\sigma$.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Cochrane (2005), §1.4 (p. 10)
> Similar: Ribeiro, Problem 1.4(c) (p. 37)

Q: The stock above pays $(1{,}50;\ 1{,}00;\ 0{,}60)$ and costs 0,972. Its expected payoff is 1,05. Which reading is right?
- $\text{cov}(m,x)=-0{,}036$, so the stock trades below $E[x]/R_f=1{,}008$ and earns $8{,}0\%$, above $R_f$.
- $\text{cov}(m,x)=+0{,}036$, so the stock trades above $E[x]/R_f=1{,}008$ and earns $8{,}0\%$, above $R_f$.
- $\text{cov}(m,x)=-0{,}036$, so the stock trades below $E[x]/R_f=1{,}008$ and earns $4{,}17\%$, exactly $R_f$.
- $\text{cov}(m,x)=0$, so the stock trades at $E[x]/R_f=1{,}008$ and its premium comes entirely from its own variance.
<!-- YW5zOjA= -->
> $\text{cov}(m,x)=E[mx]-E[m]E[x]=0{,}972-0{,}96\times1{,}05=-0{,}036$. Negative covariance *subtracts* from the price: $1{,}008-0{,}036=0{,}972$. The cheaper price delivers the higher expected return, $1{,}05/0{,}972=1{,}080$. Own variance never enters the pricing equation — only covariance with $m$ does.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Appendix 1.A (p. 32)
> Similar: Ribeiro, Problem 1.4(c) (p. 37)

Q: Suppose $m$ were constant across states. What would happen to expected returns?
- Every asset would earn an expected return equal to $R_f$, since $\text{cov}(m,x)=0$ for every payoff when $m$ does not vary.
- Expected returns would still differ across assets, since $\beta_{i,m}$ is asset-specific even when $m$ is constant.
- No risky asset could trade at all, since the Hansen–Jagannathan bound with $\sigma(m)=0$ would be violated by every one of them.
- Every asset would earn zero, since a constant $m$ performs no discounting and price would equal expected payoff.
<!-- YW5zOjA= -->
> In $p=E[x]/R_f+\text{cov}(m,x)$ a constant $m$ zeroes the second term for every $x$. Risky assets still trade — they simply earn no premium. The bound with $\sigma(m)=0$ forces every Sharpe ratio to zero; it does not forbid trade.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Cochrane (2005), §1.4 (p. 10)
> Similar: Ribeiro, Problem 1.4 (p. 37)

Q: The market's annual Sharpe ratio is 0,47 and $E[m]=0{,}96$. What does the Hansen–Jagannathan bound impose?
- $\sigma(m)\ge 0{,}49$, using $E[m]=R_f=1{,}042$ as the scaling factor on the right-hand side of the inequality.
- $\sigma(m)\le 0{,}45$, since the bound places a ceiling on the volatility of $m$ compatible with observed prices.
- $\sigma(m)\ge 0{,}47$, since the bound restricts the standard deviation of $m$ directly rather than its coefficient of variation.
- $\sigma(m)\ge 0{,}45$, and no traded asset in this economy can display a Sharpe ratio above $\sigma(m)/E[m]$.
<!-- YW5zOjM= -->
> $|E[R^e]|/\sigma(R^e)\le\sigma(m)/E[m]$ gives $\sigma(m)\ge 0{,}47\times 0{,}96\approx 0{,}45$. It is a floor, not a ceiling, and it binds against the *best* Sharpe ratio available. Note that $E[m]$ scales the bound, not $R_f$ — they are reciprocals, not the same number.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25); Cochrane (2005), §4.3.2
> Similar: Ribeiro, Problem 1.6(c) (p. 38)

## measures

Q: With $\pi=(0{,}30;\ 0{,}45;\ 0{,}25)$ and $m=(0{,}80;\ 1{,}00;\ 1{,}08)$, in which states does $\tilde\pi$ exceed $\pi$?
- In no state, since the reweighting preserves $\pi$ whenever $m$ is a monotone function of the traded stock's payoff.
- Only in the recession, since it is the single state in which the payoff of the insurance-type claim is strictly positive.
- In the normal and recession states, where $m>E[m]=0{,}96$: $\tilde\pi$ rises to 0,469 and 0,281 while the boom falls to 0,250.
- In every state, since dividing by $E[m]=0{,}96<1$ raises all three weights and the total rises to roughly 1,042.
<!-- YW5zOjI= -->
> $\tilde\pi(s)>\pi(s)$ if and only if $m(s)>E[m]$. Here $E[m]=0{,}96$, and *both* the normal state ($m=1{,}00$) and the recession ($m=1{,}08$) clear it, so both gain weight while the boom loses it. The weights always sum to one — the $E[m]$ in the denominator is precisely the normalizer.
> Ref: Ribeiro (2026), Ch. 1, §1.7 (p. 29)
> Similar: Ribeiro, Problem 1.4(d) (p. 37)

Q: Which statement about expected returns computed under $\tilde\pi$ is correct?
- $\tilde E[R^i]=R_f$ for every asset, since the reweighting absorbs the premium into each state's weight.
- $\tilde E[R^i]=E[R^i]$ for every asset, since a change of measure preserves the means of all random variables.
- $\tilde E[R^i]>R_f$ for risky assets, since the risk-neutral measure preserves the ranking of assets by premium.
- $\tilde E[R^i]=R_f$ for the riskless asset alone; all others retain their risk premia under any measure whatsoever.
<!-- YW5zOjA= -->
> $p=\tilde E[x]/R_f$ is equivalent to $\tilde E[R^i]=R_f$ for every $i$. Verify on the stock: $\tilde E[x]=0{,}25(1{,}50)+0{,}469(1{,}00)+0{,}281(0{,}60)=1{,}0125$, and $1{,}0125/0{,}972=1{,}0417=R_f$. Hence the name: under $\tilde\pi$ everything behaves as in a risk-neutral economy, without anyone being risk-neutral.
> Ref: Ribeiro (2026), Ch. 1, §1.7 (p. 29)
> Similar: Ribeiro, Problem 1.4(d) (p. 37)

Q: The recession claim above costs 0,27. What do the two measures say about it, and do they agree?
- They agree on the price 0,27 and on the expected return, which is $-7{,}41\%$ under both, since a price determines its return uniquely.
- They agree on the price 0,27; expected returns differ — $-7{,}41\%$ under $\pi$ and exactly $R_f$ under $\tilde\pi$.
- They disagree on the price — 0,27 under $\pi$ and 0,25 under $\tilde\pi$ — which is why the risk correction must be applied only once.
- They agree that the expected return is $R_f$ under both measures, since the absence of arbitrage forces a single expected return.
<!-- YW5zOjE= -->
> Under $\tilde\pi$: $\tilde E[x]=0{,}28125$, and $0{,}28125/1{,}0417=0{,}27$ — the same price. But $\tilde E[R]=0{,}28125/0{,}27=1{,}0417=R_f$, while under $\pi$ the same claim earns $-7{,}41\%$. **The measures never disagree about prices; they disagree only about expected returns.**
> Ref: Ribeiro (2026), Ch. 1, §1.7 (p. 29)
> Similar: Ribeiro, Problem 1.4(d) (p. 37)

Q: Which properties does the reweighting $\tilde\pi(s)=m(s)\pi(s)/E[m]$ guarantee, and under which hypothesis?
- It sums to one by construction and is strictly positive under no-arbitrage; under the law of one price alone it may go negative.
- It sums to one and is strictly positive already under the law of one price; no-arbitrage is needed only for the measure to be unique.
- It sums to $E[m]$ and is positive under no-arbitrage, which is why prices must be discounted by $R_f$ more than once at the end.
- It sums to one only if the market is complete; under incompleteness the reweighting fails to define a probability measure at all.
<!-- YW5zOjA= -->
> $\sum_s\tilde\pi(s)=E[m]/E[m]=1$ always — summing to one is free. What no-arbitrage adds is $m>0$, hence $\tilde\pi>0$; without it you would hold weights that sum to one but are not probabilities. Completeness governs uniqueness, nothing here.
> Ref: Ribeiro (2026), Ch. 1, §1.7 (p. 29)
> Similar: Ribeiro, True/False 22–30 (p. 40)

Q: Why is it wrong to read $\tilde\pi$ as the market's best forecast of each state's probability?
- Because $\tilde\pi$ weights each state by the variance of the payoff realized in it, and high variance does not mean high probability.
- Because $\tilde\pi$ holds only until the nearest traded maturity, whereas physical probabilities describe long-run frequencies.
- Because $\tilde\pi$ is computed from past returns, whereas the market forms expectations that look forward.
- Because $\tilde\pi$ is $\pi$ reweighted by scarcity: states with above-average $m$ gain weight, and that is compensation, not information.
<!-- YW5zOjM= -->
> The distortion between $\tilde\pi$ and $\pi$ *is* the risk premium embedded in the price. Reading $\tilde\pi$ as a forecast confuses "how much the market fears the state" with "how likely the market judges it to be."
> Ref: Ribeiro (2026), Ch. 1, §1.7 (p. 29)
> Similar: Ribeiro, True/False 1–21 (p. 39)

Q: Risk-neutral pricing returns in the binomial model and in Black–Scholes. What does Session 1 already settle about the conditions for its validity?
- Existence of $\tilde\pi$ requires payoffs to be lognormal, which is why Black–Scholes needs a continuous diffusion assumption.
- Existence of $\tilde\pi$ requires only no-arbitrage; it is uniqueness — and hence a single option price — that requires completeness.
- Both existence and uniqueness of $\tilde\pi$ require completeness; without it no risk-neutral measure exists in the first place.
- Existence of $\tilde\pi$ requires investors to be risk-neutral, an assumption the binomial model adopts when it discounts at $R_f$.
<!-- YW5zOjE= -->
> It is the existence/uniqueness pair of §1.5 translated into the language of measures. In the binomial model dynamic replication completes the market at every node, and only for that reason does the option carry a single price rather than an interval. Nobody needs to be risk-neutral, and lognormality is not what makes the measure exist.
> Ref: Ribeiro (2026), Ch. 1, §1.7 (p. 29); Ch. 8, §8.6
> Similar: Ribeiro, Problems 8.7–8.8 (p. 293); H&L, Ch. 8 (p. 223)

## record

P: A series of monthly excess market returns covers $T=1200$ months, with a sample mean of $0{,}65\%$ per month and a sample standard deviation of $4{,}80\%$ per month. Treat returns as i.i.d. and use the course's annualization conventions.

Q: What is the standard error of the annualized premium, and what would happen to it on daily data over the same century?
- About 4,80 percentage points per year; moving to daily data over the same span would shrink it by a factor close to 21.
- About 1,66 percentage points per year; moving to daily data over the same span would shrink it in proportion to the gain in estimating $\sigma$.
- About 0,14 percentage point per year; moving to daily data over the same span would shrink it further by a factor of about $\sqrt{21}$.
- About 1,66 percentage points per year; moving to daily data over the same span would not shrink it, since it depends on the sample span.
<!-- YW5zOjM= -->
> $\text{SE}=4{,}80/\sqrt{1200}=0{,}1386\%$ monthly, or $1{,}66\%$ annualized. Slicing the same calendar span more finely divides the per-period mean by $k$ and the per-period volatility by $\sqrt{k}$, and the two cancel. Finer sampling sharpens $\sigma$ and does nothing for the mean, which depends only on how much calendar time you observed.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5); BKM 13e, §5.6 (p. 143)
> Similar: Ribeiro, Problem 1.6(b) (p. 38)

Q: What is the implied annualized geometric mean, and how does it compare with the arithmetic mean?
- About 7,8% per year, equal to the arithmetic mean, because returns were assumed independent and identically distributed.
- About 6,4% per year, below the arithmetic mean, because volatility drag subtracts roughly $\sigma^2/2$ from it.
- About 9,2% per year, above the arithmetic mean, because compounding accumulates the gains over the investment horizon.
- About 4,8% per year, below the arithmetic mean, because volatility drag subtracts the whole variance $\sigma^2$ from it.
<!-- YW5zOjE= -->
> $\mu_a=12\times0{,}65\%=7{,}8\%$ and $\sigma=4{,}80\%\times\sqrt{12}=16{,}63\%$, so $\mu_g\approx7{,}8-0{,}1663^2/2=7{,}8-1{,}38\approx6{,}4\%$. I.i.d. concerns independence *across time* and says nothing about variance being zero; drag depends only on variance. The geometric mean is always the smaller of the two.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5); BKM 13e, §5.1 (p. 126)
> Similar: Ribeiro, Problems 1.1(d), 1.7(c) (pp. 36, 38)

Q: Judged against the hypothesis of a zero premium, how should this estimate be described?
- Statistically detectable and precisely measured: with $t\approx4{,}7$ the premium is pinned down to within a few tenths of a point.
- Neither detectable nor precisely measured: with a standard error of that size the premium cannot be distinguished from zero.
- Statistically detectable but imprecisely measured: $t\approx4{,}7$ clears any usual bar, yet the 95% interval spans roughly ±3,3 points.
- Not detectable but precisely measured: the point estimate is sharp, though the t-statistic falls short of conventional thresholds.
<!-- YW5zOjI= -->
> $t=0{,}65/0{,}1386\approx4{,}7$, so a zero premium is rejected comfortably. Yet $\pm1{,}96\times1{,}66\approx\pm3{,}3$ points around 7,8% leaves an interval running from roughly 4,5% to 11,1%. Detectability and precision are separate claims, and the chapter asks you to keep them apart.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5); BKM 13e, §5.6 (p. 143)
> Similar: Ribeiro, Problem 1.6(b) (p. 38)

P:

Q: An analyst proposes estimating the premium from the last ten years alone, "because markets have changed." What is the statistical cost?
- The standard error rises to roughly 5,3 points per year, so the estimate buys a possible reduction in bias at a steep cost in variance.
- The standard error is unchanged at roughly 1,66 points per year, since it depends on the number of observations rather than the span.
- The standard error falls, because a shorter and more homogeneous window removes the noise contributed by unrepresentative decades.
- The standard error rises to roughly 5,3 points per year, but this is offset because a shorter window mechanically lowers $\sigma$ as well.
<!-- YW5zOjA= -->
> Over 120 months, $\text{SE}=4{,}80/\sqrt{120}=0{,}438\%$ monthly, or about $5{,}3\%$ annualized — three times worse than the century estimate. The trade is real but brutally priced: you swap a bias you cannot measure for noise you can. Nothing forces $\sigma$ to fall on a shorter window.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5); BKM 13e, §5.6 (p. 143)
> Similar: Ribeiro, Problem 1.6(d) (p. 38)

Q: Why does ranking asset classes by risk premium differ from ranking them by Sharpe ratio?
- The premium is estimated with standard error and the Sharpe ratio without any; the gap is sampling noise and vanishes as the span grows.
- The premium uses arithmetic means and the Sharpe ratio geometric ones; the gap is volatility drag and vanishes under i.i.d. returns.
- The premium is measured in nominal terms and the Sharpe ratio in real terms; the gap reflects inflation and vanishes on deflating both.
- The premium rewards the quantity of risk and the Sharpe ratio rewards per unit of risk; only the second is invariant to leverage.
<!-- YW5zOjM= -->
> Levering an asset multiplies premium and volatility by the same factor: the premium climbs, the Sharpe ratio does not budge. That is why small stocks can lead on premium without leading on Sharpe — the extra premium compensates risk that diversification would otherwise remove.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5); BKM 13e, §5.7 (p. 147)
> Similar: Ribeiro, Problem 1.7(d) (p. 38); BKM, Ch. 5 Problem Sets (p. 161)

Q: Following Dimson, Marsh and Staunton, what is the bias in estimating the equity premium from US data alone, and what does it do to the Hansen–Jagannathan bound?
- The US was among the century's most successful markets, so the premium is overstated and the bound comes out more demanding than warranted.
- The US suffered market closures in both world wars, so the premium is understated and the resulting bound is less demanding than it should be.
- The US has the longest available series, so its premium is the most precisely estimated and the bound computed from it is the most reliable.
- The US had above-average inflation, so the nominal premium is inflated; deflating the series removes the bias and leaves the bound unchanged.
<!-- YW5zOjA= -->
> It is survivorship bias at the level of countries: the sixteen markets in Dimson show lower premia outside the US. Since the bound reads $\sigma(m)/E[m]\ge$ Sharpe, an inflated Sharpe ratio demands a more volatile $m$ than the world actually requires — which sharpens the Session 2 puzzle artificially.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5); Dimson, Marsh & Staunton, *Triumph of the Optimists*
> Similar: Ribeiro, Problem 1.6 (p. 38)
