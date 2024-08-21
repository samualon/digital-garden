---
aliases:
  - Winner's curse
---
A [[Limit order]] can become miss-priced in the future if public or private news changes, which adjust the fundamental value of the asset. Then other traders can pick-off the miss-priced limit order, which results in a loss for the original trader.
# Model
The model is a variation of the model for [[Execution risk#Model|Execution risk]].

First, the fundamental value is no longer assumed constant, but varying with a random walk:
$$ \widetilde V_{t+1} = \widetilde V_t + \widetilde \varepsilon_{t+1} $$
with $\varepsilon_{t+1}$ the arrival of news:
- iid
- Takes value $+\sigma$ or $-\sigma$ with probabilities $0.5 / 0.5$

This means that $LO$s can become miss-priced. The trader in $t$ sets his $LO$ price based on the information then. The trader in $t+1$ however, knows the realization of $\widetilde \varepsilon_{t+1}$ ($+\sigma$ or $-\sigma$).

Additionally, a miss-priced [[Limit order]] is more likely to be executed ([[Picking-off risk|Winner's curse]]).

> [!example] Corollary
> Other things equal, the proportion of limit orders in the order flow increases with the asset's [[Volatility]].

Intuitively: Increasing [[Volatility]] $\rightarrow$ Increasing [[Picking-off risk]] of LO traders $\rightarrow$ They increase their reservation spreads $\rightarrow$ They post less attractive offers $\rightarrow$ Cost of [[Market order]] trading increases $\rightarrow$ [[Limit order]]s become the optimal strategy more frequently.

> [!example] Corollary
> Other things equal, the expected limit order [[Fill rate]] decreases with the asset's [[Volatility]].

Intuitively, in high [[Volatility]], $LO$ traders price more defensively because of the higher [[Picking-off risk]]. This decreases the likelihood of execution and thus the [[Fill rate]].