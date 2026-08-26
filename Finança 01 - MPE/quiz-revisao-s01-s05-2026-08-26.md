---
quiz: "Cumulative Review — Sessions 1 to 5"
tags:
  s1: "S1 · Prices, Payoffs and the Discount Factor"
  s2: "S2 · The Consumption-Based SDF"
  s3: "S3 · Markowitz and the Frontier"
  s4: "S4 · The CAPM as a Special SDF"
  s5: "S5 · Factor Models for Risk"
---

## s1

Q: A payoff space is closed under portfolio formation and the law of one price holds, with nothing further assumed. What follows?
- Some $m$ exists with $p=E[mx]$, and it is unique, since linearity pins the representation down completely.
- Some strictly positive $m$ exists, because a linear functional cannot price a nonnegative payoff below zero.
- Some $m$ exists with $p=E[mx]$, but nothing yet guarantees that it is positive in every state.
- No $m$ exists until the market is complete, since the representation needs the payoff space to be spanned.
<!-- YW5zOjI= -->
> Law of one price gives linearity, and linearity gives a representation as an inner product — that is existence. Positivity is bought separately, by no-arbitrage; uniqueness by completeness. The three purchases are distinct and cumulative.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Cochrane (2005), §4.1 (p. 62)
> Similar: Ribeiro, Problem 1.3 (p. 37)

Q: A price system respects the law of one price yet admits an arbitrage. What can be said about $m$?
- Some strictly positive $m$ exists but is not unique, and the arbitrage is that multiplicity.
- No $m$ prices the traded assets, since arbitrage destroys the linearity the representation needs.
- Some $m$ prices every traded asset, but any such $m$ goes negative in at least one state.
- Some $m$ exists and is necessarily positive, since $m=q/\pi$ and probabilities are positive.
<!-- YW5zOjI= -->
> Linearity survives, so a representation exists; what fails is positivity, because the representation needs some $q(s)<0$ and $m=q/\pi$ inherits the sign. State prices *can* go negative — that is precisely the signature of arbitrage.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22); Cochrane (2005), §4.2 (p. 67)
> Similar: Ribeiro, Problem 1.2(d) (p. 37)

Q: In an incomplete market many discount factors price the traded assets. What is nonetheless pinned down?
- The prices of all traded assets, and the projection $x^*$ of $m$ onto the payoff space.
- The value of $m$ wherever physical probability is positive, the freedom sitting in null states.
- Nothing: incompleteness makes even traded assets admit a range of prices.
- The lowest-variance discount factor, the others following from it by rotation in the span.
<!-- YW5zOjA= -->
> Every valid $m$ can be written $m=x^*+\varepsilon$ with $E[\varepsilon x]=0$ for each traded payoff. Traded prices never move; the indeterminacy touches only payoffs outside the span.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22)
> Similar: Ribeiro, Problems 1.2(e), 1.8 (pp. 37–38)

P: Three states — boom, normal, recession — with physical probabilities $\pi=(0{,}30;\ 0{,}45;\ 0{,}25)$ and state prices $q=(0{,}24;\ 0{,}45;\ 0{,}27)$.

Q: What are the state-by-state discount factor and the net risk-free rate?
- $m=(0{,}80;\ 1{,}00;\ 1{,}08)$ and $R_f-1=4{,}00\%$, reading the rate as the shortfall of $E[m]$ below one.
- $m=(0{,}24;\ 0{,}45;\ 0{,}27)$ and $R_f-1=4{,}17\%$, since the discount factor is the state-price vector.
- $m=(0{,}80;\ 1{,}00;\ 1{,}08)$ and $R_f-1=4{,}17\%$, with $E[m]=0{,}96$ equal to the sum of the state prices.
- $m=(0{,}072;\ 0{,}2025;\ 0{,}0675)$ and $R_f-1=4{,}17\%$, weighting each state price by its probability.
<!-- YW5zOjI= -->
> $m(s)=q(s)/\pi(s)$ gives $(0{,}80;\,1{,}00;\,1{,}08)$ — low in the boom, high in the recession. $E[m]=\sum_s q(s)=0{,}96$ and $R_f=1/0{,}96=1{,}0417$. The rate is the **reciprocal** of $E[m]$, never its complement.
> Ref: Ribeiro (2026), Ch. 1, §1.5 (p. 22)
> Similar: Ribeiro, Problem 1.4(b) (p. 37)

Q: In that same economy a contract pays 1 only in the recession. What are its price and expected gross return?
- Price 0,27 and expected return $-7{,}41\%$, below $R_f$, because $\text{cov}(m,x)>0$ lifts the price.
- Price 0,27 and expected return $+4{,}17\%$, equal to $R_f$, since state prices embed the whole risk correction.
- Price 0,25 and expected return $0\%$, since a competitive insurance premium equals the expected payout.
- Price 0,225 and expected return $+11{,}1\%$, since a claim on a single state is a leveraged position.
<!-- YW5zOjA= -->
> Price $=q_3=0{,}27$; expected payoff $=\pi_3=0{,}25$; so $E[R]=0{,}25/0{,}27=-7{,}41\%$. Insurance earns below $R_f$ because it pays where $m$ is high — the price of protection, not an anomaly.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 1.5(a) (p. 37)

Q: Under the risk-neutral measure $\tilde\pi$, what does a risky asset earn?
- The same as under $\pi$, since a change of measure preserves the means of random variables.
- More than $R_f$, since the change of measure preserves the ranking of assets by premium.
- Exactly $R_f$, for every asset, since the reweighting absorbs the premium into each state's weight.
- Exactly $R_f$ for the riskless asset only, all others keeping their premia under any measure.
<!-- YW5zOjI= -->
> $p=\tilde E[x]/R_f$ is equivalent to $\tilde E[R^i]=R_f$ for every $i$. Under $\tilde\pi$ everything behaves as in a risk-neutral economy, without anyone being risk-neutral — the premium moved into the weights.
> Ref: Ribeiro (2026), Ch. 1, §1.7 (p. 29)
> Similar: Ribeiro, Problem 1.4(d) (p. 37)

P:

Q: Two assets share an expected payoff. One has $\text{cov}(m,x)>0$, the other $\text{cov}(m,x)<0$. Which is dearer, and which earns more?
- The positive-covariance asset is dearer and earns below $R_f$; the other is cheaper and earns above.
- The two cost the same, since expected payoffs are equal and covariance moves only realized variance.
- The positive-covariance asset is cheaper, since covariance with $m$ signals risk and risk is discounted.
- The positive-covariance asset is dearer and earns above $R_f$, price and premium moving together.
<!-- YW5zOjA= -->
> $p=E[x]/R_f+\text{cov}(m,x)$: the covariance is **added** to the price. Same expected payoff at a higher price means a lower expected return. The first is the insurance-type asset, the second the stock-type.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 1.5 (p. 37)

