---
aliases:
  - CAL
---
The capital allocation line summarizes the feasibility set of portfolios.
## CAL of two assets
The formula for the CAL of two assets (a risky and risk-free asset) is as follows:
$$ 
E(R_C) = R_F + \frac{ (E(R_P) + R_F)}{\sigma_P}\sigma_C 
$$
 where the intercept with the y-axis is $R_F$ and the slope $\frac{E(R_P) - R_F}{\sigma_P}$ is the [[Sharpe ratio]] of the  risky asset.
### Comments
All portfolios which combine assets $F$ and $P$ lay on this CAL and thus have the same [[Sharpe ratio]]. We can only change the [[Sharpe ratio]] if we add stocks or other risky assets to the risky portfolio $P$.

In reality, you won't be able to leverage at the risk-free rate $R_F$. This is why the [[Sharpe ratio]] will decrease when [[Leverage|leveraging]]. ![[CAL when leveraging in reality.png]]
