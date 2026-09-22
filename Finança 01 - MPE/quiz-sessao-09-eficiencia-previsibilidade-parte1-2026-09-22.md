---
quiz: "Session 9 — Efficiency, Predictability, and the Capstone, Part 1: Efficiency and the Joint Hypothesis"
tags:
  formas: "1 · The Three Forms and Their Information Sets"
  misreadings: "2 · What Efficiency Does Not Mean"
  conjunta: "3 · The Joint-Hypothesis Problem"
  grossman: "4 · Grossman–Stiglitz and the Degree of Efficiency"
  arbitragem: "5 · Behavioural Biases and the Limits to Arbitrage"
---

## formas

Q: The three forms of the efficient markets hypothesis are said to be nested. What exactly does that nesting assert?
- Each form applies to a different class of asset, so the weak form governs equities, the semi-strong form bonds, and the strong form privately held claims.
- Strong implies semi-strong implies weak, so rejecting the weak form rejects all three of them, while confirming the strong form confirms every one.
- The forms are ordered by the statistical power of their tests, so a weak-form test is the least likely to reject and a strong-form test the most likely.
- Each form adds a restriction on preferences, so the strong form requires risk neutrality while the weak form requires only that investors prefer more to less.
<!-- YW5zOjE= -->
> The nesting is over **information sets**, not assets, tests or preferences. Past prices and volumes sit inside all public information, which sits inside public and private information together. A larger claim implies the smaller ones, so implications run strong → semi-strong → weak and rejections run the other way.
> Ref: Ribeiro (2026), Ch. 9, §9.1.1 (pp. 298–299)
> Similar: BKM 13e, Ch. 11 §11.2 (p. 346)

Q: Which pairing of form and characteristic test does the chapter give?
- Weak form tested by insider-trading records; semi-strong by autocorrelation of returns; strong by the performance of mutual fund managers.
- Weak form tested by event studies; semi-strong by momentum strategies; strong by the measured profitability of technical trading rules.
- Weak form tested by autocorrelation and technical rules; semi-strong by event studies; strong by the records of insiders and managers.
- Weak form tested by variance ratios; semi-strong by insider records; strong by the cross-section of average returns.
<!-- YW5zOjI= -->
> Each test must use exactly the information set its form covers. Autocorrelation and technical rules use the price history alone. An event study asks whether a **public** announcement is impounded at once, which is why the whole of §9.2 is devoted to it. Insiders and managers are the natural population for the strong form, and it is the form the evidence rejects.
> Ref: Ribeiro (2026), Ch. 9, §9.1.1 (pp. 298–299), §9.2 (p. 305)
> Similar: BKM 13e, Ch. 11 §11.4 (p. 354)

## misreadings

Q: "Efficient markets means the price equals fundamental value." The chapter rejects this reading. What is its correction?
- The price reflects information given a model of expected returns, so prices can be wrong, and only a systematic exploitable gap is ever ruled out.
- The price equals fundamental value in the long run only, since short-run deviations are permitted provided they revert within a short horizon.
- The price equals fundamental value only for securities with traded derivatives, since replication by arbitrageurs forces the two together.
- Efficiency says nothing about value, because value is unobservable and the hypothesis concerns only the serial correlation of returns.
<!-- YW5zOjA= -->
> Two clauses matter and both get dropped. First, **given a model of expected returns** — the joint hypothesis is already inside the definition. Second, errors are permitted: if the available information is wrong the price will be wrong, and efficiency is untouched. What efficiency forbids is a gap that is systematic and exploitable, not any gap at all.
> Ref: Ribeiro (2026), Ch. 9, §9.1.2 (pp. 299–300)
> Similar: Ribeiro, True/False bank, Ch. 9

