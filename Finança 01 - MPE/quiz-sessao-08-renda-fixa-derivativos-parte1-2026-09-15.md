---
quiz: "Session 8 — Fixed Income and Derivatives, Part 1: The Curve, Duration, and Convexity"
tags:
  primitive: "1 · Zeros as the Primitive, and What a YTM Compresses"
  forwards: "2 · Spot Rates, Discount Factors, Forward Rates"
  bootstrap: "3 · Bootstrapping and the Law of One Price"
  duration: "4 · Duration, Convexity, DV01"
  immunization: "5 · Immunization and the Limits of Duration"
---

## primitive

Q: Chapter 8 opens by calling the constant $y$ of the single-yield formula (8.1) "a quotation convention, not a fact about the world". Which reading of that sentence is the chapter's?
- It means the YTM is computed from promised rather than expected cash flows, so it is a fair quotation only for default-free bonds, where the two coincide.
- It means the YTM misstates the return because coupons will not in fact be reinvested at $y$, which is the one defect that pricing off the spot curve repairs.
- It means nothing forces a dollar due in one year and one due in ten to share a rate, so the pricing rule is one spot rate per maturity and $y$ is its scalar summary.
- It means the YTM is an internal rate of return and therefore non-unique when cash flows change sign, so the spot curve is the only well-defined discounting object.
<!-- YW5zOjI= -->
> The complaint is about the *constancy* of $y$ across maturities, not about default, reinvestment or sign changes. A bond is a portfolio of zeros and must be priced by $P=\sum_t CF_t\,d_t$, discounting each cash flow at its own maturity's rate; the YTM is the one blended rate reproducing that same $P$ — a compression of the vector $(d_1,\dots,d_N)$ into a scalar. The reinvestment and default caveats are real, and Appendix C carries them, but they are a different complaint.
> Ref: Ribeiro (2026), Ch. 8, §8.1 (pp. 264–265), §8.2.1 (p. 267)
> Similar: Ribeiro, Problem 8.1(d) (p. 294); True/False 7 (p. 296)

Q: Two default-free bonds are priced off one identical spot curve, and their yields to maturity differ. What does the chapter say follows?
- Nothing is wrong: the YTM blends the curve using each bond's own cash-flow timing, so a high-coupon bond loads on the near, low-spot end and quotes a different rate.
- One of the two must be mispriced, since arbitrage across the STRIPS market forces every default-free bond off one curve to share a single internal rate of return.
- The curve must be inverted, because only a downward-sloping curve makes the blended rate depend on where a bond's cash flows sit along the maturity axis.
- The two bonds must differ in credit quality, since the spread between promised and expected yield is the only wedge that can separate two yields on one curve.
<!-- YW5zOjA= -->
> A yield to maturity is the constant $y$ that reproduces a price built from many different spot rates, so it is a value-weighted blend whose weights are the bond's own discounted cash flows. The chapter's example: the 6% three-year bond off the $(2.00,2.50,3.00)\%$ curve prices at $108.5983$ and quotes $y=2.96\%$, a number that lies between $s_1$ and $s_3$ and belongs to that bond alone. Hence the rule: price off the curve, not off a yield, whenever cash-flow timing differs.
> Ref: Ribeiro (2026), Ch. 8, §8.2.1 (p. 267), §8.2.3 (p. 268)
> Similar: Ribeiro, Problem 8.1(d) (p. 294); BKM 13e, Ch. 15 §15.2 (p. 484)

## forwards

