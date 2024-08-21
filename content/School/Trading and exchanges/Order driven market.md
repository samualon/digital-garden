---
aliases:
  - Limit order market
  - LOM
  - Auction market
  - Double auction market
---
[[Price formation, market liquidity and price discovery]] focused on [[Quote driven market|Dealer market]]s. This page focuses on limit order markets. This is the dominant market form for large stock exchanges. Traders interact directly, with the exception of brokers who act as transmitters of orders. However, these brokers don't take positions themselves.

There are two major types of order driven markets, distinguished on the condition whether orders are executed immediately upon submission or at discrete intervals:
- [[Continuous limit order market]]: immediately
- [[Call limit order market]]: discrete intervals
# Distinction with quote driven markets
In a dealer market, there's a sharp distinction between liquidity suppliers and demanders. This distinction becomes more blurred in [[Order driven market|Limit order market]]s. Agents choose dynamically whether to supply or demand liquidity. Big differences are:
- No dealers with an obligation to post quotes
- Trading happens directly between traders
- Traders choose between a [[Market order]] (MO) and [[Limit order]] (LO)
- LO are stored in the limit order book until possible future execution against a new MO
# Complexity
[[Order driven market|Limit order market]]s are complex since:
- **Action spaces are very large**: which limit price, quantity, order type to choose?
- **Non-linear pay-offs**: in some cases your LO can be executed, in others not. Pay-off can thus be either $=0$ or $>0$.
- **Dynamic**: a new LO executes against a future MO and has to compete with the currently existing LOs and possible future LOs. Strategy is thus difficult.
# Limit order vs market order
Traders face a dilemma, which order type to choose?

| [[Limit order]]                                           | [[Market order]]                 |
| --------------------------------------------------------- | -------------------------------- |
| Better price (you earn the spread)                        | Worse price (you pay the spread) |
| [[Execution risk]] (the order might not get executed)     | Certain execution                |
| [[Picking-off risk]]/[[Picking-off risk\|Winner's curse]] | [[Price impact]]                 |

Some important determinants are:
- Bid-ask spread
- [[Volatility]] of the asset's fundamental value ([[Picking-off risk]])
- Depth of both sides of the market ([[Execution risk]])
- Composition of the population of traders

In order to analyze these determinants, three models can be used:
1. **Parlour**: focus on the time priority rule and shows that the choice between MO and LO depends on depth of both sides.
2. **Foucault**: focus on the [[Picking-off risk|Winner's curse]]. [[Volatility]] is the important factor here.
3. **Foucault, Kadan, Kandel**: determinants of the price formation and order type choice are:
	- Speed of agents' arrival
	- Waiting costs
	- Composition of the population of traders