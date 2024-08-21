[[Order processing costs]] are costs that the dealer incurs when executing an order, received from a trader. These costs can include office costs, salaries, administrative costs, etc. The dealer requires compensation for these costs.

[[Order processing costs]] is a [[Market friction]].
# Background
![[Quote driven market#Organization]]
# Model
## Setup
- One financial asset is traded: $\tilde V$
- Time is divided into periods: $t=0,1,2,3,...$
- Each time $t$, one trader arrives with a 50% chance of buying or selling (arrival process is i.i.d.)
- Traders submit only [[Market order]]s
- Each order is for one unit of the asset
- Traders don't have motives
- The dealer incurs cost $c$ per transaction/unit (because one unit per transaction)
## Bid and ask prices
If a dealer is competitive and risk-neutral, he needs the following [[Ask price]] and [[Bid price]] in order to brake even and cover his costs with $c$:
$$ A_t = \mathbb{E}_t(\tilde V) + c $$
$$ B_t = \mathbb{E}_t(\tilde V) - c $$
$$ S_t = 2c $$
This order cost $c$ is what separates [[Efficient market hypothesis|EMH]] and this model. This creates a friction which results in two prices. The market is no longer perfectly liquid.
## Price impact
The immediate [[Price impact]] of a trade in this model is equal to the order cost in case of a buy and minus order cost in case of a sale:
$$ PI_t = + c \: or \: -c$$
The [[Price impact]] in later periods is zero:
$$ PI_t+s = 0, \: s=1,2,3,...$$
(see proof)
## Imperfect competition
When incorporating rent we can adjust the [[Ask price]], [[Bid price]] and bid-ask spread:
$$ A_t = \mathbb{E}(\tilde V|\mathcal{F}_t) + c +rent $$
$$ B_t = \mathbb{E}(\tilde V|\mathcal{F}_t) - c - rent $$
$$ S_t = 2c + 2rent $$