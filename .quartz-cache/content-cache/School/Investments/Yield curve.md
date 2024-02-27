---
aliases:
  - Term structure of intrest rates
---
The yield curve, or Term structure of intrest rates is a set of [[Yield to maturity|YTM]] at time $t$ for [[Bonds]] issued by the government of varying maturities.

It's important to investors for two reasons:
1. It offers a discount rate
2. It gives an indication of future expectations of rates

There are two types of yield curves:
- The [[Pure yield curve]]: uses stripped government coupon bonds, which makes them zero [[Zero-coupon bond]]s.
- The [[On-the-run yield curve]]: uses recently issued coupon bonds.

![[Yield curves.png]]
# Explanation
We can explain the yield curve **under certainty and under uncertainty**.
## Yield curve under certainty
Without intrest rate risk, bond investments with identical maturity should have the same return:
$$ (1+Y_{0,2})^2 = (1+R_{0,1})*(1+R_{1,1}) $$
We can define two types of rates here:
- $R_{0,1}$ or $R_{1,1} =$ [[Short rate]]
- $Y_{0,2}=$ [[Spot rate]]

When the [[Yield curve|Term structure of intrest rates]] is upward sloping, long [[Spot rate]]s are higher and thus future [[Short rate]]s should get higher.

When the [[Yield curve|Term structure of intrest rates]] is downward sloping, long [[Spot rate]]s are lower and thus future [[Short rate]]s should get lower.
## Forward rates
We can rewrite the equation from [[#Yield curve under certainty]] as follows:
$$ (1+Y_{O,T+1})^{T+1} = (1+ Y_{0,T})^T *(1+R_{T,1}) $$
With:
- $R_{T,1} =$ short rate at time $T$
- $Y_{0,T} =$ the rate of a [[Zero-coupon bond]] with maturity $T$

We can now solve for $R_{T,1}$ or as we will now call it $F_{T,1}$ the [[Forward rate]] for time $T$:
$$ (1+F_{T,1}) = \frac{(1+Y_{O,T+1})^{T+1}}{(1+ Y_{0,T})^T} $$

At time $0$ we can get a loan for at time $T$ at this forward rate even tough in the future, this rate might not be the same as the future [[Short rate]]. This is a [[Synthetic forward loan]].
# Theories
Two views/theories exist on the [[Yield curve]]:
1. [[Expectations hypothesis]]
2. [[Liquidity preference theory]]