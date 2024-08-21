The price impact of a trade made at time $t$ at time $t+s$ with $s=0,1,2,3,...$ is the difference between the expected transaction price at time $t+s$ (which is conditional on all prior information and the trade direction) and the expected fundamental value of the asset before the trade:
$$ PI_{t+s} = \mathbb{E}[p_{t+s}|\mathcal{F_{t-1}},d_t] - \mathbb{E}[\tilde V|\mathcal{F_{t-1}}]$$
With trade direction at time $t$ $=d_t$ with $d_t=1$ in case of a buy and $d_t = -1$ in case of a sell.

The immediate price impact is then:
$$ PI_t = \mathbb{E}[p_{t}|\mathcal{F_{t-1}},d_t] - \mathbb{E}[\tilde V|\mathcal{F_{t-1}}]$$