Q: In $E[R^i]=R_f+\beta_{i,m}\lambda_m$, what is $\lambda_m$ and what is its sign?
- $\lambda_m=\sigma(m)/E[m]$, positive, being exactly the right-hand side of the Hansen–Jagannathan bound.
- $\lambda_m=-\sigma^2(m)/E[m]$, negative, so assets with positive beta on $m$ earn below $R_f$.
- $\lambda_m=E[m]/\sigma^2(m)$, positive, the reciprocal of the price of risk.
- $\lambda_m=\sigma^2(m)/E[m]$, positive, so assets with positive beta on $m$ earn above $R_f$.
<!-- YW5zOjE= -->
> The price of risk on the discount factor is negative: whatever pays more when $m$ is high delivers when you need it most, and pays for that with a lower expected return. The first option substitutes the bound's right-hand side — a different object.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 1.4(c) (p. 37)

Q: A colleague says writing $E[R^i]=R_f+\beta_{i,m}\lambda_m$ already assumes the CAPM. What is the right reply?
- He is right: the beta representation is the security market line, which is the CAPM.
- It rewrites $p=E[mx]$ and holds for every valid $m$; the CAPM enters only by making $m$ linear in the market.
- The representation needs complete markets, and it is that hypothesis rather than the CAPM that sustains it.
- He is partly right: the representation needs $m>0$, and only the CAPM secures positivity.
<!-- YW5zOjE= -->
> The beta form is an identity, not a model: $\beta_{i,m}$ varies by asset and $\lambda_m$ is common to all. The CAPM's content is asserting $m=a+bR^{mkt}$, which is Session 4.
> Ref: Ribeiro (2026), Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, True/False 22–30 (p. 40)

Q: A century of monthly data gives a standard error of about 1,8 points on the annualized equity premium. What would daily sampling over the same century do?
- Shrink it by roughly $\sqrt{21}$, since twenty-one times as many observations enter the mean.
- Shrink it in proportion to the improvement in the estimate of volatility.
- Leave it unchanged, since the precision of a mean depends on the calendar span, not the frequency.
- Shrink it by roughly 21, since the standard error falls linearly in the number of observations.
<!-- YW5zOjI= -->
> Slicing the same span into $k$ times more periods divides the per-period mean by $k$ and its volatility by $\sqrt k$; the two cancel. Finer sampling sharpens $\sigma$ and does nothing for the mean.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5); BKM 13e, §5.6 (p. 143)
> Similar: Ribeiro, Problem 1.6(b) (p. 38)

Q: With an arithmetic mean of 7,8% and volatility of 16,6%, what is the geometric mean, and why?
- About 7,8%, equal to the arithmetic mean, because returns are assumed independent over time.
- About 6,4%, below it, because volatility drag subtracts roughly $\sigma^2/2$.
- About 9,2%, above it, because compounding accumulates gains across the horizon.
- About 4,8%, below it, because volatility drag subtracts the whole variance $\sigma^2$.
<!-- YW5zOjE= -->
> $\mu_g\approx\mu_a-\sigma^2/2=7{,}8-0{,}166^2/2\approx6{,}4\%$. I.i.d. concerns independence across time and says nothing about variance being zero; drag depends only on variance.
> Ref: Ribeiro (2026), Ch. 1, §1.2 (p. 5)
> Similar: Ribeiro, Problems 1.1(d), 1.7(c) (pp. 36, 38)

Q: For a non-spanned payoff in an incomplete market, how are the price bounds built?
- Upper is the dearest super-replicating portfolio, lower the cheapest sub-replicating one.
- Upper is $E[x]/R_f$ and lower is zero, any price between being arbitrage-free.
- Upper is the dearest sub-replicating portfolio, lower the cheapest super-replicating one.
- Upper is the cheapest super-replicating portfolio, lower the dearest sub-replicating one.
<!-- YW5zOjM= -->
> Super-replicating dominates the payoff in every state, so the **cheapest** such portfolio is the ceiling; sub-replicating is dominated, so the **dearest** is the floor. Both come out of a linear program.
> Ref: Ribeiro (2026), Ch. 1, §1.4 (p. 16)
> Similar: Ribeiro, Problem 1.8 (p. 38)

## s2

Q: Where does the consumption-based discount factor come from?
- From the law of one price, which forces the discount factor to depend on aggregate consumption.
- From the consumer's first-order condition for optimal saving — the intertemporal Euler equation.
- From market clearing among mean-variance optimizers, which makes consumption the numeraire.
- From the assumption of complete markets, under which consumption is the only priced state variable.
<!-- YW5zOjE= -->
> An investor trading off consuming a unit today against investing it delivers $p_t u'(c_t)=E_t[\beta u'(c_{t+1})x_{t+1}]$, so $m_{t+1}=\beta u'(c_{t+1})/u'(c_t)$. It is a statement about preferences and optimization, not about market structure.
> Ref: Ribeiro (2026), Ch. 2, §2.1 (p. 42); Cochrane (2005), §1.1 (p. 4)
> Similar: Ribeiro, Problem 2.1 (p. 72)

Q: Under power utility, what is the discount factor, and what does $\gamma$ control?
- $m=\beta(c_{t+1}/c_t)^{\gamma}$, where $\gamma$ is relative risk aversion, rising consumption raising the discount factor.
- $m=\beta(c_{t+1}/c_t)^{-\gamma}$, where $\gamma$ is relative risk aversion and the reciprocal of substitution.
- $m=\beta\,\gamma\,(c_{t+1}-c_t)$, where $\gamma$ scales the absolute change in consumption between the two dates.
- $m=\beta\exp(-\gamma c_{t+1})$, where $\gamma$ is absolute rather than relative risk aversion.
<!-- YW5zOjE= -->
> With $u(c)=c^{1-\gamma}/(1-\gamma)$, $u'(c)=c^{-\gamma}$, so $m=\beta(c_{t+1}/c_t)^{-\gamma}$. The **negative** exponent matters: consumption growth makes a marginal unit worth *less*. That one parameter carries both risk aversion and intertemporal substitution — a limitation the course notes rather than fixes.
> Ref: Ribeiro (2026), Ch. 2, §2.2 (p. 47)
> Similar: Ribeiro, Problem 2.2 (p. 72)

