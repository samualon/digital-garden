In contrast to [[Continuous limit order market]]s, orders are made and matched at periodical points in time, a [[Call auction]]. [[Market order]]s and [[Limit order]]s are collected in a book. All orders are then executed at the same market clearing, [[Uniform price auction]].

[[Continuous limit order market]]s usually use a [[Call limit order market]] process before open (and sometimes after close). The non-marketable orders pre-open are then added as the first orders in the [[Limit order book]].
# Process
1. All buy orders are sorted by decreasing limit price.
2. All sell orders are sorted by increasing limit price.
3. An equilibrium is found where these two series of prices cross.
4. All buy orders with a higher price than the equilibrium are executed and all sell orders with a lower price than the equilibrium orders are executed. Other orders aren't executed.

![[Call limit order process graph.png]]