[[Macaulay's duration]] is a measure of a bonds effective maturity. It weighs each payment (coupons and nominal value) over time to calculate a duration.

The weight of each payment is:
$$ w_t = \frac{\frac{C_t}{(1+Y)^t}}{P} $$
The duration of the bond is then:
$$ D = \sum_{t=1}^T t * w_t $$
for $t = 0, 1, 2, ...$

The duration of a perpetuity is:
$$ D_{perp}=\frac{(1+Y)}{Y} $$
# Impacting factors
Three impacting factors:
1. Maturity
2. Coupon size
3. Yield
## Maturity
As maturity increases we see from the equation of bonds [[Intrest rate risk]] that price change increases.
## Coupon size
As coupons get bigger, weight is shifted to the start of the investment horizon of the bond, thus the [[Macaulay's duration]] will be lower.
## Yield
As [[Yield to maturity|YTM]] increases the discount of all payments but will impact the later payments more. This will lower the duration of the bond.