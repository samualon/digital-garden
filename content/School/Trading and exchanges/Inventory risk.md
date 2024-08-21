Inventory risk is a [[Market friction]]. 

Traders on a [[Quote driven market]] usually don't directly trade at the same time, so a dealer will take the opposite side of the trade. This dealer however, has an optimal portfolio of stocks. If a trader buys f.e. 100 shares of AAPL, this means that the dealer deviates from his optimal amount of AAPL shares by 100. This is expressed as his **inventory**, an inventory of -100.

In order to fix this, the dealer pursues **balanced order flow**. By increasing the bid and ask price, he respectively decreases incentive for traders to buy AAPL from him and increases incentive for traders to sell AAPL to him. This should reduce his inventory in the short term.
# Model
## Setup
- Two-period model with $t=0$ and $t=1$
- $N$ risky assets can be traded
- Dealer is:
	- Counterparty to each trade
	- [[Risk-aversion|Risk-averse]]
	- Competitive
- Dealer enters $t=0$ with his [[Optimal risky portfolio]], his **investment account**
- This account contains $q^*_{i,0}$ units of asset $i$ and an amount cash $c_0$:
	- $q^*_{i,0} > 0 =$ long position
	- $q^*_{i,0} < 0 =$ short position
	- Cash is used to buy stocks from traders and increases when selling stocks to traders
	- $R_f$ on cash $=0$
- Observed fundamental value of risky asset $i$ at time $t=0$ is $V_{i,0}$
- The dealer's wealth in $t=0$ ($=$ initial wealth) is equal to his optimal portfolio $W_0$:
$$ W_0 = \sum_{i=1}^N V_{i,0} q^*_{i,0} + c_0$$
We consider two cases:
1. Dealer does not trade in $t=0$
2. Dealer acts as counterparty in an order from a trader
### Dealer does not trade
The dealer keeps his optimal portfolio until $t=1$. His payoff for each asset $i$ is $\tilde V_i$ where $\tilde V$ doesn't change over time so he doesn't update his beliefs after a sale or a trade.

The dealers **terminal wealth** at $t=1$ is then:
$$ \tilde W^{No \: Trade}_1 = \sum^N_{i=1} \tilde V_{i,1} q^*_{i,0} + c_0$$
### Dealer trades
We assume:
- One transaction per trading period
- Traders only submit [[Market order]]s
- Size of the trader's order is $x_{i,0}$ units of asset $i$
	- $x_{i,0} > 0 =$ Dealer receives a buy order
	- $x_{i,0} < 0 =$ Dealer receives a sell order

The dealer's trading account or inventory of $i$ is then the difference between his optimal position and his current position.

The dealers terminal wealth is then:
$$ \tilde W^{Trade}_1 = \sum^N_{i=1} \tilde V_{i,1} q^*_{i,0} + c_0 - \tilde V_{i,1} x_{i,0} + p_{i,0} x_{i,0}$$
We now need to find the price $p_{i,0}$ where the dealer will be willing to execute the order. See [[#Solution]].
## Solution
The dealer will execute the order if his utility is equal between having not traded and having traded:
$$ \mathbb{E}_0 [U(\widetilde W^{No \: Trade}_1)] = \mathbb{E}_0 [U(\widetilde{W}^{Trade}_1)] $$
With a mean-variance preference, this equals:
$$ \Rightarrow \mathbb{E}_0(\widetilde W^{No \: Trade}_1) - \frac{A}{2} var_0(\widetilde W^{No \: Trade}_1) = \mathbb{E}_0(\widetilde{W}^{Trade}_1)) - \frac{A}{2} var_0(\widetilde{W}^{Trade}_1)) $$
This results in the following solution (see proof):
$$ p_{i,0} = \overline{V}_i - A \sigma_{i,*} + \frac{A}{2} \sigma^2_i x_{i,0}$$
The ask and bid prices are:
$$ A_{i,0} = \overline{V}_i - A \sigma_{i,*} + \frac{A}{2} \sigma^2_i |x_{i,0}| = M_{i,0} + \frac{A}{2} \sigma^2_i |x_{i,0}| $$
$$ B_{i,0} = \overline{V}_i - A \sigma_{i,*} - \frac{A}{2} \sigma^2_i |x_{i,0}| = M_{i,0} - \frac{A}{2} \sigma^2_i |x_{i,0}| $$
With spread:
$$ S_0 = A \sigma^2_i |x_{i,0}| $$
With:
- $\overline{V}_i = \mathbb{E}_0 [\widetilde{V}_i]$
- $\sigma^2_i = Var(\widetilde{V}_i)$
- $\sigma_{i,*} = Cov(i,*)$ with $*=$ the optimal portfolio at time $t=0$
- $M_{i,0} = \overline{V}_i - A \sigma_{i,*}$
# Initial inventory
With initial inventory $I_i,0$, we get the following wealth function:
$$ W_0 = \sum^N_{i=1} V_{i,0}q^*_{i,0} + c_0 + V_{i,0}I_{i,0} $$
This gives the following price:
$$ p_{i,0} = \overline V_i - A \sigma_{i,*} - AI_{i,0} \sigma^2_i + \frac{A}{2} \sigma^2_i x_{i,0} $$
Ask and bid are then:
$$ A_{i,0} = \overline V_i - A \sigma_{i,*} - AI_{i,0} \sigma^2_i + \frac{A}{2} \sigma^2_i |x_{i,0}| $$
$$ = M_{i,0} + \frac{A}{2} \sigma^2_i |x_{i,0}|$$
$$ B_{i,0} = \overline V_i - A \sigma_{i,*} - AI_{i,0} \sigma^2_i - \frac{A}{2} \sigma^2_i |x_{i,0}| $$
$$ = M_{i,0} - \frac{A}{2} \sigma^2_i |x_{i,0}|$$
With mid quote:
$$ M_{i,0} = \overline V_i - A \sigma_{i,*} - AI_{i,0} \sigma^2_i $$ 
And spread:
$$ S_0 = A \sigma^2_i |x_{i,0}| $$
## Spread and mid quote
The magnitude of the spread is thus unaffected by the inventory, but the position of the spread (or the mid quote) is:
- If the inventory is higher, then the dealer quotes a lower mid quote, which makes it easier to sell and get back to the optimum portfolio.
- If the inventory is lower, then the dealer quotes a higher mid quote, which makes it easier to buy and get back to the optimum portfolio.
# Price impact
## Fundamental value
Instead of using $\widetilde V_i$ which represented *pay-off*, we use $\widetilde V^*_i$ which represents the fundamental value of asset $i$.