Q: What does the consumption beta representation say a risk premium is proportional to?
- The covariance of the asset's return with consumption growth.
- The variance of the asset's own return, scaled by risk aversion.
- The correlation between the asset's return and the market return.
- The variance of consumption growth, common across all assets.
<!-- YW5zOjA= -->
> $E[R^i]-R_f\approx\gamma\,\text{cov}(R^i,\Delta\ln c)$. An asset paying badly when consumption is already low is genuinely painful and must offer a premium; own variance is irrelevant except through that covariance.
> Ref: Ribeiro (2026), Ch. 2, §2.3 (p. 51)
> Similar: Ribeiro, Problem 2.4 (p. 72)

P: Aggregate consumption growth has volatility about 1% a year. The market's Sharpe ratio is about 0,30.

Q: What level of risk aversion does the Hansen–Jagannathan bound then require under power utility?
- About 30, since $\sigma(m)/E[m]\approx\gamma\,\sigma(\Delta\ln c)$ must clear the Sharpe ratio.
- About 0,3, since the bound divides the Sharpe ratio by $\sigma(m)$ rather than multiplying.
- About 3, since $\gamma$ scales with the premium over consumption volatility directly.
- About 300, since the bound compares the squared Sharpe ratio with $\sigma^2(\Delta\ln c)$.
<!-- YW5zOjA= -->
> $\gamma\ge 0{,}30/0{,}01=30$. Values of that size imply absurd behaviour elsewhere — indifference between a certain sum and a coin flip over trivial stakes — which is the puzzle in one line.
> Ref: Ribeiro (2026), Ch. 2, §2.4 (p. 55), §2.5 (p. 64); Mehra–Prescott (1985)
> Similar: Ribeiro, Problem 2.3 (p. 71)

Q: In that same setting, what exactly is the equity premium puzzle?
- The premium is measured with too much error for the model to be tested at all.
- The equity premium is too small to be consistent with any positive level of risk aversion.
- Consumption growth is too volatile, so the model predicts a far larger premium than observed.
- Consumption growth is too smooth to generate the observed premium at plausible risk aversion.
<!-- YW5zOjM= -->
> The model needs $m$ volatile enough to clear the bound, and $m$ inherits its volatility from consumption growth. Consumption is far smoother than returns, so only an implausible $\gamma$ closes the gap. Sampling error is a real caveat but not the puzzle.
> Ref: Ribeiro (2026), Ch. 2, §2.4 (p. 55); Campbell (2018), Ch. 6
> Similar: Ribeiro, Problem 2.3 (p. 71)

Q: What does the Hansen–Jagannathan bound restrict, and in which direction?
- It caps $\sigma(m)/E[m]$ above by the highest Sharpe ratio available in the economy.
- It fixes $\sigma(m)/E[m]$ exactly at the market's Sharpe ratio in any economy without arbitrage.
- It bounds $\sigma(m)$ below by the market premium, independently of $E[m]$.
- It bounds $\sigma(m)/E[m]$ below by the highest Sharpe ratio available in the economy.
<!-- YW5zOjM= -->
> $|E[R^e]|/\sigma(R^e)\le\sigma(m)/E[m]$ is a **floor** on the volatility of the discount factor, and it binds against the *best* Sharpe ratio available. It becomes an equality only in special cases, such as the CAPM economy of chapter 4.
> Ref: Ribeiro (2026), Ch. 2, §2.5 (p. 64); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problems 2.3 (p. 71), 1.6(c) (p. 38)

Q: A candidate discount factor reproduces the market's Sharpe ratio but is built from a variable nobody consumes. Is that a problem for the theory of chapter 2?
- No: chapter 2 asks only that some $m$ clear the bound, whatever variable happens to generate it in the end.
- No: any variable correlated with consumption growth is equivalent for pricing purposes.
- Yes: the claim names marginal utility of *consumption* as the discount factor; a substitute abandons that.
- Yes: a discount factor not built from consumption violates the law of one price.
<!-- YW5zOjI= -->
> Chapter 1 already guarantees *some* $m$ exists — that is nearly empty. Chapter 2's content is naming a specific, observable candidate and accepting the consequences. Replacing it with a fitted variable buys the bound at the cost of the economics.
> Ref: Ribeiro (2026), Ch. 2, §2.6 (p. 69); §2.1 (p. 42)
> Similar: Ribeiro, True/False 1–30 (pp. 74–76)

Q: What must any valid discount factor look like, according to the closing section of the chapter?
- Perfectly correlated with the market return, which is the only priced source of risk.
- Constant across states, so that the risk-free rate is well defined in every economy.
- Positive and of unit mean, since it must price the riskless asset with no discounting.
- Volatile enough to clear the bound, and low precisely in the states investors most fear.
<!-- YW5zOjM= -->
> The bound forces volatility; the economics of $p=E[x]/R_f+\text{cov}(m,x)$ forces the *timing* — $m$ must be **high** in bad states and low in good ones. Any candidate model has to deliver both, and consumption growth struggles with the first.
> Ref: Ribeiro (2026), Ch. 2, §2.6 (p. 69)
> Similar: Ribeiro, Problem 2.6 (p. 72)

Q: Consumption growth is smooth and the risk-free rate is low and stable. What tension does power utility create between these two facts?
- None: a low risk-free rate is exactly what a smooth consumption path predicts at any $\gamma$.
- A high $\gamma$ lowers the predicted risk-free rate without any limit, which contradicts its observed stability over time.
- The high $\gamma$ needed for the premium implies a strong urge to borrow against growth, forcing a counterfactually high $R_f$.
- A low $\gamma$ is needed for the risk-free rate, and the same low $\gamma$ also delivers the premium.
<!-- YW5zOjI= -->
> This is the risk-free rate puzzle, the companion to the equity premium puzzle. With one parameter doing two jobs, the $\gamma$ that generates enough $\sigma(m)$ simultaneously implies impatience to consume today against a growing future, forcing a counterfactually high $R_f$.
> Ref: Ribeiro (2026), Ch. 2, §2.4 (p. 55); Campbell (2018), Ch. 6
> Similar: Ribeiro, Problem 2.5 (p. 72)

Q: How does the consumption discount factor relate to chapter 1's framework?
- It is a candidate for $m$ inside the same equation, which gives $p=E[mx]$ its content.
- It replaces $p=E[mx]$ with a different pricing equation derived from preferences.
- It holds only in complete markets, whereas $p=E[mx]$ holds generally.
- It applies to consumption claims only, other assets requiring a separate discount factor.
<!-- YW5zOjA= -->
> Chapter 1 says some $m$ exists and is nearly empty; chapter 2 names one. The framework is unchanged — only the candidate is new, and naming a candidate is what makes the theory refutable.
> Ref: Ribeiro (2026), Ch. 2, §2.1 (p. 42); Ch. 1, §1.3 (p. 13)
> Similar: Ribeiro, True/False 1–30 (pp. 74–76)