Q: A student argues that because long-horizon returns are predictable from the dividend–price ratio, markets cannot be efficient. Which reply does the chapter endorse?
- The predictability is a small-sample artifact, so once the Stambaugh and Newey–West corrections are applied the evidence for it disappears altogether.
- Predictability of raw returns is compatible with efficiency only when the predictor is itself a traded asset, which the dividend–price ratio is not.
- Predictability refutes the weak form but leaves the semi-strong form intact, since the dividend–price ratio is public rather than price-history information.
- The argument confuses efficiency with a random walk; a random walk needs constant expected returns, and efficiency has never asserted any such thing.
<!-- YW5zOjM= -->
> This is the chapter's central reconciliation and its most examinable sentence. A **random walk** requires expected returns to be constant; **efficiency** does not. If the expected return itself varies, returns are predictable and the predictable part is compensation that moves — which is entirely consistent with efficiency. §9.3 supplies the evidence that this is what the data look like.
> Ref: Ribeiro (2026), Ch. 9, §9.1.2 (pp. 299–300), §9.3.3 (pp. 313–314)
> Similar: Ribeiro, Problem 9.2

Q: For which misreading does the chapter say the truth is precisely the reverse of the claim?
- That nobody can beat the market, since a measurable minority of managers beat it persistently once survivorship bias is removed from the sample.
- That fundamentals do not matter, since efficiency says prices track them so closely that nobody can profit from the tracking.
- That prices follow a random walk, since prices are in fact strongly mean-reverting at every horizon the literature has examined.
- That price equals value, since the two coincide exactly whenever markets are complete and arbitrage is unrestricted.
<!-- YW5zOjE= -->
> The misreading that efficiency makes fundamental analysis pointless inverts the content of the hypothesis. Efficiency is a claim about how hard the market works: prices follow fundamentals so closely that the marginal analyst cannot profit. It describes the intensity of competition among people who care about fundamentals, not their irrelevance.
> Ref: Ribeiro (2026), Ch. 9, §9.1.2 (p. 300)
> Similar: BKM 13e, Ch. 11 §11.2 (p. 346)

## conjunta

