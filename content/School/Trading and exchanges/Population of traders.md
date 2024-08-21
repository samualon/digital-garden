Foucault, Kadan and Kandel (2005) developed a model to assess the strategy of impatient and patient liquidity traders. Two variables are used as determinants of the limit order book dynamics in equilibrium:
1. Proportion of patient traders
2. Order arrival rate
# Setup
- $LO$s are infinitely lived and cannot be cancelled or changed.
- Traders have a preference for immediacy through a penalty on waiting time.
- Traders arrive sequentially and alternate between buyer and seller
- No quantity choice (each trade for one unit)
- Only quote-improving $LO$s are allowed

The main idea of the model is: *Patient traders will submit a $LO$, impatient traders a $MO$.*
# Key results
## Spread
Rate at which market orders are submitted is decreasing with the size of the spread.

Spread improvements are larger when:
	- Proportion patient traders $\theta_P$ is large
	- Waiting cost $\delta_P$ is large
	- Order arrival rate $\lambda$ is small
## Resilience
When traders are heterogeneous, resilience of the order book $R$:
- Increases in proportion of patient traders $\theta_P$
- Increases in waiting cost $\delta_P$
- Decreases in order arrival rate $\lambda$

If the proportion of patient traders increases:
- Demand for liquidity decreases
- Expected time to execution of an $LO$ increases
- Waiting cost increases
- Resilience is higher
## Fast vs slow markets
| Fast           | Slow           |
| -------------- | -------------- |
| Lower spread   | Higher spread  |
| Less resilient | More resilient |