Q: An asset's return is uncorrelated with consumption growth. What premium does the consumption model assign it?
- A premium proportional to its own variance, since total risk is still borne by the investor.
- A premium equal to the market's, since uncorrelated assets inherit the average.
- Zero premium, so it earns the risk-free rate whatever its own volatility.
- A negative premium, since uncorrelated assets provide diversification and command a fee.
<!-- YW5zOjI= -->
> With $E[R^i]-R_f\approx\gamma\,\text{cov}(R^i,\Delta\ln c)$, zero covariance gives zero premium regardless of $\sigma(R^i)$. It is the same lesson as chapter 1's idiosyncratic risk and chapter 4's beta — only covariance with the pricing variable is paid for.
> Ref: Ribeiro (2026), Ch. 2, §2.3 (p. 51)
> Similar: Ribeiro, Problem 2.4 (p. 72)

Q: What does the consumption-based model contribute that chapter 1 could not?
- A guarantee that $m$ is positive, which the law of one price alone cannot deliver.
- A proof that markets are complete whenever a representative consumer exists.
- An observable, falsifiable candidate for $m$ — which then fails that test.
- A method for computing state prices directly from observed asset prices.
<!-- YW5zOjI= -->
> The contribution is discipline: an $m$ built from data anyone can measure, which can therefore be *rejected*. That it is rejected quantitatively — the puzzles — is the finding, not a failure of the exercise.
> Ref: Ribeiro (2026), Ch. 2, §2.6 (p. 69)
> Similar: Ribeiro, True/False 1–30 (pp. 74–76)

## s3

P: Two risky assets: the first has volatility 0,20, the second 0,30, and their correlation is 0,30.

Q: What is the covariance between them, and what is the variance of an equally weighted portfolio?
- Covariance 0,0180 and portfolio variance 0,0415, so portfolio volatility is 0,2037.
- Covariance 0,3000 and portfolio variance 0,2500, so portfolio volatility is 0,5000.
- Covariance 0,0180 and portfolio variance 0,0650, the simple average of the two variances.
- Covariance 0,0600 and portfolio variance 0,0625, so portfolio volatility is 0,2500.
<!-- YW5zOjA= -->
> $\text{cov}=\rho\sigma_1\sigma_2=0{,}3(0{,}2)(0{,}3)=0{,}018$. Portfolio variance $=0{,}25(0{,}04)+0{,}25(0{,}09)+2(0{,}25)(0{,}018)=0{,}0415$, so $\sigma_p=0{,}2037$ — below the 0,25 average of the two volatilities. That gap is diversification.
> Ref: Ribeiro (2026), Ch. 3, §3.1 (p. 78)
> Similar: Ribeiro, Problem 3.1 (p. 109)

Q: In that same pair, the minimum-variance combination has volatility 0,1867 against a naive average of 0,25. What produced the gain?
- The averaging of expected returns, which lowers exposure to either asset's $\mu$.
- The lower volatility $\sigma_1$ of the first asset, which dominates any combination.
- Imperfect correlation: $\rho<1$ drops volatility below the weighted average.
- The equal weighting $w=0{,}5$, optimal whenever two assets are available.
<!-- YW5zOjI= -->
> Volatilities add linearly only at $\rho=1$. Anything less makes the portfolio's volatility strictly below the weighted average, and the lower the correlation the larger the gain — the entire content of diversification.
> Ref: Ribeiro (2026), Ch. 3, §3.1 (p. 78)
> Similar: Ribeiro, Problem 3.1 (p. 109)

Q: What shape does the minimum-variance frontier of $N$ risky assets take in mean–standard-deviation space, and in mean–variance space?
- A parabola in $(\sigma,E[R])$ and a hyperbola in $(\sigma^2,E[R])$.
- A hyperbola in $(\sigma,E[R])$ and a parabola in $(\sigma^2,E[R])$.
- A straight line in both, since the frontier is generated by two funds.
- An ellipse in $(\sigma,E[R])$ and a straight line in $(\sigma^2,E[R])$.
<!-- YW5zOjE= -->
> With Merton's constants $A$, $B$, $C$, $D$, the relation $\sigma^2=\big(C(E[R])^2-2A\,E[R]+B\big)/D$ is a parabola in variance, and taking square roots turns it into a hyperbola in standard deviation.
> Ref: Ribeiro (2026), Ch. 3, §3.2 (p. 84); H&L, Ch. 3 §3.11 (p. 67)
> Similar: Ribeiro, Problem 3.2 (p. 109)

Q: Two-fund spanning says what about the minimum-variance frontier?
- Two funds span the frontier only when all investors share the same $\gamma$.
- Any two assets generate the frontier, provided their correlation $\rho$ is zero.
- The frontier needs exactly two funds, one at $R_f$ and one risky, and no other build.
- Any two distinct frontier portfolios generate the rest, weights being affine in $E[R]$.
<!-- YW5zOjM= -->
> Because $\mathbf{w}_p$ is affine in $E[\tilde r_p]$, two frontier portfolios at distinct expected returns generate all the rest by combination. This is *spanning*, an algebraic fact — distinct from *separation*, the economic claim that investors choose among two funds.
> Ref: Ribeiro (2026), Ch. 3, §3.2 (p. 84); H&L, Ch. 3 §3.9–3.10 (p. 66)
> Similar: Ribeiro, Problem 3.3 (p. 109)

Q: Adding a risk-free asset changes the efficient set how?
- It shifts the hyperbola up by $R_f$, leaving its shape entirely unchanged.
- It leaves the frontier unchanged, since a riskless asset has $\sigma=0$ to combine.
- It becomes a second hyperbola, tangent to the first at the $\sigma$-minimising point.
- It becomes a straight line from $R_f$ through the tangency portfolio.
<!-- YW5zOjM= -->
> Mixing cash with one risky portfolio traces a straight line in $(\sigma,E[R])$. The steepest such line is tangent to the frontier, and its slope is the tangency portfolio's Sharpe ratio. In equilibrium that line is the capital market line.
> Ref: Ribeiro (2026), Ch. 3, §3.3 (p. 91)
> Similar: Ribeiro, Problem 3.4 (p. 109)

Q: With a risk-free rate of 3%, a market at 9% and market volatility 0,20, what does the capital allocation line assign to a portfolio of volatility 0,35, and does that apply to any asset?
- 13,5%, and it applies to every asset, since the line prices total risk universally.
- 12,0%, and it applies only to efficient portfolios; individual assets use beta instead.
- 13,5%, and it applies only to efficient portfolios; individual assets use beta instead.
- 10,5%, and it applies to every asset, since leverage scales the premium proportionally.
<!-- YW5zOjI= -->
> $1{,}03+0{,}30(0{,}35)=1{,}135$. But the line describes what is *attainable* by mixing cash with the tangency portfolio — efficient portfolios. An inefficient asset with that volatility sits strictly below it and is not mispriced.
> Ref: Ribeiro (2026), Ch. 3, §3.3 (p. 91); Ch. 4, §4.2 (p. 120)
> Similar: Ribeiro, Problems 3.4 (p. 109), 4.1 (p. 146)

