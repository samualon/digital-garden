Assume a population of traders where some traders possess private information about stock $i$. Dealers can't know which traders possess this information.

If a dealer trades with a trader who possesses private information he makes a loss:
- If the trader knows that $\widetilde V$ is higher than what the dealer thinks, he will buy at the price set by the dealer and gain value.
- If the trader knows that $\widetilde V$ is lower than what the dealer thinks, he will sell at the price set by the dealer and gain value.
# Model
In the model we assume that $\widetilde V$ can either be of low value $V^L$ with probability $\theta$, or of high value $V^H$ with probability $1-\theta$. $V^L < V^H$.

There are two groups of traders. Proportion $\kappa$ of traders know before they trade if $\widetilde V = V^L$ or $= V^H$. Fraction $1-\kappa$ does not know the real value of $\widetilde V$ and trades for reasons exogenous of the model (noise traders). These uninformed traders buy with probability $\gamma_{Buy}$ and sell with probability $\gamma_{Sell}$.

![[Asymmetric information model tree.png]]

For each time period $t$, the dealer knows the distribution of chances of the fundamental value of $\widetilde V$ and the proportion of informed traders, but doesn't know which value for $\widetilde V$ is realized and which traders are informed.

For each time period $t$, exactly one trader arrives randomly chosen from the trader population who can put a market order for a sell or buy of one unit.

![[Asymmetric information models timeline.png]]

The dealer can revise his quotes before the next trader arrives in $t+1$. His quotes are conditional on the order of the trader:
$$ A_t= \mathbb E (\widetilde V| \mathcal F_t) = \mathbb E(\widetilde V| \mathcal F_{ŧ-1}, Buy_t) $$
$$ B_t= \mathbb E (\widetilde V| \mathcal F_t) = \mathbb E(\widetilde V| \mathcal F_{ŧ-1}, Sell_t) $$
## Initial bid and ask at $t=0$
Initially, the dealer can't yet have learned about prior trades, so:
$$ A_0 = \mathbb E(\widetilde V|Buy_0)$$
$$ B_0 = \mathbb E(\widetilde V|Sell_0)$$
Since we know $\widetilde V$ can assume two values:
$$ A_0 = V^L \mathbb P(\widetilde V = V^L|Buy_0) + V^H \mathbb P(\widetilde V = V^H|Buy_0) $$
We can then work out:

![[Formulae asymmetric information models initial bid and ask.png]]
(see proof)

If we add the assumption that $\theta$, $\gamma_{Buy}$ and $\gamma_{Sell} = \frac{1}{2}$, then the formulas get simplified:

![[Simplified formulae asymmetric information models bid and ask.png]]
## Spread
The simplified formula for $S_0$ shows that a positive spread arises due to asymmetric information (through the proportion of $\kappa$, the proportion of uninformed-informed traders).

> [!example] Proposition 1
> The spread is increasing in the probability of informed trading $\kappa$ and in the variance of the value of the risky asset

This proposition has two parts that can be intuitively interpreted:
1. **Proportion of informed traders**: larger $\kappa$ increases the chances of a dealer meeting an informed trader, which means he has higher expected losses which he will compensate with a larger spread.
2. **Variance of $\widetilde V$**: The variance, in other words the difference between possible values of $\widetilde V$ has a positive impact on the informational advantage of informed traders, increasing expected losses of the dealer which will make him increase his spread.
(See proof)
## Updating bid and ask over $t$
We now look at $t=0 \rightarrow t=1$ and we assume at $t=0$ a buy.

The dealer can update his price before $t=1$ and does this with the information that the previous trade was a buy. $\mathcal F_1$ is larger than $\mathcal F_0$. In the future:
$$ \mathcal F_0 \subseteq \mathcal F_1 \subseteq \mathcal F_2 ...$$
The dealer can learn since order flow must reflect information. However, $Buy_0$ doesn't give him the information whether the trader was informed or not, but the probability is more positive that he was informed. This learning is called **Bayesian updating**.

Since informed traders are at one side of the market, the order flow won't be balanced. The bid and ask are updated as follows:

![[Asymmetric information models ask and bid at time 1.png]]

The formulae for $A_1$ and $B_1$ are then:

![[Formulae asymmetric information models bid and ask at time 1.png]]
(see proof)

If we add the assumption that $\theta$, $\gamma_{Buy}$ and $\gamma_{Sell} = \frac{1}{2}$, then the formulas get simplified:

