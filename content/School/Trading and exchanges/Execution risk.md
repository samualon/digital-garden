When placing a [[Limit order]], there's a possibility that your order never gets executed as opposed to a [[Market order]] which is always executed.
# Model
The following model is a simplified version of Foucault.
## Setup
- Market for one asset
- Trading days as discrete interval $t=1,2,3,...,\widetilde T$
	- $\widetilde T=$ the random day trading for the asset stops and pay-off is realized.
	- Random because each period $t$ has chance $1-\rho>0$ that trading stops.
- Parameter $\rho$ thus captures [[Execution risk]]
- Fundamental value $V$ which is $cte$ over time.
- Each $t$ one trader arrives in the market
- While the asset has value $V$, each trader has different personal values attached to the asset (stem from different sources, opinions, preferences, etc)
	- Value of asset $V$ at $t=V+\widetilde \beta_t$. 
	- $V=$ fundamental value
	- $\widetilde \beta_t=$ personal valuation of the trader at time $t$
		- Fraction $k$ has high personal valuation $\beta_h$ for the asset
		- Fraction $1-k$ has low personal valuation $-\beta_l$ for the asset
	- It has been proven that we can simplify the model by assuming that traders of type $\beta_h$ only submit buy orders and $-\beta_l$ only sell orders.
- Traders are risk-neutral
- Traders maximize expected utility
- Traders account for other traders' optimal strategies
- Limit orders stay in the book for one period
- LOs can't be modified or canceled

We now assume a trader at time $t$ of type $\beta_h$. Since we assumed he would only buy, he has three strategies:
1. Submit a buy [[Limit order]]: $LOBuy$
2. Submit a buy [[Market order]]: $MOBuy$
3. Submit no order
(Analogue for type $-\beta_l$)

- If he is indifferent between $LOBuy$ and $MOBuy$ we assume he chooses a [[Market order]].
- If the [[Limit order book]] is empty, he submits a [[Limit order]]
## Equilibrium order choice strategy
### Introduction
Assume a trader in $t$ of type $\beta_h$. If he submits a $LOBuy$ he needs to determine his bid price. While doing so, he has to account for the execution probability. $LOBuy$ is executed if:
1. Trading continues (Probability $\rho$)
2. Next trader is a seller (Probability $1-k$)
3. Next trader submits a $MOSell$

The first two conditions are exogenous, but the third one is endogenous. By increasing the his bid price, the trader at time $t$ can increase the chances of a $MOSell$ in the following period. However, the trader wants to maximize his gains, so he doesn't want to set a too high of a [[Bid price]].

> [!warning] Key insight
> The buyer at time $t$ thus needs to put a bid price at which the seller in $t+1$ is indifferent between $LOSell$ and $MOsell$.

We don't set the bid higher, because at the criterium above the seller is already convinced to submit a $MOSell$. There's no need to give up more of the profits.
### Formalization
$\widehat B_{t+1}$ is the bid price set by the trader at $t$ at which the seller at $t+1$ is indifferent between $MOSell$ and $LOSell$. This bid is a function of $V$ and $\beta_l$:
$$ \widehat B_{t+1} = \widehat B_{t+1}(V,\beta_l) $$

The expected gain of a $LOBuy$ at $t$ **in case it's executed**:
$$ = V+\beta_h-\widehat B_{t+1} $$
(his personal valuation of the asset - the bid price that has to be set)

This gain however, is only executed upon execution, which depends on:
- The continuation of trading $\rho$
- The next trader being a seller $1-k$

The expected gain of the $t$ trader when submitting a $LOBuy$ is thus:
$$ (1) \; \rho (1-k) (V+\beta_h - \widehat B_{t+1}) $$
What about the expected gain of a $MOBuy$ submitted at $t$? We denote the ask price where the trader of type $\beta_h$ at $t$ is indifferent between $MOBuy$ and $LOBuy$ as $\widehat A_t$. This bid is a function of $V$ and $\beta_h$ (analogue to the indifferent bid price of the trader in $t+1$):
$$ \widehat A_t = \widehat A_t (V,\beta_h) $$
The gain of a $MOBuy$ is then:
$$ (2) \; V+ \beta_h - \widehat A_t $$
Then the buyer at $t$ is indifferent between a $MOBuy$ and $LOBuy$ if both have the same gain:
$$ V+ \beta_h - \widehat A_t = \rho (1-k) (V+\beta_h - \widehat B_{t+1})$$
The same reasoning can be applied to a trader of type $\beta_l$ in $t$:
$$ \widehat B_t - (V-\beta_l) = \rho k(\widehat A_{t+1} - (V-\beta_l)) $$
(with the left side the gain for a $MOSell$ and the right side for $LOSell$)
### Solution
Since the problem that the traders solve doesn't depend on the time period of the trade, we can drop the time subscript (the problem in $t$ is the same problem in $t+s$):
$$ V+ \beta_h - \widehat A = \rho (1-k) (V+\beta_h - \widehat B)$$
$$ \widehat B - (V-\beta_l) = \rho k(\widehat A - (V-\beta_l)) $$
Solving these two equations to their equilibrium ask and bid quotes $A^*$ and $B^*$ results in the following:

> [!example] Theorem
> The equilibrium ask quote, set by a trader of type $\beta_l$ is:
> $$ A^*=\widehat A=V-\beta_l + \frac{1-\rho(1-k)}{1-\rho^2k(1-k)}(\beta_h + \beta_l) $$
> The equilibrium bid quote, set by a trader of type $\beta_h$ is:
> $$ B^*=\widehat B=V+\beta_h + \frac{1-\rho k}{1-\rho^2k(1-k)}(\beta_h + \beta_l) $$
(See proof [[T&E delen videos herbekijken]])

Depending on the current market price, the formulae above will decide whether to submit a $LO$ or $MO$. F.e. if the ask price in the market is higher than $A^*$, then the trader of type $\beta_h$ gains more when submitting a $LOBuy$ with bid price $B^*$. Otherwise he should submit a $MOBuy$ (symmetric for a $\beta_l$ trader who sells).

To make the expression more tractable, we can assume $k=1-k=0.5$:

> [!example] Corollary
> ![[Tractable equilibrium prices of execution risk.png]]

This corollary shows:

> [!example] Corollary
> The spread is increasing in [[Execution risk]].

Intuitively, a decreasing $\rho$ means that trading has a smaller probability of continuing, meaning that $LO$s are less likely to execute, making $MO$s more attractive. This also means that $LO$s must be less aggressively priced to be attractive to the next trader $\rightarrow$ higher ask and lower bid $\rightarrow$ wider spread.