Q: What is the frontier–SDF duality of this chapter?
- The minimum-variance portfolio is the projection $x^*$ of $m$ onto the payoff space.
- The tangency portfolio's weights equal the state prices $q$, normalised to sum to one.
- The frontier's curvature equals $\sigma^2(m)$ at every point along its length.
- The maximum attainable Sharpe ratio equals the tightest bound $\sigma(m)/E[m]$.
<!-- YW5zOjM= -->
> The mean–variance frontier of returns and the Hansen–Jagannathan frontier of discount factors are the same object seen from two sides: the best Sharpe ratio available is exactly what the bound must accommodate. Chapter 4 makes it an equality by putting the market at the tangency.
> Ref: Ribeiro (2026), Ch. 3, §3.4 (p. 96); Cochrane (2005), §5.6
> Similar: Ribeiro, Problem 3.5 (p. 109)

Q: What is the error-maximization problem in mean–variance optimisation?
- The optimiser systematically underweights assets whose expected returns are estimated with error.
- The optimiser loads on whatever was most favourably mis-estimated, so error becomes weight.
- The optimiser maximises the variance of the estimation error rather than minimising portfolio variance.
- The optimiser is unbiased in-sample but arbitrary out-of-sample, since weights do not depend on the inputs.
<!-- YW5zOjE= -->
> Feed the optimiser estimates and it treats them as truth, tilting hardest towards whatever looked best — which is disproportionately whatever was over-estimated. The in-sample frontier is therefore optimistic, and the out-of-sample Sharpe ratio drops.
> Ref: Ribeiro (2026), Ch. 3, §3.5 (p. 100)
> Similar: Ribeiro, Problem 3.6 (p. 109)

Q: The Project 1 brief warns that extreme weights and a fall in out-of-sample Sharpe are expected. Why?
- Because the panel is too small for the frontier to be estimated at all.
- Because they are the visible symptoms of error maximization.
- Because survivorship bias in the constituents guarantees the frontier is misplaced.
- Because daily data cannot be annualized without distorting the covariance matrix.
<!-- YW5zOjE= -->
> The brief is explicit that the confrontation between theory and estimated inputs *is* the deliverable. Extreme weights, sign flips and a lower out-of-sample Sharpe are results to show and comment on, not defects to tune away.
> Ref: Ribeiro (2026), Ch. 3, §3.5 (p. 100); `Projetos/Project1_Brief.pdf`
> Similar: Ribeiro, Problem 3.6 (p. 109)

Q: How does the global minimum-variance portfolio differ from the tangency portfolio?
- The tangency portfolio ignores the covariance matrix, depending only on expected returns.
- They coincide whenever a risk-free asset exists, since both maximise the Sharpe ratio.
- The minimum-variance portfolio maximises the Sharpe ratio; the tangency portfolio minimises variance.
- The minimum-variance portfolio ignores expected returns entirely; the tangency portfolio needs them.
<!-- YW5zOjM= -->
> The minimum-variance weights solve $\Sigma w\propto\mathbf{1}$ and need no expected returns at all — which is why they are far more stable out of sample. The tangency portfolio needs $\mu$, the noisiest input there is.
> Ref: Ribeiro (2026), Ch. 3, §3.2 (p. 84), §3.5 (p. 100)
> Similar: Ribeiro, Problem 3.7 (p. 109)

Q: Two portfolios have identical volatility, one on the frontier and one inside it. What distinguishes them?
- Nothing relevant, since volatility is a complete description of a portfolio's risk.
- They differ only in composition, and any investor is indifferent between them.
- The interior one has a higher expected return, being compensated for its inefficiency.
- The interior one earns less at that same volatility, and cannot be improved upon.
<!-- YW5zOjM= -->
> The frontier is defined as minimum variance *for a given* expected return, equivalently maximum expected return for a given variance. An interior portfolio is dominated: the same risk, less reward.
> Ref: Ribeiro (2026), Ch. 3, §3.2 (p. 84)
> Similar: Ribeiro, Problem 3.2 (p. 109)

Q: Why is the covariance matrix a more reliable input than the vector of expected returns?
- Because covariances are estimated from more observations, means requiring the whole calendar span.
- Because second moments converge with sampling frequency while means depend only on span.
- Because covariances are bounded and means are not, so estimation error cannot accumulate.
- Because the optimiser is insensitive to the covariance matrix but highly sensitive to means.
<!-- YW5zOjE= -->
> Sampling more finely genuinely sharpens second moments; it does nothing for a mean, whose precision depends on calendar span alone. That asymmetry — the same one behind chapter 1's standard-error result — is why minimum-variance portfolios travel better than tangency ones.
> Ref: Ribeiro (2026), Ch. 3, §3.5 (p. 100); Ch. 1, §1.2 (p. 5)
> Similar: Ribeiro, Problems 3.6 (p. 109), 1.6(b) (p. 38)

## s4

P: A risk-free rate of 3%, a market with expected gross return 1,09 and volatility 0,20. Asset A has beta 1,5 and total volatility 0,35.

Q: What is the market's Sharpe ratio here?
- 0,30, dividing the market's excess return of 6 points by its volatility of 0,20.
- 0,45, dividing the market's gross return of 9% by its volatility of 0,20.
- 0,06, which is the premium itself expressed as a decimal fraction.
- 0,20, which is the market volatility, the premium cancelling in the ratio.
<!-- YW5zOjA= -->
> $(1{,}09-1{,}03)/0{,}20=0{,}30$. A Sharpe ratio always uses an **excess** return: it measures reward above the risk-free alternative, not above zero.
> Ref: Ribeiro (2026), Ch. 4, §4.1 (p. 117)
> Similar: Ribeiro, Problem 4.5 (p. 147)

Q: What expected gross return does the CAPM assign asset A, and what does beta multiply?
- 1,090, beta multiplying the market's gross return.
- 1,135, beta multiplying the volatility through the Sharpe ratio.
- 1,120, beta multiplying the market premium of 6 points.
- 1,150, beta multiplying a 10-point premium implied by the Sharpe ratio.
<!-- YW5zOjI= -->
> $1{,}03+1{,}5(0{,}06)=1{,}12$. Beta multiplies the **premium** — never the gross return, never the volatility, never anything derived from the Sharpe ratio.
> Ref: Ribeiro (2026), Ch. 4, §4.2 (p. 120)
> Similar: Ribeiro, Problem 4.1 (p. 146)