Q: The chapter insists that a forward rate is "locked in today, not a forecast". Which argument establishes the value of $f_{n-1,n}$, and what does it assume about expectations?
- A forward is a zero-net-supply contract, so the market clears only when it equals the consensus forecast; the assumption is that the marginal investor is risk-neutral over one period.
- Two riskless routes from today to date $n$ cost a dollar and must pay the same, which pins $1+f_{n-1,n}=(1+s_n)^n/(1+s_{n-1})^{n-1}$; no expectation enters at all.
- The forward equals the expected short rate plus a term premium estimated from the slope, so it is a forecast corrected for risk rather than a pure no-arbitrage object.
- Rolling one-period bonds must match the $n$-period bond in expectation, which pins the forward once investors agree on the distribution of future short rates.
<!-- YW5zOjE= -->
> Equation (8.5) comes from a pure replication argument: invest for $n$ periods at $s_n$, or invest for $n-1$ periods at $s_{n-1}$ and contract *today* to roll one period at $f_{n-1,n}$. Both are riskless and cost one dollar, so they must return the same, and the forward is fixed by two observed spot rates. The expectations hypothesis (§8.4) is the separate, and rejected, claim that this locked-in rate happens to equal $E_t[r_{t+n-1}]$; the arithmetic of (8.5) holds either way.
> Ref: Ribeiro (2026), Ch. 8, §8.2.2 (p. 267), eq. (8.5)
> Similar: Ribeiro, Problem 8.2(c) (p. 294); True/False 27 (p. 297)

Q: A spot curve rises with maturity. What does the chapter's averaging property imply for the forward curve, and why?
- Forwards lie below spots, because each spot rate compounds the forwards out to its own maturity and compounding a rising sequence overshoots the terminal rate.
- Forwards equal spots at every maturity, because a rising curve is exactly the case in which the geometric average of the short rate and the forwards is flat.
- Forwards lie above spots, because each spot rate is a geometric average of the short rate and the forwards out to it, and a rising average needs higher margins.
- Forwards lie above spots only if the curve rises faster than the term premium, since the averaging property holds under the expectations hypothesis alone.
<!-- YW5zOjI= -->
> Compounding (8.5) gives $(1+s_n)^n=(1+s_1)\prod_{k=2}^n(1+f_{k-1,k})$: the $n$-period spot rate is the geometric average of today's short rate and all the forwards out to $n$. An average rises only when the marginal term exceeds it, so a rising spot curve forces forwards above spots — and a falling one puts them below. Example 8.1 shows it numerically: spots $2.00, 2.50, 3.00\%$ against forwards $2.00, 3.00, 4.01\%$. This is arithmetic, not an assumption about premia.
> Ref: Ribeiro (2026), Ch. 8, §8.2.2 (p. 267), Example 8.1 (p. 268)
> Similar: Ribeiro, Problem 8.1(c), Problem 8.2(a) (p. 294)

## bootstrap

Q: In Example 8.1 the two-year spot rate is extracted from a two-year 4%-coupon bond priced at $102.9103$, given $s_1=2.00\%$. Which sequence is the bootstrap step, stated in literal terms?
- Solve the single-yield formula (8.1) for the bond's YTM, then set $s_2$ equal to it, since a two-year bond's internal rate of return is by construction the two-year zero rate.
- Discount the date-1 coupon at $s_2$ itself and iterate on $s_2$ numerically, since both cash flows must be discounted at the rate being solved for.
- Average $s_1$ with the bond's coupon rate weighted by present value, since the bootstrap is the inverse of the weighted-average construction of a coupon bond.
- Discount the date-1 coupon at the known $s_1$, subtract it from the price, and solve the residual $104/(1+s_2)^2=98.9887$ for the one remaining unknown.
<!-- YW5zOjM= -->
> The bootstrap is recursive precisely because each bond adds one equation for one new unknown: known coupons are discounted at previously solved spot rates, and the final cash flow carries the new rate. Here $102.9103-4/1.02=98.9887$ and $s_2=(104/98.9887)^{1/2}-1=2.50\%$. Discounting the first coupon at $s_2$ would be pricing a one-year cash flow at a two-year rate — the very blending the spot curve exists to avoid — and the bond's own YTM (about 2.49%) is not $s_2$.
> Ref: Ribeiro (2026), Ch. 8, §8.2.3 (pp. 267–268), Example 8.1
> Similar: Ribeiro, Problem 8.1(a) (p. 294); BKM 13e, Ch. 15 §15.2 (p. 484)

