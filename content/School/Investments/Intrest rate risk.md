Changes in intrest rates have an impact on bond prices:
- An increase in intrest rates has a decreasing effect on bond prices.
- A decrease in intrest rates has a positive effect on bond prices.

Intrest rate risk increases for:
- Longer maturities
- Lower coupons
- Lower yields

For [[Zero-coupon bond]]s it's easy to calculate the impact of a change in maturity or [[Yield to maturity|YTM]] by using the pricing formula '$P=\frac{1}{(1+Y)^T}$' and taking the  first derivative:
$$ \frac{dP}{P} = -T(\frac{dY}{1+Y}) $$
with $\frac{dP}{P}$ being the percentage change in P.

For normal [[Bonds]], it's more difficult to calculate intrest rate risk, we have to use [[Macaulay's duration]].

We can then use this duration as the maturity $T$:
$$ \frac{dP}{P} = -D(\frac{dY}{1+Y}) $$
# Duration in practice
Practitioners will often use the [[Modified duration]], denoted as $D^*$, instead of the [[Macaulay's duration]] as it captures the intrest rate sensitivity better.

The price change equation then changes to:
$$ \frac{dP}{P}= -D^* dY $$
with:
- $D^*=$ [[Modified duration]]
- $dY=$ percentage change in [[Yield to maturity|YTM]]
# Convexity
In reality the duration approximation of price change in bonds by changing the [[Yield to maturity|YTM]] is a linear curve. In reality, actual prices are on a curve. 

![[Bond price change duration vs reality.png]]

For small changes in [[Yield to maturity|YTM]], the duration can be a fairly accurate indicator, but the larger the less accurate. The real price change will always be higher than the expected price change using duration.

Convexity can be calculated by using the following formula:
$$ Convexity = \frac{1}{P} ((\sum_{t=1}{T} \frac{t*(t+1)*C}{(1+Y)^{t+2}})+\frac{T*(T+1)*M}{(1+Y)^{T+2}}) $$
This convexity can then be combined with the duration to get the percentage price change:
$$ \frac{dP}{P} = -D^* * dY * \frac{1}{2} * Convexity * (dY)^2 $$
## Advantage
Convexity is considered a good thing since positive changes in [[Yield to maturity|YTM]] have a smaller negative impact on bond price changes and negative changes in [[Yield to maturity|YTM]] have a larger positive impact on bond price changes.
# Effective duration and convexity
Practitioners will often use the concept of [[Effective duration]] and [[Effective convexity]] instead of [[Modified duration]].