Q: Asset A sits on the security market line at 12% but the capital market line at its volatility would demand 13,5%. Is it mispriced?
- Yes: any asset below the capital market line earns less than its risk warrants.
- No: the 1,5-point gap is its idiosyncratic risk, which is diversifiable and unpaid.
- Yes: the two lines must agree for every asset in equilibrium.
- No: the gap is estimation error in beta and vanishes in a longer sample.
<!-- YW5zOjE= -->
> A's systematic volatility is $\beta\sigma_{mkt}=0{,}30$ and its idiosyncratic part $\sqrt{0{,}35^2-0{,}30^2}=0{,}1803$. Feed the systematic part into the capital market line and you get exactly 12% — the two lines are one, read with and without the part nobody pays for.
> Ref: Ribeiro (2026), Ch. 4, §4.2 (p. 120)
> Similar: Ribeiro, Problem 4.1 (p. 146)

Q: Decompose asset A's variance, given beta 1,5, total volatility 0,35 and market volatility 0,20.
- Systematic 0,3000 and idiosyncratic 0,0500, with $R^2=0{,}857$.
- Systematic 0,0900 and idiosyncratic 0,0325, with $R^2=0{,}735$.
- Systematic 0,0600 and idiosyncratic 0,0625, with $R^2=0{,}490$.
- Systematic 0,1225 and idiosyncratic 0,0000, with $R^2=1{,}000$.
<!-- YW5zOjE= -->
> $\text{var}=\beta^2\sigma^2_{mkt}+\text{var}(\varepsilon)$: systematic $2{,}25(0{,}04)=0{,}09$, total $0{,}35^2=0{,}1225$, residual $0{,}0325$, $R^2=0{,}735$. Everything is in **variance** units; 0,30 is a standard deviation and does not belong in this identity. Check: $R^2=\rho^2$ with $\rho=0{,}30/0{,}35=0{,}857$.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129)
> Similar: Ribeiro, Problem 4.3 (p. 147)

Q: Twenty-five assets each carry idiosyncratic variance 0,0325 with uncorrelated residuals. Equally weighted, what is the portfolio's residual risk?
- Variance 0,0325 and volatility 0,180, the portfolio inheriting its constituents' residual variance.
- Variance 0,0065 and volatility 0,081, residual variance falling with the square root of the count.
- Variance 0,0013 and volatility 0,036, independent residuals averaging down with the square of the weight.
- Variance 0,0000 and volatility 0,000, idiosyncratic risk vanishing completely in any large portfolio.
<!-- YW5zOjI= -->
> Independent residuals enter with $w_i^2$, so $0{,}0325/25=0{,}0013$ and volatility $0{,}036$. Variance falls with $N$, volatility with $\sqrt N$, and the systematic block does not fall at all.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129)
> Similar: Ribeiro, Problem 4.3 (p. 147)

Q: With $R_f=1{,}03$, a market premium of 0,06 and market variance 0,04, what is $b$ in $m=a+b\,R_{mkt}$?
- $-1{,}500$, from $-E[R^e_{mkt}]/\sigma^2(R_{mkt})$, with no discounting applied.
- $-1{,}456$, from $-\tfrac{1}{R_f}\,E[R^e_{mkt}]/\sigma^2(R_{mkt})$.
- $+1{,}456$, positive because the market risk premium is itself positive.
- $-0{,}300$, from $-E[R^e_{mkt}]/\sigma(R_{mkt})$, the negative of the Sharpe ratio.
<!-- YW5zOjE= -->
> $-(1/1{,}03)(0{,}06/0{,}04)=-1{,}4563$. Two standard slips: dropping the $1/R_f$ factor, and dividing by $\sigma$ rather than $\sigma^2$. The sign must be negative because $m$ falls as the market rises.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124)
> Similar: Ribeiro, Problem 4.2 (p. 147)

Q: In that economy $\sigma(m)=0{,}2913$ and $E[m]=0{,}9709$. What does the Hansen–Jagannathan bound give?
- $\sigma(m)/E[m]=0{,}30$, comfortably above the market Sharpe ratio, so the bound is slack.
- $\sigma(m)/E[m]=0{,}30$, exactly the market Sharpe ratio, so the bound holds with equality.
- $\sigma(m)/E[m]=0{,}28$, below the market Sharpe ratio, so the CAPM violates the bound here.
- $\sigma(m)/E[m]=0{,}06$, matching the market premium rather than the Sharpe ratio.
<!-- YW5zOjE= -->
> $0{,}2913/0{,}9709=0{,}30$. Equality is forced: the bound binds against the *highest* Sharpe ratio available, and under the CAPM the market is the tangency portfolio, so the market's own ratio is that maximum.
> Ref: Ribeiro (2026), Ch. 4, §4.3 (p. 124); Ch. 1, §1.6 (p. 25)
> Similar: Ribeiro, Problem 4.2 (p. 147)

Q: A researcher regresses excess returns on the market, gets $R^2=0{,}94$, and calls it evidence for the CAPM. What is wrong?
- The index model fits with or without the CAPM, whose content is $\alpha_i=0$.
- The regression should use gross returns, so $\hat\alpha_i$ is not the restricted object.
- Nothing, provided $\beta_i$ is statistically significant at conventional levels.
- The regression estimates $\beta_i$ but not $\alpha_i$, so no intercept restriction is testable.
<!-- YW5zOjA= -->
> $R^2$ measures how much of the *variance* the market explains — the estimation vehicle. The CAPM is an equilibrium restriction on the *intercept*. They are different parts of the same regression, and one says nothing about the other.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129)
> Similar: Ribeiro, Problem 4.4 (p. 147)

Q: An alpha estimate of 2,0 points a year has a standard error of 2,5. What follows?
- The CAPM is rejected here, since $\hat\alpha>0$ is a pricing error the model forbids.
- The CAPM is confirmed, since failing to reject $\alpha=0$ supports the restriction.
- Nothing: $t=0{,}8$, so the estimate is indistinguishable from zero either way.
- The result is uninterpretable, since $\alpha$ needs a cross-sectional regression.
<!-- YW5zOjI= -->
> $t=2{,}0/2{,}5=0{,}8$. Note the symmetry: failing to reject is not confirmation either, since the interval is wide enough to admit economically large alphas. Alpha is perfectly estimable from a time series.
> Ref: Ribeiro (2026), Ch. 4, §4.4 (p. 129)
> Similar: Ribeiro, Problem 4.4 (p. 147)

