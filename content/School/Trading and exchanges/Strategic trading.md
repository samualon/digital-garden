[[Asymmetric information models]] offer a way for dealers to *protect* themselves from informed traders, but how can informed traders most optimally trade with information?

An intuitive solution would be for the trader to trade as much as possible with her information. However, since the dealer can observe order flow, he will adjust his prices quickly, which will bring them closer to the real fundamental value.

A solution for the traders is to hide her trades in the order flow by hiding it between the noise traders. If fluctuation of noise traders is higher, this is easier for the informed trader.
# Model
## Intuition
Some setup of the model:
- There are two types of traders:
	- Uninformed traders (noise traders) that trade randomly
	- One informed trader who knows the value of $\widetilde V$
- The dealer sets prices efficiently (conform [[Semi-strong-form efficiency]]) based on order flow.
- Trading is modeled as an auction:
	1. Informed and uninformed traders simultaneously choose quantities that they want to trade (the informed trader doesn't know how much the uninformed traders will trade)
	2. Dealer sets **one** price and trades the quantities that clear the market.
## Setup
- One period
- One risky asset $\widetilde V$ with (no $V^H$ or $V^L$):
$$ \widetilde V \sim N(\overline V, \sigma^2_V) $$
- Traders can only submit market orders
- Uninformed traders trade in total a quantity following:
$$ \overline u \sim N(0, \sigma^2_u) $$
- One informed trader:
	- Receives signal about the fundamental value of $\widetilde V$
	- Is the only one with the information
	- Trades quantity $\widetilde x$
- The dealer:
	- Is risk-neutral
	- Sets price $\widetilde p$ after observing order flow
### Dealer
The dealer observes order flow $\widetilde w= \widetilde x + \widetilde u$, but not $\widetilde x$ or $\widetilde u$ separately. He sets market clearing price $\widetilde p$:
$$ \widetilde p = P(\widetilde w) = \mathbb E(\widetilde V|\widetilde w) $$ The dealer's expected profits $=0$ (see proof).
### Trader
Values $\widetilde V, \widetilde u$ are realized and the informed trader chooses $\widetilde x$. She's aware of $\widetilde V$ but not of $\widetilde u$. Her quantity $\widetilde x$ depends of course on $\widetilde V$:
$$ \widetilde x = X(\widetilde V) $$
She aims to maximize her expected profits:
$$ \mathbb E(\widetilde \pi | \widetilde V = V ) = ¸\mathbb E((\widetilde V - \widetilde p) \widetilde x | \widetilde V = V) $$
Her profits thus depend on the dealers price funcion (through $\widetilde p = P(\widetilde w))$.
## Solution
> [!info] Defintion
> The equilibrium is a combination of $X$ and $P$ such that 1. and 2. hold:
> 1. **Profit maximization:** For any alternative strategy $X'$:
> $$ \mathbb E[\widetilde \pi(X,P)|\widetilde V = V] \geq \mathbb E[\widetilde \pi(X',P)|\widetilde V = V] $$
> 2. **Market efficiency**: The following is satisified:
> $$ \widetilde p = \mathbb E(\widetilde V|\widetilde w) $$

> [!example] Theorem
> Constants $\beta$ and $\lambda$:
> $$ \beta = \sqrt \frac{\sigma^2_u}{\sigma^2_V} \: and \: \lambda = \frac{1}{2} \sqrt \frac{\sigma^2_V}{\sigma^2_u} $$
> The informed trader's strategy is:
> $$ X(\widetilde V) = \beta (\widetilde V - \overline V) $$
> The equilibrium price is:
> $$ P(\widetilde w) = \overline V + \lambda \widetilde w = \overline V + \lambda(\widetilde x + \widetilde u) $$
(See proof)
### Intuition
The optimal quantity of the informed trader:
 $$ X(\widetilde V) = \beta (\widetilde V - \overline V)=\sqrt \frac{\sigma^2_u}{\sigma^2_V}(\widetilde V - \overline V)  $$
 This shows two things:
 1. The variance of uninformed trading increases her optimal trading quantity, since this would make it easier to hide her trades.
 2. The variance of $V$ decreases her optimal trading quantity. It represents her information advantage. If her information advantage is higher, she reveals more information to the dealer while trading thus letting the dealer adjust his prices to the fundamental value of $\widetilde V$. She needs to trade more cautiously to avoid adverse price movements.
## Implications
### Market liquidity
As there's only one price, this model can't use the bid-ask spread to measure liquidity, it uses depth:

> [!info] Definition
> Depth of the market is measured by:
> $$ \frac{1}{\lambda} $$

Since:
$$ \lambda = \frac{1}{2} \sqrt \frac{\sigma^2_V}{\sigma^2_u} \Rightarrow \frac{1}{\lambda} = 2 \sqrt \frac{\sigma^2_u}{\sigma^2_v} $$
This means depth, or liquidity, is increasing in $\sigma^2_u$ and decreasing in $\sigma^2_V$.
### Price discovery
> [!info] Definition
> The price of information informativeness, or the price discovery, is:
> $$ \Sigma_1 = Var(\widetilde V|\widetilde p) $$

With  $\sum_0$ being the variance of the fundamental value before trading or $\sigma^2_V$ and $\sum_1$ after one round of trading.

> [!example] Proposition
> Price informativeness is given by:
> $$ \Sigma_1 = Var(\widetilde V|\widetilde p) = \frac{1}{2} \sigma^2_V = \frac{1}{2} \Sigma_0$$
(See proof)

This shows that one half of the informed trader's information is incorporated into prices.
### Expected profits of the informed trader
> [!example] Proposition
> The expected profit of the informed trader is:
> $$ \mathbb E(\widetilde \pi) = \frac{\sigma^2_V}{4\lambda}= \frac{1}{2} \sqrt{\sigma^2_V \sigma^2_u} $$

The expected profits of the informed trader are positive. However, it isn't necessarily always positive. F.e. if a large amount of uninformed traders by chance do the same order as the informed trader, this can push the price up above the real fundamental value, creating a loss for the informed trader. 
### Transaction costs for uninformed traders
> [!example] Proposition
> The expected trading cost for uninformed traders is:
> $$ \mathbb E(\widetilde{TC}) = \frac{1}{2} \sqrt{\sigma^2_V \sigma^2_u} $$

Since dealers make no profit, the expected loss of the liquidity traders is the expected profit of the informed trader.
# $N$ period model
