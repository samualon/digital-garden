In order to understand the key concepts of [[Financial market infrastructure]], we need a benchmark: **efficient markets**. Deviations from the [[Efficient market hypothesis]] are [[Market friction]], which introduce:
- [[Market liquidity]]
- [[Price impact]]
- [[Price discovery]]
# Efficient market hypothesis
The fundamental value of an asset $\tilde{V}$ is the value at which the asset can be liquidated in a friction-less and efficient market. This value will be certain at some point in the future ($V$), but it's still unsure today.

In [[Efficient market hypothesis|EMH]], the price of asset $\tilde{V}$ reflects all available information at time $t$ with $t=0,1,2,3, ...$ The price is the expected value of the asset given all the available information at time $t$.  This leads to the definition of [[Efficient market hypothesis|EMH]].

In the context of [[Trading and exchanges]], we don't account for the time-value of money (discounting) as the time between f.e. $t_1$ and $t_2$ is often very small.
## Definition of EMH
Price $p_t$ of an asset should be equal to the estimated fundamental value of the asset, given all information at time $t$:
$$ p_t = \mathbb{E}_t [\tilde{V}] \: or \: \mathbb{E}[\tilde{V} | \mathcal{F}_t] $$
With $\mathcal{F}_t =$ the information set at time $t$.
## Forms of EMH
Depending on the information set, EMH has three forms:
1. [[Weak-form efficiency]]
2. [[Semi-strong-form efficiency]]
3. [[Strong-form efficiency]]
## Implications of EMH
### Price only changes at arrival of news
News is the update of the expectation of the fundamental value of $V$ due to the arrival of news between $t$ and $t+1$:
$$ \tilde{\varepsilon} = \mathbb{E}_{t+1}[\tilde{V}] - \mathbb{E}_t[\tilde{V}] $$
The following must hold:
$$ \mathbb{E}[\tilde \varepsilon_{t+1}] = 0 \: and \: \mathbb{E}[\tilde \varepsilon_t] =0$$
$\Rightarrow$ the news is isn't known at $t$ and can't have an impact of the estimation of $\tilde \varepsilon$ at time $t+1$.

Additionally:
$$ \mathbb{E}[\tilde \varepsilon_t \tilde \varepsilon_s] = 0$$
for $t\neq s$, which means prior information (news) can't forecast future news.

In this way, the best estimation of $p_t+1$ is $p_t$ with all the information at time $t$. Prices are [[Martingale]]:
$$ p_t = \mathbb{E}_t[p_{t+1}] \: § $$