Q: Remove the risk-free asset from the CAPM economy, changing nothing else. What survives?
- Nothing: without a risk-free rate the tangency portfolio is undefined and no relation can be written.
- The relation survives with the intercept replaced by the expected return on a zero-beta portfolio.
- The relation holds for efficient portfolios alone, individual assets becoming bounded in an interval.
- The relation survives unchanged, since the risk-free asset enters only the capital market line.
<!-- YW5zOjE= -->
> Black's (1972) zero-beta CAPM: $E[R_i]=E[R_z]+\beta_i(E[R_{mkt}]-E[R_z])$, with $R_z$ the minimum-variance portfolio uncorrelated with the market. The frontier never needed a risk-free asset; only the anchor is replaced.
> Ref: Ribeiro (2026), Ch. 4, §4.1 (p. 117); H&L, Ch. 4 (p. 97)
> Similar: Ribeiro, Problem 4.5 (p. 147)

Q: A fitted cross-sectional line has intercept 5,5% against a risk-free rate of 3% and passes through the market at 9%. What alphas does that imply at betas 0,5 and 1,5?
- $+1{,}25$ and $-1{,}25$ points, the fitted slope being 3,5 against the theoretical 6.
- $-1{,}25$ and $+1{,}25$ points, the fitted line being steeper than the theoretical one.
- $+2{,}50$ and $-2{,}50$ points, the intercept exceeding the risk-free rate by 2,5.
- Zero at both, since a line through the market reproduces the CAPM at every beta.
<!-- YW5zOjA= -->
> Fitted slope $=0{,}09-0{,}055=0{,}035$. At $\beta=0{,}5$: 7,25% against 6%, so $+1{,}25$. At $\beta=1{,}5$: 10,75% against 12%, so $-1{,}25$. The lines cross at $\beta=1$. This flatness is what Betting Against Beta trades.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); BKM 13e, §13.1 (p. 410)
> Similar: Ribeiro, Problem 4.6 (p. 148)

Q: Why is any empirical rejection of the CAPM called a joint-hypothesis problem?
- Because the test bundles the model with the estimator's asymptotics, so rejection may be small-sample bias.
- Because the test bundles the model with the assumption of constant betas over the sample.
- Because the test bundles the model with a market proxy and an assumption about expectations.
- Because the test bundles the model with normality, so rejection may reflect fat tails.
<!-- YW5zOjI= -->
> Roll supplies the proxy half — the true market portfolio is unobservable — and Fama the expectations half. A rejection condemns the bundle without naming which component failed. The others are genuine but narrower worries.
> Ref: Ribeiro (2026), Ch. 4, §4.5 (p. 136); Cochrane (2005), §9.3 (p. 167)
> Similar: Ribeiro, True/False 1–30 (pp. 148–149)

## s5

Q: A factor model can be asked to do two jobs. What are they?
- Restrict expected returns, and restrict the level of the risk-free rate.
- Restrict the discount factor, and restrict the preferences of the representative investor.
- Restrict the number of priced factors, and restrict the number of states of nature.
- Restrict the covariance matrix, and restrict the cross-section of expected returns.
<!-- YW5zOjM= -->
> A risk model constrains $\Sigma$ — second moments, chapter 5. A returns model constrains $E[R^e]$ — first moments, chapter 6. Keeping them apart is the chapter's central discipline.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153)
> Similar: Ribeiro, Problem 5.4 (p. 184)

Q: Must a risk model's factors be priced?
- No, since the model claims only that returns co-move through the factors — a second-moment claim.
- Yes, since the covariance matrix is derived from the beta representation of expected returns.
- Yes, since an unpriced factor contributes no variance to portfolios built on the model.
- No, provided the factors are mutually orthogonal, which removes the pricing requirement.
<!-- YW5zOjA= -->
> Pricing is a first-moment claim; co-movement is a second-moment claim. An industry dummy can drive covariance while carrying no premium at all, and it is a perfectly good risk factor.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153)
> Similar: Ribeiro, Problem 5.7 (p. 185)

Q: One analyst says a model failed because implied correlations miss realized ones; another says it failed because assets show systematic alphas. What has each diagnosed?
- Both diagnosed the same failure, alphas and correlation errors being two views of one misspecification.
- Neither diagnosed a failure, both symptoms being artefacts of finite samples.
- The first a failed returns model, the second a failed risk model, the labels being conventionally reversed.
- The first a failed risk model, the second a failed returns model — a model can fail either independently.
<!-- YW5zOjM= -->
> Correlation mismatch condemns the second-moment claim; systematic alphas condemn the first-moment claim. A model can pass one and fail the other, which is why naming the job under test is the discipline.
> Ref: Ribeiro (2026), Ch. 5, §5.1 (p. 153)
> Similar: Ribeiro, Problem 5.4 (p. 184)

P: A single-index risk model with market variance 0,04. Asset A has beta 1,5 and idiosyncratic variance 0,0325; asset B has beta 0,5 and 0,1000; asset C has beta 1,0 and 0,0500. Residuals are uncorrelated.

Q: What is the covariance between A and B, and what is A's total variance?
- Covariance 0,0300 and variance 0,1225, from $\beta_A\beta_B\sigma^2_{mkt}$ and $\beta_A^2\sigma^2_{mkt}+D_A$.
- Covariance 0,0300 and variance 0,0900, from $\beta_A\beta_B\sigma^2_{mkt}$ and the systematic term alone.
- Covariance 0,1225 and variance 0,1525, from the shared market term plus both residual variances.
- Covariance 0,7500 and variance 0,3500, from the product of betas and the root of the summed variances.
<!-- YW5zOjA= -->
> Off-diagonal $1{,}5(0{,}5)(0{,}04)=0{,}03$ — residual terms never enter a covariance here. Diagonal $2{,}25(0{,}04)+0{,}0325=0{,}1225$, so $\sigma_A=0{,}35$, the same asset A as chapter 4.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: Equally weighted across A, B and C, what are the portfolio's beta and total variance?
- Beta 1,0 and variance 0,0603, systematic 0,0400 plus idiosyncratic $0{,}1825/9=0{,}0203$.
- Beta 1,0 and variance 0,1008, systematic 0,0400 plus the average $0{,}1825/3$.
- Beta 1,0 and variance 0,0400, $\text{var}(\varepsilon_p)$ vanishing in any such portfolio.
- Beta 3,0 and variance 0,3600, summing the betas and squaring before $\sigma^2_{mkt}$.
<!-- YW5zOjA= -->
> Residual variances enter with the **square** of the weight: $(1/9)(0{,}0325+0{,}1000+0{,}0500)=0{,}0203$, not their average. Total $0{,}0603$, so $\sigma_p=0{,}2455$. Taking the simple average is the standard slip.
> Ref: Ribeiro (2026), Ch. 5, §5.3 (p. 161)
> Similar: Ribeiro, Problem 5.2 (p. 183)