Q: The chapter calls bootstrapping "the law of one price of Chapter 1 made operational". What is the trade that enforces it, and what does the phrase concede about practice?
- The trade is the STRIPS strip-and-reconstitute arbitrage, and the concession is that real curves are fit to many noisy bonds at once with smoothing, without changing the logic.
- The trade is the cash-and-carry arbitrage in Treasury futures, and the concession is that the curve is identified only up to the cheapest-to-deliver bond in each maturity bucket.
- The trade is a duration-matched barbell against a bullet, and the concession is that the bootstrap holds only for parallel shifts of the extracted spot curve.
- The trade is borrowing at the forward rate and lending spot, and the concession is that bootstrapping requires a traded zero at every maturity to close the recursion.
<!-- YW5zOjA= -->
> A coupon bond must cost exactly what its stripped pieces cost, or a dealer strips it (or reconstitutes it) for a riskless profit — the STRIPS market of Appendix C makes that literal. The chapter is candid that quotes are noisy and maturities do not line up as neatly as Example 8.1, so practitioners fit a smoothed curve to the whole traded universe; what does not change is the definition: the spot curve is the set of discount factors that reprices that universe.
> Ref: Ribeiro (2026), Ch. 8, §8.2.3 (p. 268); Appendix C (STRIPS)
> Similar: Ribeiro, Problem 8.1(d) (p. 294)

## duration

Q: Macaulay and modified duration "are the same number up to the factor $1+y$", and the chapter says their coincidence *is* the content of the concept. Which statement gets both the definitions and the division of labour right?
- Macaulay is the elasticity of price to yield and modified the weighted-average maturity; match modified to a liability horizon and multiply Macaulay by $\Delta y$ for a price move.
- Both are elasticities measured in years, and the choice between them is a convention about whether the yield is quoted annually or at the payment frequency.
- Macaulay is a time and modified a price elasticity; match Macaulay to a horizon for immunization, and use modified in $\Delta P/P\approx-D_{mod}\Delta y$.
- Macaulay is a time and modified a price elasticity, and $D_{mod}=D_{Mac}(1+y)$, so modified always exceeds Macaulay whenever yields are positive.
<!-- YW5zOjI= -->
> $D_{Mac}$ (8.6) is the present-value-weighted average time to payment, in years; $D_{mod}=-\frac{1}{P}\frac{dP}{dy}=D_{Mac}/(1+y)$ (8.7) is a proportional price change per unit of yield. Interchanging them injects a $1+y$ error into every hedge — and note the direction: modified duration is *smaller*, being Macaulay divided, not multiplied, by $1+y$. The immunization result is about the horizon at which price and reinvestment risk cancel, which is Macaulay.
> Ref: Ribeiro (2026), Ch. 8, §8.3.1 (pp. 269–270), Common pitfalls (p. 293)
> Similar: Ribeiro, Problem 8.3(a) (p. 294); True/False 11 (p. 296); BKM 13e, Ch. 16 §16.1 (p. 510)

Q: In Example 8.2 (6% annual coupon, 5 years, priced to yield 5%, $P=104.3295$, $D_{mod}=4.2645$, $C=23.444$) a $+1$ percentage-point yield move gives a duration-only estimate of $-\$4.449$ and an exact reprice change of $-\$4.3295$. What does the convexity term do, and why does its sign never flip?
- It adds $+\$0.122$, recovering almost all of the error, and stays positive for an ordinary bond because every cash flow is positive, so the true curve lies above its tangent.
- It subtracts $\$0.122$, correcting the tangent's habitual overstatement of the price, and is positive only because the yield move here happens to be an increase rather than a decrease.
- It adds $+\$0.122$ and is signed by $\Delta y$, so it cushions losses when rates rise and offsets part of the gain when they fall, leaving the approximation symmetric.
- It adds $+\$0.122$, and its sign is positive because the bond trades at a premium; a discount bond of the same maturity would carry negative convexity instead.
<!-- YW5zOjA= -->
> The second-order term is $\tfrac12 C(\Delta y)^2 P$, and $(\Delta y)^2>0$ whatever the direction of the move, while $C>0$ for any bond with all cash flows positive (8.8). So convexity adds to the price on a rise *and* on a fall — the analytic form of "the gain from a fall exceeds the loss from a rise". Here $\tfrac12(23.444)(0.01)^2(104.3295)=+\$0.122$, turning $-\$4.449$ into $-\$4.327$ against the exact $-\$4.3295$. Negative convexity needs an embedded option (a callable), not a discount price.
> Ref: Ribeiro (2026), Ch. 8, §8.3.2 (p. 270), Example 8.2 (pp. 270–271)
> Similar: Ribeiro, Problem 8.3(b) (p. 294); True/False 15 (p. 296)

