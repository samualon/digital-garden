# Coupon or no coupon
## Coupon bond
A [[Coupon bond]] price is calculated as follows:
$$ P_{0,t} = \sum_{t=1}^T \frac{C_t}{(1+ R_{0,t})^t} + \frac{par \: value}{(1+R_{0,T})^T} $$
With:
- $C_t=$ coupon payment at time $t$
- $R_{0,t} =$ market (spot) intrest rates
- $T=$ maturity period of the bond

# Invoice price
During time in between coupon payments [[Accrued intrest]] arises, which is intrest that accumulates since the last bond payment. The bond holder isn't payed for this yet.

To incorporate this into the price of the bond, you add the [[Accrued intrest|calculated accrued intrest]] to the flat price of the bond. 
# Yield to maturity
[[Yield to maturity]] is used to summarize the performance of a bond.

Since [[Yield to maturity|YTM]] is calculated in case of holding the bond until maturity, it can only be used to compare bonds with the same maturity. We can, however, use [[1-period realized return]] to compare bonds of different maturities.
## YTM and prices
[[Yield to maturity|YTM]] and prices are inversely and linearly related, since higher coupon bonds are sold at higher prices.

There exist three situations of relation between:
- [[Yield to maturity|YTM]]
- [[Current yield]]
- Premium, par or discount selling
- Coupon rate

| Selling | Relation |
| ---- | ---- |
| Premium | Coupon rate > current yield > YTM |
| Par | Coupon rate = current yield = YTM |
| Discount | Coupon rate  < current yield < YTM |
## YTM and realized returns
YTM will differ from the realized returns as the bond can be sold before maturity or not all coupons are payed out.

By doing a **horizon analysis**, we can assess the realized return by:
- forecasting future reinvestment rates (how much do I gain on coupons I already received?)
- forecasting future bond prices (at what price could I sell my bond prematurily?)
## YTM on callable bonds
[[Yield to maturity|YTM]] doesn't incorporate the risk of a call, so it can't be applied effectively to callable bonds.

Risk of a call is higher when intrest rates are low and vise verse.

[[Yield to call]] calculates a [[Yield to maturity|YTM]] where maturity is the point where a call is most likely.
# Yield spread
Comparable bonds can differ in prices because of two risks carried by the bond:
- [[Default risk|Credit risk]] or [[Default risk]]
- [[Liquidity risk]]

These risks are reflected in the [[Yield spread]] of the bonds.