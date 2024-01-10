## Chapter 02
- [ ] Prices in EMH are frictionless
- [ ] News $\epsilon_t$ 
- [ ] Properties of news
- [ ] Prices in EMH are martingale + proof
- [ ] Prices are uncorrelated
- [ ] $A_t$ and $B_t$ are equal to $\mathbb{E}_t(\tilde{V})$
- [ ] Price impact at time $t$
- [ ] Immediate price impact

> [!faq]- Tips chapter 02
> #### Prices in EMH are frictionless
> $$p_t = \mathbb{E}(\tilde{V}|\mathbb{F}_t)$$
> #### Prices are uncorrelated
> Start from the fact that $\Delta p_t = \epsilon_t$ and thus $cov(\Delta p_t, \Delta p_s) = cov(\epsilon_p, \epsilon_s)$ 
> #### Price impact
> $$PI_t+s = \mathbb{E}(p_{t+s}|\mathbb{F}_{t-1}, d_t) - \mathbb{E}(\tilde{V}|\mathbb{F}_{t-1})$$
> In case of immediate price impact, just drop the $s$ in the equation above.
## Chapter 03 - Order costs
- [ ] Order costs and immediate price impact
- [ ] Order costs and (long run) price impact

> [!faq]- Tips chapter 03
> #### Order costs and immediate price impact
> Use $A_t = E(p_t | \mathbb{F}_{t-1}, d_t)$ and the fact that $\tilde{V}$ is independent from $d_t$.
> #### Order costs and price impact
> Use the fact that $p_{t+s} = E(\tilde{V}|\mathbb{F}_{t-1}) + cd_{t+s}$ , that $\tilde{V}$ and $d_{t+s}$ are independent and that at period $t$ the chances of a sell or buy are both 50% (thus expected value of 0).
## Chapter 04 - Inventory risk
- [ ] Price with inventory risk
- [ ] Midquote
- [ ] Price impact with inventory risk
- [ ] Long run price impact with inventory risk

> [!faq]- Tips chapter 04
> #### Price with inventory risk
> For $E(\tilde{W}^{No \: Trade}_1)$ and $E(\tilde{W}^{Trade}_1)$ use $\bar{V} = E(\tilde{V})$ and $var(c_0) = 0$. 
> #### Immediate price impact with inventory risk
> Fill in the std formula for $PI_t$ using $p_{i,t} = \bar{V}_i - A \sigma_{i,o} + \frac{A}{2} \sigma^2_i$ and $E(\bar{V}^*_i | \mathbb{F}_{t-1}) = \bar{V}_i - A \sigma_{i,0}$ (= midquote without inventory).

🚧 Under construction 🚧