Q: For 500 assets, how many parameters does an unrestricted covariance matrix need, against a single-index model?
- 250.000 against 500, the full matrix having $N^2$ entries and the model one beta each.
- 125.250 against 501, the model needing one beta per asset plus the market variance.
- 1.000.000 against 1.001, each pair storing both a covariance and a correlation.
- 125.250 against 1.001, the full matrix holding $N(N+1)/2$ entries and the model $2N+1$.
<!-- YW5zOjM= -->
> $500(501)/2=125.250$ against $2(500)+1=1.001$ — 500 betas, 500 residual variances, one market variance. Symmetry means $N(N+1)/2$ distinct entries, never $N^2$.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: What does a diagonal $D$ assert economically, and where does it fail?
- That residuals have equal variance across assets, failing whenever firm sizes differ materially.
- That residuals are normally distributed, failing whenever returns show fat tails.
- That residuals are uncorrelated over time, failing at high sampling frequencies.
- That residuals are uncorrelated, so co-movement runs through the factor; it fails on industry shocks.
<!-- YW5zOjM= -->
> A diagonal $D$ says the factor is the **only** shared driver. Two oil firms move together beyond their market betas, so their residuals correlate and the model understates their joint risk — a testable implication, and the motivation for a second factor.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problems 5.1 (p. 183), 5.3 (p. 184)

Q: Why does the single-index covariance matrix take the form $\beta\beta^\top\sigma^2_{mkt}+D$?
- Because one common source of co-movement makes the systematic part rank one, $D$ carrying the rest.
- Because the market must be mean-variance efficient, which forces the systematic block to rank one.
- Because $\Sigma$ must be invertible, and only a rank-one block guarantees positive definiteness.
- Because OLS residuals are orthogonal, which mechanically produces a rank-one matrix.
<!-- YW5zOjA= -->
> One factor means every pair covaries only through it — exactly a rank-one outer product. $D$ then holds what the factor does not explain. Invertibility is a by-product of $D$ being positive, not the reason for the structure.
> Ref: Ribeiro (2026), Ch. 5, §5.2 (p. 155)
> Similar: Ribeiro, Problem 5.1 (p. 183)

Q: What does adding a second factor do, mechanically?
- It raises the rank of the systematic block, decorrelating those residuals.
- It lowers the parameter count, making the covariance matrix easier to estimate.
- It makes $D$ non-diagonal, which is what lets industry effects enter the model.
- It guarantees that alphas become zero once the second source of premium is accounted for.
<!-- YW5zOjA= -->
> The shared driver is *promoted* out of $D$ into $BFB^\top$, restoring the diagonal assumption. Note it **increases** the parameter count and leaves $D$ diagonal by construction — both of which students routinely reverse.
> Ref: Ribeiro (2026), Ch. 5, §5.4 (p. 167)
> Similar: Ribeiro, Problem 5.3 (p. 184)

Q: For 500 assets and five factors, roughly how many parameters does $\Sigma=BFB^\top+D$ require?
- About 2.500, from the loadings alone, $F$ and $D$ being normalised away.
- About 3.015: 2.500 loadings, 15 entries of $F$, 500 residual variances.
- About 125.250, since any 500-asset model must still specify the full matrix.
- About 505, from 500 residual variances plus five factor variances.
<!-- YW5zOjE= -->
> $B$ is $500\times5=2.500$; $F$ symmetric $5\times5$ gives $15$; $D$ contributes 500. Total 3.015 — a large saving on 125.250, and more than the 1.001 one factor needs.
> Ref: Ribeiro (2026), Ch. 5, §5.4 (p. 167)
> Similar: Ribeiro, Problem 5.3 (p. 184)

Q: Define tracking error against a benchmark, and say what produces it.
- The average absolute return difference, arising from the residual block alone.
- The difference in Sharpe ratios, arising from the factor covariance matrix.
- The volatility of the portfolio itself, the benchmark contributing no variance.
- The volatility of the return difference, from active tilts and residuals alike.
<!-- YW5zOjM= -->
> $\text{TE}=\sigma(R_p-R_b)$, computed on active weights through the same $\Sigma$. A portfolio matching the benchmark's factor exposures exactly can still have tracking error, from stock-specific bets living in $D$.
> Ref: Ribeiro (2026), Ch. 5, §5.5 (p. 173)
> Similar: Ribeiro, Problem 5.6 (p. 185)

Q: Why does a factor-model covariance matrix usually beat the sample one out of sample?
- Because it is unbiased while the sample matrix is not, at any sample size.
- Because bias in a covariance matrix affects the level of variance but never the weights.
- Because it uses more of the data, being estimated from both returns and factor realizations.
- Because the structure it imposes suppresses estimation error in the many off-diagonal entries.
<!-- YW5zOjM= -->
> The sample matrix has $N(N+1)/2$ noisy entries and the optimiser consumes its *inverse*, loading on precisely the worst-estimated ones. The factor model trades a little bias for a large reduction in estimation variance.
> Ref: Ribeiro (2026), Ch. 5, §5.5 (p. 173)
> Similar: Ribeiro, Problem 5.5 (p. 184)

Q: A manager holds a concentrated portfolio and argues she should be paid for its full volatility. What does chapter 5 let you say?
- That she is paid for the systematic part only, residual risk being diversifiable and unpriced.
- That she is paid for total volatility, since her own portfolio is the relevant risk to her.
- That the model splits her risk in two, but not whether either part is paid for.
- That a concentrated portfolio cannot be decomposed, the decomposition needing many holdings.
<!-- YW5zOjI= -->
> This is the chapter's own boundary. A risk model measures and decomposes; it makes **no** claim about what earns a premium. The compensation answer is chapter 6's, and giving it here is exactly the overreach §5.6 warns against — even though the answer happens to be right.
> Ref: Ribeiro (2026), Ch. 5, §5.6 (p. 178)
> Similar: Ribeiro, Problem 5.4 (p. 184)

Q: What does a risk model explicitly not claim?
- That its factors are priced, that alphas are zero, or that expected return follows from exposures.
- That its covariance forecasts are stable over time, the only limitation the chapter records.
- That residual risk exists at all, a complete model leaving nothing outside the factor block.
- That its factors are uncorrelated with one another, which distinguishes it from a returns model.
<!-- YW5zOjA= -->
> Everything a risk model says lives in second moments. Reading a premium off a loading imports a first-moment claim it never made — the same error as treating $R^2$ as evidence for the CAPM, one chapter on.
> Ref: Ribeiro (2026), Ch. 5, §5.6 (p. 178)
> Similar: Ribeiro, Problem 5.4 (p. 184)
