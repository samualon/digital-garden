Ownership and determining the value of the company are central parts in investing. Valuation is crucial in this, because:
- it determines how much ownership the investor receives for a given investment.
- it allows the investor to estimate expected returns. 
# Notation
| Symbol     | Meaning                                                                       |
| ---------- | ----------------------------------------------------------------------------- |
| $I$        | Investment                                                                    |
| $F_x$      | Ownership share of person $x$                                                 |
| $V$        | Valuation                                                                     |
| $S$        | Number of shares                                                              |
| $S_{pre}$  | Pre-deal owner shares                                                         |
| $S_{post}$ | Post-deal owner shares                                                        |
| $S_{inv}$  | New investors shares                                                          |
| $r$        | Investment round 1, 2, 3, ... , $R$                                           |
| $i$        | The round where an investor investes                                          |
| $F_i(r)$   | The ownership fraction in round $r$ of an investor that invested in round $i$ |
| $X_{ent}$  | Entrepreneurial gains                                                         |
# Mechanics
Two important mechanics of ownership and valuation exist:
- [[Implied valuation]]
- [[Pre- and post-money valuation]]
# Number of shares
In the first [[Funding rounds|funding round]], the number of shares can be chosen freely. In latter [[Funding rounds]], the number of shares is given by:
$$ S_{post} = S_{pre} + S_{inv} $$
This gives the following relations with the price of shares:
$$ I = P * S_{inv} $$
$$ V = P * S $$
This gives the following relation for ownership:
$$ F_{inv} = \frac{S_{inv}}{S_{post}} $$
# [[Stock option pool]]
Stock option pools (SOP) creates new owners, we need to adjust the formulas above:
$$ S_{post} = S_{pre} + S_{inv} + S_{SOP} $$
$$ V_{pre} = P * (S_{pre} + S_{SOP}) $$
$$ F_{pre} = \frac{S_{pre}}{S_{post}} $$

$$ F_{inv} = \frac{S_{inv}}{S_{post}} $$

$$ F_{SOP} = \frac{S_{SOP}}{S_{post}} $$
We assume a *fully diluted base*, which means that we interpret the shares of the SOP as common stock. This means that $V_{pre}$ includes founders and the option holders' shares.

The values invested, shares and ownership fractions can be organized into a [[Capitalization table]]. 
# Ownership dilution
When new investments are made over investment rounds, the shares held by investors before the investment are affected. Their share value is reduced.

In each round, a new valuation is implied:
$$ V_{post}(r) = \frac{I(r)}{F_r(r)} $$
Dilution of ownership across rounds can thus be expressed as:
$$ F_i(r) = F_i(r-1) * (1-F_r(r)) $$
![[Capitalization table under dilution.png]]
# Returns
When we consider investor returns, we have two types of returns:
- [[Realized returns]]: backward-looking and objective
- [[Expected returns]]: forward-looking and based on expectations
## Risk in entrepreneurial finance
A basic principle of risk and return is that higher returns can be achieved by taking on investments with higher risks, but overall investors are [[Risk-aversion|risk-averse]] and want to be compensated for additional risk.

In [[Entrepreneurial finance]] however, two differences exist with typical [[Corporate finance]]:
1. Risk in [[Entrepreneurial finance]] is often extreme (statistical [[Skewness]])
2. Investments also carry [[Liquidity risk]]

Even though risks are usually higher in [[Entrepreneurial finance]], this doesn't mean that these investors are risk-preferent. They're *risk-tolerant*, but will always work to reducing their exposure to risk.
## Measures of returns
Three standard measures of returns:
- [[Net Present Value]]
- [[Internal rate of return]]
- [[Cash on cash multiple]]
### Comparison
|                 | [[Net Present Value\|NPV]]                                                              | [[Internal rate of return\|IRR]]                                                      | [[Cash on cash multiple\|CCM]]            |
| --------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------- |
| *Advantages*    | - Time horizon taken into account<br>- Compare investments with different time horizons | - Time horizon taken into account                                                     | - Easy to use                             |
| *Disadvantages* | - Need for a correct discount rate                                                      | - Can't compare investments with different time horizons (without making assumptions) | - Time horizon **not** taken into account |

For decision-making, the [[Net Present Value|NPV]] should thus be used, but it's not uncommon for reporting to use [[Internal rate of return|IRR]] and [[Cash on cash multiple|CCM]].
## Valuation and returns
For company-level exits using $CCM = \frac{X}{V_{post}}$:
- Higher exit value leads to higher realized investor return
- Higher valuation leads to lower realized investor return

For entrepreneurial gains using $X_{ent} = X x (1- \frac{I}{V_{post}})$:
- A higher exit value $X$ leads to higher entrepreneurial gains
- A higher valuation $V_{post}$ leads to higher entrepreneurial gains

For $V_{post}$ assumed as expected value $\frac{X^e}{CCM^e}$:
- A higher expected exit $X^e$ leads to higher valuation
- A higher required return $CCM^e$ leads to a lower valuation
# Valuation
Venture valuation is determined by four aspects:
- The opportunity itself
- The market environment
- Competition
- Investor quality
# Founder agreements
The [[Founder agreement]]  has to divide the ownership between founders before the company can reach out to investors.

The [[FAST tool]] can help with this split of ownership.