![[Simplified formulae asymmetric information models bid and ask at time 1.png]]
## Bid, ask and spread of $t=0$ vs $t=1$
![[Asymmetric information models A0 and A1.png]]

Since $0<\kappa<1 \Rightarrow A_1 > A_0$. The dealer revises his ask price upwards after $t=0$. The same is true for $B_0$ and $B_1$.

![[Asymmetric information models S0 and S1.png]]

Since $0<\kappa<1 \Rightarrow S_1 < S_0$. Since the dealer learned from the order flow and adjusted it's prices, the information gain of informed traders is lower. This means the dealer needs to compensate less for the losses and the spread becomes lower.

Thus:

> [!example] Corollary
> After a buy in $t=0$, the ask and bid quotes are revised upwards at $t=1$ and the spread declines at $t=1$.
## Price impact
### Immediate price impact
> [!example] Theorem
> The immediate price impact of a buy order:
> $$ PI_t = \mathbb E(\widetilde V|\mathcal F_{t-1}, Buy_t) - \mathbb E(\widetilde V|\mathcal F_{t-1}) $$
> The immediate price impact of a sell order:
> $$ PI_t = \mathbb E(\widetilde V|\mathcal F_{t-1}, Sell_t) - \mathbb E(\widetilde V|\mathcal F_{t-1}) $$
### Long-term price impact
In the long-term, if there are no new orders after $t$ and no new information arrives, then the dealer won't have any reason to revise his prices. This leads to a permanent impact of the order at $t$:

![[Asymmetric information models long-term price impact.png]]
## Price discovery
> [!info] Definition
> [[Price discovery]] is the extend to which prices reflect information, and the speed at which information is incorporated into prices.

There are thus two questions that we can ask on [[Price discovery]]:
1. To which extent do prices reflect information?
2. How fast is information incorporated into prices?
### Market form
The first question concerns which type of market the model is in:
- [[Strong-form efficiency]]
- [[Semi-strong-form efficiency]]
- [[Weak-form efficiency]]
#### Semi-strong-form efficiency
The market in the model above is [[Semi-strong-form efficiency|semi-strong-form efficient]], since:
$$ A_t = \mathbb E(\widetilde V|\mathcal F_{t-1}, Buy_t) $$
$$ B_t = \mathbb E(\widetilde V|\mathcal F_{t-1}, Sell_t) $$
These prices reflect publicly available information.

Even though this model presents two separate prices ($A_t$ and $B_t$), the two prices are not related to market inefficiency. They are a result of the dealer's learning and this is what incorporates information of the order flow into prices.

Since our model is semi [[Semi-strong-form efficiency|semi-strong-form efficient]]:
> [!example] Corollary
> Transaction prices in the model are [[Martingale]]. First differences between prices are serially uncorrelated.

This is in contrast with the negative serial correlation between prices in the models of [[Inventory risk]].
#### Strong-form efficiency
It isn't true that at any time $t$, the market in the model would be [[Strong-form efficiency|strong-form efficient]]. However, if there are informed traders ($\kappa > 0$), then in the limit prices will converge to the fundamental value. So in $t \rightarrow \infty$ the market becomes [[Strong-form efficiency|strong-form efficient]].
### Speed of price discovery
Again, the transaction price is: 
$$ p_t = V^L \mathbb P(\widetilde V|\mathcal F_{t-1}, d_t) + V^H \mathbb P(\widetilde V| \mathcal F_{t-1}, d_t)$$
We know that if all information is public: $p_t = V^H$. So the speed of incorporation of information into prices is the speed of $p_t \rightarrow V^H$. And $p_t \rightarrow V^H$ if $\mathbb P(\widetilde V = V^H|\mathcal F_{t-1}, d_t) \rightarrow 1$.

> [!example] Theorem
> The speed at which information is incorporated into prices depends on the proportion of informed traders $\kappa$ (if $\kappa > 0$).

The above can be proven intuitively. If there are no informed traders, then buy and sell orders are 50/50. If there are some informed traders, then the order flow becomes unbalanced. This is how dealers become aware of information and increase prices. Another illustration, if $\kappa$ is close to 1, then buy orders will dominate and dealers will assign a high probability to $\mathbb P(\widetilde V = V^H)$, which will make them increase the price close to $V^H$.
## Policy
> [!example] Theorem
> Due to informed trading, there's a trade-off between market liquidity and informational efficiency.

