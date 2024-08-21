There are three determinants of the bid-ask spread:
1. [[Order processing costs]]
2. [[Inventory risk]]
3. [[Asymmetric information models]]

We can compose the $PI_{t+s}$ over time using what these models indicate:

![[Price impact of the three determinants of spread.png]]

Three conclusions:
- The size of the spread and immediate [[Price impact]] are a result of all three of the determinants.
- Long-run [[Price impact]] is exclusively determined by [[Asymmetric information]]
- The order flow contains information, this leads to [[Price discovery]]
# Bid-ask spread
The bid-ask spread and it's three determinants, have important implications for policy makers? The spread can be seen as a friction to trading.

By finding out which determinant drives the spread, we can improve on it:

| Determinant                  | Solution                   |
| ---------------------------- | -------------------------- |
| *Real frictions*             | Improve the trading system |
| *Market power*               | Increase competition       |
| *[[Asymmetric information]]* | Improve transparency       |
## Econometric model
Huang and Stoll (1997) developed a general approach to estimating the impact of the components of the spread.

Starting with news as an impacting factor of $V_t$:
- $V_t$ fundamental value of the asset at time $t$
- $V_t$ changes with either private or public news:
	- Public news is $\varepsilon_t$
	- Private news is reflected in trades. The % of the half-spread ($\frac{S}{2}$) due to asymmetric information is $\alpha$.
- $d_{t-1}$ the trade direction at time $t$

We can compose $V_t$ as $V_{t-1} +$ the impact of public and private news. We can express $V_t$ as:
$$ V_t = V_{t-1} + \alpha \frac{S}{2} d_{t-1} + \varepsilon_t $$
$V_t$ however, can't be observed, so we need to relate it to the mid quote $M_t$.

We assume that trades are of size one. The dealer's inventory at time $t-1$ is then:
$$ \sum_{i=1}^{t-1} d_i $$
We can denote the proportion of the half-spread that is due to inventory risk as $\beta$:
$$ \beta \frac{S}{2} \sum_{i=1}^{t-1} d_i $$
Then $\Rightarrow$
$$ M_t = V_t + \beta \frac{S}{2} \sum_{i=1}^{t-1} d_i $$
By taking the first difference, we can rewrite this as:
$$ \Delta M_t = (\alpha + \beta) \frac{S}{2} d_{t-1} + \varepsilon_t $$
(See proof)

Since $P_t$ is either the ask or the bid plus or minus a half of the spread, and term $\eta_t$ to account for rounding errors since in practice prices are discrete:
$$ P_t = M_t + \frac{S}{2} d_t + \eta_t$$
We can then take the first difference:
$$ \Delta P_t = (\alpha + \beta) \frac{S}{2} d_{t-1} + \frac{S}{2} (d_t - d_{t-1}) + e_t$$
With $e_t=\Delta \eta_t + \varepsilon_t$ (See proof)

This equation allows us to estimate:
- Spread $S$
- Percentage of the spread due to inventory and [[Asymmetric information]] $\alpha + \beta$
- Percentage of the spread due to order processing costs $1-\alpha - \beta$

However, we still need to be able to *separate* the spread due to inventory and the spread due to [[Asymmetric information]].

We denote $\pi$ the probability that the next trade direction is opposite to the prior. If $\pi \neq 0.5$, then there's some predictability in the trades:
$$ \mathbb E(d_{t-1}|d_{t-2}) = \pi (-d_{t-2}) + (1-\pi) d_{t-2} $$
$$ \mathbb E(d_{t-1}|d_{t-2}) = (1-2\pi) d_{t-2}$$
This implies that the trade in $t-1$ is partly due to predictable information and partly due to unpredictable private information. We can modify the equation for $V_t$ accordingly:
$$ V_t = V_{t-1} + \alpha \frac{S}{2} (d_{t-1} - (1 - 2\pi)d_{t-2}) + \varepsilon_t $$
$$ V_t = V_{t-1} + \alpha \frac{S}{2} d_{t-1} - \alpha \frac{S}{2} (1- 2\pi) d_{t-2} + \varepsilon_t$$
We then find for the change in $P_t$:

![[Formulae estimation determinant of spread.png]]