The expected fundamental value of the asset is then:
$$ \mathbb{E} (\widetilde V^*_i | \mathcal F_{t-1}) = \overline V_i - A\sigma_{i,0}$$
This includes [[Risk-aversion]] $A$.
## Immediate $PI$
When assuming zero starting inventory, the immediate $PI$ of a buy order for one unit is:
$$ PI_{i,t} = \frac{A}{2} \sigma^2_i $$
The immediate $PI$ of a sell order of one unit is:
$$ PI_{i,t} = - \frac{A}{2} \sigma^2_i $$
(see proof)
## Long-term $PI$
In the long-term 
$$ \lim_{s \rightarrow \infty} (PI_{t+s})=0 $$
(see proof)
## Corollaries
This brings four corollaries:
1. Inventory is mean-reverting
2. Inventory risk implies a positive correlation in the short-term between the change in mid quote and order flow. In the long-term, the correlation between both is negative.
3. Under inventory models, there is negative correlation in changes (difference with the prior amount) in:[^1]
	- Prices
	- Trades
4. Dealers with more extreme inventory positions will quote more aggressively.[^2]
# Empirical evidence
Hansh et al. (1998) tested the inventory model using four steps:
1. Use theory to derive empirically verifiable predictions
2. Choose dataset
3. Compute variables to measures concepts of the theory
4. Build and estimate the econometric model

The data covered 273 trading days of thirty FTSE-100 stocks.
## Inventory series
The inventory of dealer $j$ in stock $i$ at time $t$ is given by:
$$ Q^j_{i,t} = Q^j_{i,0} + \sum^t_{s=1} q^j_{i,s} $$
With:
- $q^j_{i,s} =$ the trade by dealer $j$ in stock $i$ at time $s$:
	- $q>0 =$ sell order from trader
	- $q<0 =$ buy order from trader

Because we can't observe [[Risk aversion]] $A$ of dealers, we standardize the inventory using the inventory from above:
$$ I^j_{i,t} = \frac{Q^j_{i,t} - \overline Q^j_i}{S^j_i}$$
With:
- $\overline Q^j_i =$ the average level of inventory of dealer $j$ in stock $i$
- $S^j_i=$ the sample standard deviation

We can then prove:
$$ I^j_{i,t} = \frac{\sum^t_{s=1} q^j_{i,s} - \frac{\sum^T_{s=1} (\sum^s_{r=1} q^j_{i,r})}{T+1}}{S^j_i} $$
(see proof)

[^1]: When a dealer sells a lot, the price will increase, after which they will sell a lot and the prices will decrease. Same for the traders perspective (order flow).
[^2]: In a market with multiple dealers, the dealer with the highest inventory will quote the best ask prices. The dealer with the lowest inventory will quote the best bid prices.