## immunization

Q: A pension owes $\$1{,}000{,}000$ in five years at a flat 5% yield and immunizes with a barbell of three- and ten-year zeros ($w_3=0.7143$, $w_{10}=0.2857$, PV $\$783{,}526$). What is the residual risk, and how does the barbell's convexity enter the verdict?
- The residual is reinvestment risk on the three-year leg, and the barbell's higher convexity is what creates it, since dispersed cash flows must be rolled at unknown future rates.
- The residual is that duration drifts with time and yield, and the barbell's convexity is irrelevant to it, since convexity is a second-order effect on price and not on the horizon.
- The residual is curve-steepening risk, and the extra convexity helps against large parallel shifts while doing nothing about the non-parallel move duration cannot see.
- The residual is credit risk on the longer leg, and the extra convexity compensates for it, which is why liability-driven investors prefer barbells to a single duration-matched bullet.
<!-- YW5zOjI= -->
> Duration matching immunizes against the *parallel* component of a curve move only. The barbell's cash flows are more dispersed than a five-year bullet's, so it carries more convexity, which is worth money against large shifts; but dispersion is exactly what exposes it when the short and long ends move by different amounts. Hence the chapter's verdict: among duration-matched portfolios the more convex one is better protected against large shifts, and liability-driven investing stays an active, rebalanced discipline.
> Ref: Ribeiro (2026), Ch. 8, §8.3.3 (p. 271), §8.3.4 (p. 272)
> Similar: Ribeiro, Problem 8.3(c) (p. 294); True/False 29 (p. 297); BKM 13e, Ch. 16 §16.3 (p. 527)

Q: Which statement about the duration of special bonds and portfolios is exactly right as Chapter 8 states it?
- A perpetuity's duration is $1/y$, independent of coupon; a callable bond's effective duration rises as yields fall, because the call extends the bond's expected life.
- Portfolio duration is the value-weighted average of holdings' durations; a perpetuity's is $(1+y)/y$; a callable's effective duration can fall as yields drop, since the call shortens its life.
- Portfolio duration is the maturity-weighted average of holdings' durations; a zero's duration is its maturity; a callable is priced by the closed-form formula with the call date as maturity.
- Portfolio duration is additive only for zeros, since coupon bonds' weighted-average times cannot be aggregated; a perpetuity's duration is undefined, its maturity being infinite.
<!-- YW5zOjE= -->
> Duration is additive *by value* — a portfolio's cash flows are the union of its bonds' — which is what lets a manager summarize a whole book with one number and immunize by matching it. The perpetuity formula is $D_{perp}=(1+y)/y$ (8.10), 21 years at $y=5\%$, independent of the coupon. And a callable breaks the comparative statics: as yields fall the issuer's option truncates the upside and the expected life shortens toward the call date, so the *effective* duration, measured by repricing under small up/down shifts, can fall — the negative convexity of §8.3.2.
> Ref: Ribeiro (2026), Ch. 8, §8.3.4 (p. 272), eq. (8.10)
> Similar: Ribeiro, Problem 8.3(d) (p. 295); BKM 13e, Ch. 16 §16.1 (p. 510)