More informed traders increases the spread, which lowers the market's liquidity. However, more informed traders increases the speed at which information is incorporated into prices, which increases the market's informational efficiency. This is a difficult trade-off.
# Measuring asymmetric information
PIN is a theory that can be used to measure asymmetric information. It is similar to the previous [[#Model]], but it adds event uncertainty. Besides having $V^L$ and $V^H$, there's also the possibility of having no information.
## Setup
- A single risky asset is traded over $D$ trading days, indexed $d=0,1,2,...,D$.
- Within each day, time is continuously indexed by $t$, where $t \in [0,T]$.
- The dealer sets an ask and bid price at each point in time.
- Before each trading day starts, nature decides if an information event takes place:
	- Probability $\alpha$ there is an information event
		- Probability $\delta$ bad news
		- Probability $1 - \delta$ good news
	- Probability $1-\alpha$ no information event: no asymmetric information so no informed traders
	- Information events are independently distributed
- Value of the asset at the end of trading day $d$ is $V_d$.
- $V^H_d =$ value of the asset on day $d$ in case of good news
- $V_d^L=$ value of the asset on day $d$ in case of bad news
- $V_d^{no}=$ value of the asset on day $d$ in case of no news
- $V_d^L < V_d^{no} < V^H_d$

There are two types of traders:
1. Informed traders
2. Uninformed traders
### Informed traders
Informed traders observe whether an information event occurred and whether its good or bad news. They will buy in case of good news and sell in case of bad news.

They arrive at a rate of $\mu$ per period of time. The likelihood of observing $x$ orders in a time period is:
$$ e^{-\mu} \frac{\mu^x}{x!} $$
### Uninformed traders
They do not observe the information event. Uninformed buyers arrive at rate $\varepsilon_{Buy}$ and sellers at rate $\varepsilon_{Sell}$.
### Dealer
The dealer is risk-neutral and competitive.

He knows the parameters of the model, but can't observe nature's choice between good, bad and no news. The arrival rates of traders however, allow him to learn and update his beliefs, [[Bayesian updating]].
### Overview
![[PIN asymmetric information tree.png]]
## Probability of Informed Trading (PIN)
>[!info] Definition
>The probability that a trade is information-based is:
>$$ PIN = \frac{\alpha \mu}{\alpha + \varepsilon_{Buy} + \varepsilon_{Sell}} $$

(No proof)

This is simply the ratio between the arrival rate of informed traders and the arrival rate of all traders.

Additionally, it can be shown that the PIN is positively related to the spread:
$$ S_0 = PIN(V_d^H - V_d^L) $$
### Estimating PIN
Assume a trading day with bad news. In this case, buyers (who will only be uninformed traders) will arrive at rate $\varepsilon_{Buy}$. Sellers (who will be both uninformed and informed traders) will arrive at $\varepsilon_{Sell} + \mu$. In this case, the likelihood of observing $\#Buys$ and $\#Sells$ is then:
$$ e^{- \varepsilon_{Buy}} \frac{(\varepsilon_{Buy})^{\#Buys}}{\#Buys!} * e^{- (\varepsilon_{Sell} + \mu)} \frac{(\varepsilon_{sell} + \mu) ^{\#Sells}}{\#Sells}$$
Something similar goes for a trading day with good news and no news:
$$ e^{- (\varepsilon_{Buy} + \mu)} \frac{(\varepsilon_{Buy} +\mu)^{\#Buys}}{\#Buys!} * e^{- \varepsilon_{Sell}} \frac{(\varepsilon_{sell}) ^{\#Sells}}{\#Sells}$$
$$ e^{- \varepsilon_{Buy}} \frac{(\varepsilon_{Buy})^{\#Buys}}{\#Buys!} * e^{- \varepsilon_{Sell}} \frac{(\varepsilon_{sell}) ^{\#Sells}}{\#Sells}$$
Using the probabilities for no news $1-\alpha$, bad news $\alpha \delta$ and good news $\alpha(1-\delta)$, we can estimate the likelihood of informed trading by combining the three equations above:

![[Estimating PIN formula.png]]
Where $\theta=(\alpha, \mu, \varepsilon_{Buy}, \varepsilon_{Sell}, \delta)$.

Since days are assumed independent, we can observe the likelihood of $(\#Buys_d, \#Sells_d)^D_{d=1}$:

![[Estimating parameters of the PIN model.png]]

This formula then gives us estimations of all the parameters in $\theta$.