We can now estimate:
- Spread $S$
- Spread due to [[Asymmetric information]] $\alpha$
- Spread due to inventory costs $\beta$
- Spread due to order handeling costs $1-\alpha - \beta$
- Probability of trade reversal $\pi$

In case the spread isn't needed to be estimated, we can use the following model:

![[Formulae estimation determinant of spread without estimation of spread.png]]
## Example results
The following results were found by Huang and Stoll (1997):

![[Result 1 empirical model of spread.png]]

$\alpha <0$ and $\pi < 0.5$ are empirically possible, but not in theory. A possible reason could be because large orders are in the data decomposed into many smaller orders, which could result in apparent positively serially correlated orders instead of negatively serially correlated orders.

After bunching related orders together, we obtain the following results:

![[Result 2 empirical model of spread.png]]

Thus the:
- inventory cost component of the spread is $28.65\%$
- [[Asymmetric information]] component of the spread is $9.59\%$
- [[Order processing costs]] component of the spread is $61.8\%$
# Price impact of trading
The price impact of a trade contains two components:
1. A permanent (persistent) component: [[Asymmetric information]] and informed trading
2. A temporary (transient) component: [[Inventory risk]], [[Order processing costs]], discrete pricing, price smoothing, ...
## Setup
- Ask, bid and mid quote $A_t, B_t,M_t$ at time $t$.
- The quotes of a trade at time $t$ were set at $t-1$.
- After the trade in $t$, public information arrives. The dealer then updates quotes.
## Econometric model
The information that is contained in the trade at time $t$ is given by the revision of the mid quote, or $r_t$:
$$ r_t = M_t - M_{t-1} $$
This revision can be due to both public and private information. We assume that this revision is constant (so we get an average revision from the model) and we assume a linear relation:
$$ r_t = \beta_0 x_t + \varepsilon_{r,t} $$
With error term $\varepsilon_{r,t}$ which reflects public information, $x_t$ the trade size and $\beta_0$ the coefficient of the price impact of the trade. However, this form is incomplete (see ppt):
$$ (1) \: \: \: r_t = \alpha_1 r_{t-1} + \alpha_2 r_{t-2} + ... + \beta_0 x_t + \beta_1 x_{t-1} + ... + \varepsilon_{rt}$$
Furthermore, inventory models also predict serial correlation in trades, so:
$$ (2) \: \: \: x_t = \gamma_1 r_{t-1} + \gamma_2 r_{t-2} + ... + \delta_1 x_{t-1} + \delta_2 x_{t-2} + ...+ \varepsilon_{rt} $$
Equation $(1)$ and $(2)$ form a bivariate vector-autoregressive model, or **VAR**. This allows us to apply the formula to trades and make a resolution between private and public information. We assume:

![[Empirical model price impact assumptions.png]]
## Example
VAR is signed in trade size $x_t$. This makes it difficult to compare multiple different assets. For this, Hasbrouck (1991a) proposed to use indicator $d_t$, where $d_t = +1$ if $x_t > 0$, $d_t = 0$ if $x_t=0$ and $d_t < 0$ if $x_t < 0$. VAR is then:

![[VAR with indicator d instead of x.png]]

(See example ppt)
# Price discovery
The question to be answered is: *How much do trades contribute to the incorporation of information in prices of stocks?*
## Econometric model
Denote mid quote at time $t$ as $M_t$ and signed[^1] trade volume $x_t$.

We follow the sequence of assumptions of [[#Price impact of trading|Hasbrouck]]:
1. Trade $x_t$ is executed at the quotes set at the previous period.
2. Non-trade public information arrives
3. Dealer posts new quotes ($M_t$), mid quote $M_t$ is the one after the trade at $t$

The mid quote is seen as the sum of two observable components:
$$ M_t = M^*_t + s_t$$
With $M^*_t = \mathbb E_t (\widetilde V)$. This is seen as the assets efficient price, an expectation of the fundamental value based on all the public information at $t$. It follows a random walk:
$$ M^*_t = M^*_{t-1} + \varepsilon_t$$





[^1]: Trade volume with a $+$ or $-$ denoting respectively a buy or sell order.