Q: The chapter boxes the joint-hypothesis problem as a key result. Which statement is it?
- Efficiency can be tested alone provided the benchmark is the market portfolio, since the CAPM is the unique equilibrium model.
- Efficiency and the expected-return model are always tested together, so a rejection condemns both and efficiency is never testable alone.
- Efficiency can be tested alone in event studies, since a short event window makes the choice of benchmark model immaterial to the abnormal return.
- Efficiency is testable only in its strong form, since the weak and semi-strong forms rest on an information set never directly observed.
<!-- YW5zOjE= -->
> An abnormal return is realized return minus **normal** return, and the normal return comes from a model. So the null being tested is always a conjunction. Find abnormal returns and you have found either inefficiency or a benchmark missing a risk factor, and no amount of data separates the two. State findings as a pair: *under this benchmark, this anomaly is this large.*
> Ref: Ribeiro (2026), Ch. 9, §9.1.3 (pp. 300–301), Key result
> Similar: Ribeiro, Ch. 4 §4.5 (Roll's critique); Ch. 6 §6.2

Q: The joint-hypothesis problem is linked to two earlier impasses in the course. Which pair, and what do the three share?
- Roll's critique and characteristics-versus-covariances: in each, a model and a claim about prices are testable only as a conjunction.
- The equity premium puzzle and the risk-free rate puzzle: in each, a plausible calibration of preferences fails to reproduce a first moment of the data.
- Two-fund separation and the Treynor–Black ladder: in each, an optimal portfolio splits into a benchmark plus an orthogonal active part.
- Grossman–Stiglitz and the limits to arbitrage: in each, frictions stop prices from fully reflecting available information.
<!-- YW5zOjA= -->
> Roll's critique says tests of the CAPM are really joint tests with the proxy for the market portfolio. The characteristics-versus-covariances debate says a return pattern cannot be labelled risk or mispricing from the pattern alone. Both are the joint-hypothesis structure in another costume: a claim about prices is inseparable from the $m$ used to judge it.
> Ref: Ribeiro (2026), Ch. 9, §9.1.3 (p. 301); Ch. 4 §4.5; Ch. 6 §6.2
> Similar: Ribeiro, True/False bank, Ch. 9

## grossman

Q: What does the Grossman–Stiglitz (1980) argument establish about perfectly informative prices?
- That they are impossible: nobody pays to gather what the price already reveals, and then it cannot reveal it.
- That they require risk-neutral investors, because risk aversion drives a wedge between price and expected payoff.
- That they arise only in complete markets, since spanning is what aggregates every private signal into prices.
- That they are generic, because competition among informed traders drives the marginal value of private information to zero.
<!-- YW5zOjA= -->
> The argument is a reductio. If prices revealed everything, the return to research would be zero, so nobody would research; with nobody researching, there is nothing for prices to reveal. Equilibrium therefore requires **enough inefficiency to pay for the research that makes prices informative** — which is why efficiency is a degree, not a property.
> Ref: Ribeiro (2026), Ch. 9, §9.1.4 (pp. 301–303)
> Similar: H&L (1988), Ch. 9 §9.8–9.10 (out of scope, named only)

Q: Reading efficiency as a degree rather than a yes-or-no property leads to which prediction?
- That efficiency is highest where prices are most volatile, since volatility attracts the research capital that informs prices.
- That efficiency rises monotonically over calendar time, because cheaper computation lowers information costs everywhere.
- That a researched large-cap sits closer to efficient than a small, hard-to-short security, because information costs differ.
- That efficiency is a property of the payoff structure, so derivatives are priced more efficiently than their underlyings.
<!-- YW5zOjI= -->
> The degree is set by the cost of gathering information and the capital pursuing it. Where research is cheap and capital deep, prices sit close to efficient; where a security is obscure, illiquid and costly to short, the equilibrium sits further away. §9.1.5 then explains why those pockets persist: that is exactly where arbitrage is hardest.
> Ref: Ribeiro (2026), Ch. 9, §9.1.4 (pp. 302–303)
> Similar: Ribeiro, Problem 9.1

## arbitragem

Q: Why is a catalogue of behavioural biases not by itself a theory of prices?
- Because the biases documented in the laboratory have never been shown among professionals managing institutional capital.
- Because the biases are individually small, so only their interaction in general equilibrium generates a measurable deviation.
- Because biases move the quantity traded rather than the price, and price is set by the marginal investor, not the average one.
- Because arbitrageurs would trade against any bias and remove it, so a theory of prices needs the limits to arbitrage too.
<!-- YW5zOjM= -->
> Documenting that investors err is not enough: the standing objection is that a rational trader exploits the error and thereby eliminates it. What makes behavioural finance a theory of **prices** is the second half — why a rational trader cannot or will not close the gap. The limits to arbitrage are load-bearing; the biases are the input they act on.
> Ref: Ribeiro (2026), Ch. 9, §9.1.5 (pp. 303–305)
> Similar: Ribeiro, True/False bank, Ch. 9

Q: In the Shleifer–Vishny account of noise-trader risk, what is the mechanism that makes it bite?
- The arbitrageur's risk aversion rises as the position moves against him, so he closes the trade before the mispricing corrects.
- Short-sale constraints stop the arbitrageur from taking the position at all, so the mispricing is never traded against at all.
- Margin requirements scale with realised volatility, so a widening mispricing forces a proportional cut in position size.
- He runs other people's money, and a widening mispricing triggers redemptions exactly when the opportunity is best.
<!-- YW5zOjM= -->
> The point is an agency one, not a preference one. A mispricing that worsens before it corrects produces interim losses; the investors who supplied the capital observe those losses and withdraw; so the position is cut precisely when its expected return is highest. Delegation turns a temporary adverse move into a permanent constraint.
> Ref: Ribeiro (2026), Ch. 9, §9.1.5 (p. 304)
> Similar: Ribeiro, Problem 9.3
